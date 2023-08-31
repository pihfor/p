<script>
// import Layout from "../../../layouts/main.vue";
// import appConfig from "../../../../app.config";
import "@vueform/multiselect/themes/default.css";
import Lottie from "@/components/widgets/lottie.vue";
import animationData from "@/components/widgets/msoeawqm.json";
import animationData1 from "@/components/widgets/gsqxdxog.json";
import Swal from "sweetalert2";
import flatPickr from "vue-flatpickr-component";
import "flatpickr/dist/flatpickr.css";


export default {
  page: {
    title: "Complains",
    // meta: [{ name: "description", content: appConfig.description }],
  },
  data() {
    return {
      title: "Complains",
      items: [
        {
          text: "",
          href: "/",
        },
        {
          text: "Complains",
          active: true,
        },
      ],
      createAppModal: false,
      status: null,
      status1: null,
      value: null,
      value1: null,
      searchQuery: null,
      statusvalue: null,
      jobvalue: null,
      date2: null,
      timeConfig: {
        enableTime: false,
        dateFormat: "d M, Y",
      },
      page: 1,
      perPage: 8,
      pages: [],
      statuscategory: 'All',
      complain: [
        {
          id: "1",
          img: require("@/assets/images/companies/img-4.png"),
          name: "Syntyce Solutions",
          description: "Exam marks",
          date: "30 Sep, 2022",
          contacts: "785-685-4616",
          type: "Full Time",
          status: "Rejected"
        },
        {
          id: "2",
          img: require("@/assets/images/brands/slack.png"),
          name: "Plunkett Infotech",
          description: "first semester course",
          date: "26 Sep, 2022",
          contacts: "734-544-2407",
          type: "Full Time",
          status: "New"
        }, {
          id: "3",
          img: require("@/assets/images/companies/img-4.png"),
          name: "Martin's",
          description: "CA marks",
          date: "26 Sep, 2022",
          contacts: "303-606-1985",
          type: "Part Time",
          status: "New"
        }, {
          id: "4",
          img: require("@/assets/images/companies/img-3.png"),
          name: "Meta4Systems",
          description: "CA marks",
          date: "27 Sep, 2022",
          contacts: "610-440-0592",
          type: "Part Time",
          status: "Rejected"
        }, {
          id: "5",
          img: require("@/assets/images/companies/img-4.png"),
          name: "Grey Fade",
          description: "level one course",
          date: "28 Sep, 2022",
          contacts: "907-452-3702",
          type: "level one course",
          status: "Pending"
        }, 
      ],
      defaultOptions: {
        animationData: animationData
      },
      defaultOptions1: {
        animationData: animationData1
      },
      isType: null,
    };
  },
  computed: {
    displayedPosts() {
      return this.paginate(this.complain);
    },
    resultQuery() {
      if (this.searchQuery) {
        const search = this.searchQuery.toLowerCase();
        return this.displayedPosts.filter((data) => {
          return (
            data.name.toLowerCase().includes(search) ||
            data.description.toLowerCase().includes(search) ||
            data.contacts.toLowerCase().includes(search) ||
            data.status.toLowerCase().includes(search)
          );
        });
      } else if (this.status !== null || this.value !== null) {
        return this.displayedPosts.filter((data) => {
          if (this.status != null && this.value != null) {
            if (this.status === data.status) {
              if (this.value === data.type) {
                return data;
              } else if (this.value == 'All') {
                return data;
              }
            } else if (this.value == 'All' && this.status == 'All') {
              return data;
            } else if (this.status == 'All') {
              if (this.value === data.type) {
                return data;
              }
            }
          } else if (this.status === data.status) {
            return data;
          } else if (this.value === data.type) {
            return data;
          } else if (this.status == 'All' || this.value == 'All') {
            return data;
          }
          else {
            return null;
          }
        });
      } else {
        return this.displayedPosts;
      }
    },
  },
  watch: {
    complain() {
      this.setPages();
    },
  },
  created() {
    this.setPages();
  },
  methods: {
    setPages() {
      let numberOfPages = Math.ceil(this.complain.length / this.perPage);
      this.pages = [];
      for (let index = 1; index <= numberOfPages; index++) {
        this.pages.push(index);
      }
    },
    paginate(complain) {
      let page = this.page;
      let perPage = this.perPage;
      let from = page * perPage - perPage;
      let to = page * perPage;
      return complain.slice(from, to);
    },
    changecategory(data) {
      this.statuscategory = data;
    },
    onChangeStatus(e) {
      this.statuscategory = e;
    },
    onChangeType(e) {
      this.isType = e;
    },
    SearchData() {
      this.resultQuery;
      this.status = this.status1;
      this.value = this.value1;
    },

    handleComplaindetails(e, item) {
      this.createAppModal = true;
      const modalHeader = document.querySelector('.exampleModalLabel');
      const addbtn = document.getElementById('add-btn');
      const editbtn = document.getElementById('edit-btn');

      if (e.path[1].id == "create-btn") {
        document.getElementById("addform").reset();
        modalHeader.innerHTML = "Add Complain";
        addbtn.style.display = 'block';
        editbtn.style.display = 'none';

      } else {
        modalHeader.innerHTML = "Edit Complain";
        addbtn.style.display = 'none';
        editbtn.style.display = 'block';

        document.getElementById("id-field").value = item.id;
        document.getElementById("name").value = item.name;
        document.getElementById("description-field").value = item.description;
        document.getElementById("date-field").value = item.date;
        document.getElementById("contact-field").value = item.contacts;
      }
    },

    deleteComplain(event) {
      Swal.fire({
        title: "Are you sure?",
        text: "You won't be able to revert this!",
        icon: "warning",
        showCancelButton: true,
        cancelButtonColor: "#f46a6a",
        confirmButtonColor: "#34c38f",
        confirmButtonText: "Yes, delete it!",
      }).then((result) => {
        if (result.value) {
          console.log("this.complain.indexOf(event)", this.complain.indexOf(event));
          this.complain.splice(this.complain.indexOf(event), 1);
          Swal.fire("Deleted!", "Your file has been deleted.", "success");
        }
      });
    },

    deleteMultiple() {
      let ids_array = [];
      var items = document.getElementsByName("chk_child");
      items.forEach(function (ele) {
        if (ele.checked == true) {
          var trNode = ele.parentNode.parentNode.parentNode;
          var newid = trNode.querySelector(".id a").innerHTML;
          var id = newid.slice(3);
          ids_array.push(id);
        }
      });
      if (typeof ids_array !== "undefined" && ids_array.length > 0) {
        if (confirm("Are you sure you want to delete this?")) {
          var cusList = this.complain;
          ids_array.forEach(function (id) {
            cusList = cusList.filter(function (complain) {
              console.log('complain', complain);
              return complain.id != id;
            });
          });
          this.complain = cusList;
          document.getElementById("checkAll").checked = false;
          var itemss = document.getElementsByName("chk_child");
          itemss.forEach(function (ele) {
            if (ele.checked == true) {
              ele.checked = false;
              ele.closest("tr").classList.remove("table-active");
            }
          });
        } else {
          return false;
        }
      } else {
        Swal.fire({
          title: "Please select at least one checkbox",
          confirmButtonClass: "btn btn-info",
          buttonsStyling: false,
          showCloseButton: true,
        });
      }
    },

    handlecomplain() {
      const companyfield = document.getElementById('name').value;
      const descriptionfield = document.getElementById('description-field').value;
      const contactfield = document.getElementById('contact-field').value;
      const date = document.getElementById('date-field').value;
      const closebtn = document.getElementById("close-modal");

      if (document.querySelector('.exampleModalLabel').innerHTML == "Add complain") {
        const id = this.complain.length + 1;

        if (id != null && companyfield != null && descriptionfield != null && contactfield != null) {
          const data = {
            id: id,
            img: require("@/assets/images/companies/img-4.png"),
            name: companyfield,
            description: descriptionfield,
            contacts: contactfield,
            date: (date || new Date().toUTCString().slice(5, 16)),
            type: (this.jobvalue || "Full Time"),
            status: (this.statusvalue || "New")
          };
          closebtn.click();
          this.complain.unshift(data);
        }
        document.getElementById("addform").reset();
      } else {
        this.complain;
        const id = document.getElementById("id-field").value;

        this.complain.forEach(element => {
          if (element.id.toString() == id.toString()) {
            element.name = companyfield,
              element.description = descriptionfield,
              element.contacts = contactfield,
              element.date = (date || new Date().toUTCString().slice(5, 16)),
              element.type = (this.jobvalue || "Full Time"),
              element.status = (this.statusvalue || "New");
          }
        });
        closebtn.click();
      }
    }

  },
  components: {
    // Layout,
    lottie: Lottie,
    flatPickr
  },
  mounted() {
    var checkAll = document.getElementById("checkAll");
    if (checkAll) {
      checkAll.onclick = function () {
        var checkboxes = document.querySelectorAll(
          '.form-check-all input[type="checkbox"]'
        );

        if (checkAll.checked == true) {
          checkboxes.forEach(function (checkbox) {
            checkbox.checked = true;
            checkbox.closest("tr").classList.add("table-active");
            document.getElementById('remove-actions').style.display = 'block';
          });
        } else {
          checkboxes.forEach(function (checkbox) {
            checkbox.checked = false;
            checkbox.closest("tr").classList.remove("table-active");
            document.getElementById('remove-actions').style.display = 'none';
          });
        }
      };
    }

    var checkboxes = document.querySelectorAll('#complainList .form-check-input');
    Array.from(checkboxes).forEach(function (element) {
      element.addEventListener('change', function (event) {
        var checkedCount = document.querySelectorAll('#complainList .form-check-input:checked').length;

        if (event.target.closest("tr").classList.contains("table-active")) {
          (checkedCount > 0) ? document.getElementById("remove-actions").style.display = 'block' : document.getElementById("remove-actions").style.display = 'none';
        } else {
          (checkedCount > 0) ? document.getElementById("remove-actions").style.display = 'block' : document.getElementById("remove-actions").style.display = 'none';
        }
      });
    });
  }
};
</script>

<template>
  <div>
    <b-row>
      <b-col lg="12">
        <b-card no-body>
          <b-card-header class=" d-md-flex border-0">
            <div class="d-md-flex align-items-center">
              <h5 class="card-title mb-3 mb-md-0 flex-grow-1">COMPLAINS</h5>
            </div>
          </b-card-header>
        </b-card>
        <b-card>
          <b-card-body>
            <b-row>
                <b-col class="text-md-end p-2">
                    <div>
                        <b-button class="text-md-end" type="button" variant="primary" @click="createAppModal = !createAppModal">
                            Add Complain
                        </b-button>
                    </div>
                </b-col>
            </b-row>
           
          </b-card-body>
          <b-card-body>
            <div>
              <div class="table-responsive table-card mb-1">
                <table class="table table-nowrap align-middle" id="jobListTable">
                  <thead class="text-muted table-light">
                    <tr class="text-uppercase">
                      <th class="sort" data-sort="id" style="width: 140px;">Complain ID</th>
                      <th class="sort" data-sort="company">Name</th>
                      <th class="sort" data-sort="description">Description</th>
                      <th class="sort" data-sort="date">Submission Date</th>
                      <th class="sort" data-sort="contacts">Contacts</th>
                      <th class="sort" data-sort="status">Status</th>
                      <th class="sort" data-sort="city">Action</th>
                    </tr>
                  </thead>
                  <tbody class="list form-check-all" v-for="(data, index) of resultQuery" :key="index">
                    <tr v-if="statuscategory == 'All' || statuscategory == data.status">
                      <td class="id">
                        <b-link href="#" class="fw-medium link-primary">{{ data.id }}</b-link>
                      </td>
                      <td class="company">
                        <div class="d-flex align-items-center">
                          <div class="flex-grow-1 ms-2">{{ data.name }}</div>
                        </div>
                      </td>
                      <td class="description">{{ data.description }}</td>
                      <td class="date">{{ data.date }}</td>
                      <td class="contacts">{{ data.contacts }}</td>
                      <td class="status"><span class="badge text-uppercase" :class="{
                          'badge-soft-success': data.status == 'Approved',
                          'badge-soft-warning': data.status == 'Pending',
                          'badge-soft-danger': data.status == 'Rejected',
                          'badge-soft-info': data.status == 'New',
                        }">{{ data.status }}</span>
                      </td>
                      <td>
                        <ul class="list-inline hstack gap-2 mb-0">
                          <li class="list-inline-item" v-b-tooltip.hover title="View">
                            <b-link href="/complainsingle" class="text-primary d-inline-block">
                              <i class="ri-eye-fill fs-16"></i>
                            </b-link>
                          </li>
                          <li class="list-inline-item" data-bs-toggle="tooltip" data-bs-trigger="hover"
                            data-bs-placement="top" title="Remove">
                            <b-link class="text-danger d-inline-block remove-item-btn" @click="deleteComplain(data)">
                              <i class="ri-delete-bin-5-fill fs-16"></i>
                            </b-link>
                          </li>
                        </ul>
                      </td>
                    </tr>
                  </tbody>
                </table>
                <div class="noresult" style="display: none" :class="{ 'd-block': resultQuery.length == 0 }">
                  <div class="text-center">
                    <lottie class="avatar-xl" colors="primary:#121331,secondary:#08a88a" :options="defaultOptions"
                      :height="75" :width="75" />
                    <h5 class="mt-2">Sorry! No Result Found</h5>
                    <p class="text-muted mb-0">
                      We've searched more than 150+ result We did not find jobs for you search.
                    </p>
                  </div>
                </div>
              </div>



              <div class="d-flex justify-content-end">
                <div class="pagination-wrap hstack gap-2">
                  <b-link class="page-item pagination-prev disabled" href="#" v-if="page != 1" @click="page--">
                    Previous
                  </b-link>
                  <ul class="pagination listjs-pagination mb-0">
                    <li :class="{ active: pageNumber == page, disabled: pageNumber == '...', }"
                      v-for="(pageNumber, index) in pages" :key="index" @click="page = pageNumber">
                      <b-link class="page" href="#">{{ pageNumber }}</b-link>
                    </li>
                  </ul>
                  <b-link class="page-item pagination-next" href="#" @click="page++" v-if="page < pages.length">
                    Next
                  </b-link>
                </div>
              </div>
            </div>

            <!-- create app modal  -->
            <b-modal v-model="createAppModal" id="showModal" title-class="exampleModalLabel" hide-footer
              class="v-modal-custom" centered no-close-on-backdrop>
              <b-form action="#" autocomplete="off" id="addform" class="tablelist-form">
                <input type="hidden" id="id-field" />

                <div class="mb-3 d-none" id="modal-id">
                  <label for="complainId" class="form-label">ID</label>
                  <input type="text" id="complainId" class="form-control" placeholder="ID" readonly />
                </div>

                <div class="mb-3">
                  <label for="name" class="form-label">Name</label>
                  <input type="text" id="name" class="form-control" placeholder="Enter name"
                    required />
                </div>

                <div class="mb-3">
                  <label for="description-field" class="form-label">description</label>
                  <input type="text" id="description-field" class="form-control" placeholder="Enter description"
                    required />
                </div>

                <div class="mb-3">
                  <label for="date-field" class="form-label">Date</label>
                  <flat-pickr id="date-field" placeholder="Select date" v-model="date2" :config="timeConfig"
                    class="form-control flatpickr-input"></flat-pickr>
                </div>

                <div class="mb-3">
                  <label for="contact-field" class="form-label">Contact Info</label>
                  <input type="text" id="contact-field" class="form-control" placeholder="Enter contact" required />
                </div>

                <b-row class="gy-4 mb-3">
                  <b-col md="6">
                    <label for="file" class="form-label">Upload File</label>
                    <input type="file">
                  </b-col>
                </b-row>

                <div class="hstack gap-2 justify-content-end mt-3">
                  <b-button type="button" variant="light" id="close-modal" @click="createAppModal = false">Close
                  </b-button>
                  <b-button type="button" variant="success" id="add-btn" @click="handleComplain">Add</b-button>
                  <b-button type="button" variant="success" id="edit-btn" @click="handleComplain">Update
                  </b-button>
                </div>
              </b-form>
            </b-modal>
          </b-card-body>
        </b-card>
      </b-col>
    </b-row>
  </div>
</template>