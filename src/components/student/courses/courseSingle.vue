<script>

import { ref, watch } from "vue";
import useVuelidate from "@vuelidate/core";

import DropZone from "@/components/widgets/dropZone";

// import Layout from "../../../layouts/main.vue";
// import appConfig from "../../../../app.config";

export default {
    methods: {
    deleteRecord(ele) {
      ele.target.parentElement.parentElement.parentElement.remove();
    },
  },
  setup() {
    let files = ref([]);
    let dropzoneFile = ref("");
    const drop = (e) => {
      dropzoneFile.value = e.dataTransfer.files[0];
      files.value.push(dropzoneFile.value);
    };
    const selectedFile = () => {
      dropzoneFile.value = document.querySelector(".dropzoneFile").files[0];
      files.value.push(dropzoneFile.value);
    };
    watch(
      () => [...files.value],
      (currentValue) => {
        return currentValue;
      }
    );

    return { dropzoneFile, files, drop, selectedFile, v$: useVuelidate() };
  },
  page: {
    title: "Starter",
    // meta: [{ name: "description", content: appConfig.description }],
  },
  data() {
    return {
      title: "complain",
      items: [
        {
          text: "complains",
          href: "/",
        },
        {
          text: "complain",
          active: true,
        },
      ],
    };
  },
  components: {
    // Layout,
    DropZone,
  },
};
</script>

<template>
  <div>
    <b-card>
         <b-card-header>
            <div class="d-md-flex align-items-center">
            <h5 class="card-title mb-3 mb-md-0 flex-grow-1">Computer Graphics</h5>
            </div>
        </b-card-header>
    </b-card>

    
    <b-row class="mt-2">
      <b-col xxl="12">
        <b-card no-body>
          <b-card-body>
            <h5 class="mb-3">Description</h5>

            <p class="text-muted mb-2">A Product Designer of a company is responsible for the user experience of a
              product, which usually includes taking direction on the business goals and objectives from product
              management. Product Designers are typically associated with the visual or tactile aspects of a product
              but sometimes they can also play a role in the information architecture and system design of a product.
            </p>
            <p class="text-muted mb-4">Product designer is an exceptional career choice. The demand for product
              designers is increasing with each passing day but there is a huge shortage for a skilful product
              designer in the market. With hard work and an apt skill set, a product designer can make a handsome
              amount of money.</p>
          </b-card-body>
        </b-card>

        <b-card no-body>
            <b-card-header>
                <div>
                    <ul class="nav nav-tabs-custom rounded card-header-tabs border-bottom-0" role="tablist">
                        <li class="nav-item">
                            <b-link class="nav-link active" data-bs-toggle="tab" href="#notes" role="tab">
                                Notes
                            </b-link>
                        </li>
                        <li class="nav-item">
                            <b-link class="nav-link" data-bs-toggle="tab" href="#assignments" role="tab">
                                Assignments
                            </b-link>
                        </li>
                    </ul>
                </div>
            </b-card-header>
            <b-card-body>
                <div class="tab-content">
                    <div class="tab-pane active" id="notes" role="tabpanel">
                        <div class="table-responsive table-card">
                            <table class="table table-borderless align-middle mb-0">
                                <thead class="table-light text-muted">
                                    <tr>
                                        <th scope="col">File Name</th>
                                        <th scope="col">Type</th>
                                        <th scope="col">Size</th>
                                        <th scope="col">Upload Date</th>
                                        <th scope="col">Action</th>
                                    </tr>
                                </thead>
                                <tbody>
                                    <tr>
                                        <td>
                                            <div class="d-flex align-items-center">
                                                <div class="avatar-sm">
                                                    <div
                                                        class="avatar-title bg-soft-primary text-primary rounded fs-20">
                                                        <i class="ri-file-zip-fill"></i>
                                                    </div>
                                                </div>
                                                <div class="ms-3 flex-grow-1">
                                                    <h6 class="fs-15 mb-0">
                                                        <b-link href="javascript:void(0)">App
                                                            pages.zip</b-link>
                                                    </h6>
                                                </div>
                                            </div>
                                        </td>
                                        <td>Zip File</td>
                                        <td>2.22 MB</td>
                                        <td>21 Dec, 2021</td>
                                        <td>
                                            <div class="dropdown">
                                                <b-link href="javascript:void(0);"
                                                    class="btn btn-light btn-icon" id="dropdownMenuLink1"
                                                    data-bs-toggle="dropdown" aria-expanded="true">
                                                    <i class="ri-equalizer-fill"></i>
                                                </b-link>
                                                <ul class="dropdown-menu dropdown-menu-end"
                                                    aria-labelledby="dropdownMenuLink1"
                                                    data-popper-placement="bottom-end"
                                                    style="position: absolute; inset: 0px 0px auto auto; margin: 0px; transform: translate(0px, 23px);">
                                                    <li>
                                                        <b-link class="dropdown-item"
                                                            href="javascript:void(0);"><i
                                                                class="ri-eye-fill me-2 align-middle text-muted"></i>View
                                                        </b-link>
                                                    </li>
                                                    <li>
                                                        <b-link class="dropdown-item"
                                                            href="javascript:void(0);"><i
                                                                class="ri-download-2-fill me-2 align-middle text-muted"></i>Download
                                                        </b-link>
                                                    </li>
                                                    <li class="dropdown-divider"></li>
                                                </ul>
                                            </div>
                                        </td>
                                    </tr>
                                    <tr>
                                        <td>
                                            <div class="d-flex align-items-center">
                                                <div class="avatar-sm">
                                                    <div
                                                        class="avatar-title bg-soft-danger text-danger rounded fs-20">
                                                        <i class="ri-file-pdf-fill"></i>
                                                    </div>
                                                </div>
                                                <div class="ms-3 flex-grow-1">
                                                    <h6 class="fs-15 mb-0">
                                                        <b-link href="javascript:void(0);">Velzon
                                                            admin.ppt</b-link>
                                                    </h6>
                                                </div>
                                            </div>
                                        </td>
                                        <td>PPT File</td>
                                        <td>2.24 MB</td>
                                        <td>25 Dec, 2021</td>
                                        <td>
                                            <div class="dropdown">
                                                <b-link href="javascript:void(0);"
                                                    class="btn btn-light btn-icon" id="dropdownMenuLink2"
                                                    data-bs-toggle="dropdown" aria-expanded="true">
                                                    <i class="ri-equalizer-fill"></i>
                                                </b-link>
                                                <ul class="dropdown-menu dropdown-menu-end"
                                                    aria-labelledby="dropdownMenuLink2"
                                                    data-popper-placement="bottom-end"
                                                    style="position: absolute; inset: 0px 0px auto auto; margin: 0px; transform: translate(0px, 23px);">
                                                    <li>
                                                        <b-link class="dropdown-item"
                                                            href="javascript:void(0);"><i
                                                                class="ri-eye-fill me-2 align-middle text-muted"></i>View
                                                        </b-link>
                                                    </li>
                                                    <li>
                                                        <b-link class="dropdown-item"
                                                            href="javascript:void(0);"><i
                                                                class="ri-download-2-fill me-2 align-middle text-muted"></i>Download
                                                        </b-link>
                                                    </li>
                                                    <li class="dropdown-divider"></li>
                                                </ul>
                                            </div>
                                        </td>
                                    </tr>
                                    <tr>
                                        <td>
                                            <div class="d-flex align-items-center">
                                                <div class="avatar-sm">
                                                    <div
                                                        class="avatar-title bg-soft-info text-info rounded fs-20">
                                                        <i class="ri-folder-line"></i>
                                                    </div>
                                                </div>
                                                <div class="ms-3 flex-grow-1">
                                                    <h6 class="fs-15 mb-0">
                                                        <b-link href="javascript:void(0);">Images.zip</b-link>
                                                    </h6>
                                                </div>
                                            </div>
                                        </td>
                                        <td>ZIP File</td>
                                        <td>1.02 MB</td>
                                        <td>28 Dec, 2021</td>
                                        <td>
                                            <div class="dropdown">
                                                <b-link href="javascript:void(0);"
                                                    class="btn btn-light btn-icon" id="dropdownMenuLink3"
                                                    data-bs-toggle="dropdown" aria-expanded="true">
                                                    <i class="ri-equalizer-fill"></i>
                                                </b-link>
                                                <ul class="dropdown-menu dropdown-menu-end"
                                                    aria-labelledby="dropdownMenuLink3"
                                                    data-popper-placement="bottom-end"
                                                    style="position: absolute; inset: 0px 0px auto auto; margin: 0px; transform: translate(0px, 23px);">
                                                    <li>
                                                        <b-link class="dropdown-item"
                                                            href="javascript:void(0);"><i
                                                                class="ri-eye-fill me-2 align-middle"></i>View
                                                        </b-link>
                                                    </li>
                                                    <li>
                                                        <b-link class="dropdown-item"
                                                            href="javascript:void(0);"><i
                                                                class="ri-download-2-fill me-2 align-middle"></i>Download
                                                        </b-link>
                                                    </li>
                                                </ul>
                                            </div>
                                        </td>
                                    </tr>
                                    <tr>
                                        <td>
                                            <div class="d-flex align-items-center">
                                                <div class="avatar-sm">
                                                    <div
                                                        class="avatar-title bg-soft-danger text-danger rounded fs-20">
                                                        <i class="ri-image-2-fill"></i>
                                                    </div>
                                                </div>
                                                <div class="ms-3 flex-grow-1">
                                                    <h6 class="fs-15 mb-0">
                                                        <b-link href="javascript:void(0);">Bg-pattern.png
                                                        </b-link>
                                                    </h6>
                                                </div>
                                            </div>
                                        </td>
                                        <td>PNG File</td>
                                        <td>879 KB</td>
                                        <td>02 Nov 2021</td>
                                        <td>
                                            <div class="dropdown">
                                                <b-link href="javascript:void(0);"
                                                    class="btn btn-light btn-icon" id="dropdownMenuLink4"
                                                    data-bs-toggle="dropdown" aria-expanded="true">
                                                    <i class="ri-equalizer-fill"></i>
                                                </b-link>
                                                <ul class="dropdown-menu dropdown-menu-end"
                                                    aria-labelledby="dropdownMenuLink4"
                                                    data-popper-placement="bottom-end"
                                                    style="position: absolute; inset: 0px 0px auto auto; margin: 0px; transform: translate(0px, 23px);">
                                                    <li>
                                                        <b-link class="dropdown-item"
                                                            href="javascript:void(0);"><i
                                                                class="ri-eye-fill me-2 align-middle"></i>View
                                                        </b-link>
                                                    </li>
                                                    <li>
                                                        <b-link class="dropdown-item"
                                                            href="javascript:void(0);"><i
                                                                class="ri-download-2-fill me-2 align-middle"></i>Download
                                                        </b-link>
                                                    </li>
                                                </ul>
                                            </div>
                                        </td>
                                    </tr>
                                </tbody>
                            </table>
                        </div>
                    </div>
                </div>
            </b-card-body> 

            <b-card-body>
                <div class="tab-content">
                    <div class="tab-pane" id="assignments" role="tabpanel">                     
                        <div>
                            <p class="text-muted">
                            Drag and drop files here to upload them.
                            </p>
                            <DropZone @drop.prevent="drop" @change="selectedFile" />
                            <ul class="list-unstyled mb-0 mt-3" id="dropzone-preview">
                            <div class="border rounded" v-for="(file, index) of files" :key="index">
                                <div class="d-flex p-2">
                                <div class="flex-grow-1">
                                    <div class="pt-1">
                                    <h5 class="fs-14 mb-1" data-dz-name="">
                                        {{ file.name }}
                                    </h5>
                                    <p class="fs-13 text-muted mb-0" data-dz-size="">
                                        <strong>{{ file.size / 1024 }}</strong> KB
                                    </p>
                                    <strong class="error text-danger" data-dz-errormessage=""></strong>
                                    </div>
                                </div>
                                <div class="flex-shrink-0 ms-3">
                                    <b-button variant="danger" size="sm" data-dz-remove="" @click="deleteRecord">
                                    Delete
                                    </b-button>
                                </div>
                                </div>
                            </div>
                            </ul>
                        </div>
                    </div>
                </div>
            </b-card-body>
        </b-card>
      </b-col>
    </b-row>
  </div>
</template>