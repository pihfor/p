<script>
// import Layout from "../../../layouts/main.vue";
// import appConfig from "../../../../app.config";

export default {
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
//   components: {
//     Layout,
//   },
};
</script>

<template>
  <Layout>
    <b-card>
         <b-card-header>
            <div class="d-md-flex align-items-center">
            <h5 class="card-title mb-3 mb-md-0 flex-grow-1">COMPLAINS</h5>
            </div>
        </b-card-header>
    </b-card>

    
    <b-row class="mt-2">
      <b-col xxl="3">
        <b-card no-body>
          <b-card-header>
            <h5 class="mb-0">Complain Overview</h5>
          </b-card-header>
          <b-card-body>
            <div class="table-responsive table-card">
              <table class="table mb-0">
                <tbody>
                  <tr>
                    <td class="fw-medium">Name :</td>
                    <td>Syntyce Solutions</td>
                  </tr>
                  <tr>
                    <td class="fw-medium">Matricule :</td>
                    <td>Uba12njnfi</td>
                  </tr>
                  <tr>
                    <td class="fw-medium">Date :</td>
                    <td>02 Sep, 2022</td>
                  </tr>
                  <tr>
                    <td class="fw-medium"> Contact :</td>
                    <td>785-685-4616</td>
                  </tr>
                </tbody>
              </table>

            </div>
          </b-card-body>
        </b-card>
      </b-col>
      <b-col xxl="9">
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
                            <b-link class="nav-link active" data-bs-toggle="tab" href="#home-1" role="tab">
                                Comments (2)
                            </b-link>
                        </li>
                        <li class="nav-item">
                            <b-link class="nav-link" data-bs-toggle="tab" href="#messages-1" role="tab">
                                Attachments File (4)
                            </b-link>
                        </li>
                    </ul>
                </div>
            </b-card-header>
            <b-card-body>
                <div class="tab-content">
                    <div class="tab-pane active" id="home-1" role="tabpanel">
                        <h5 class="card-title mb-4">Comments</h5>
                        <div data-simplebar style="height:auto;" class="px-3 mx-n3 mb-2">
                            <div class="d-flex mb-4">
                                <div class="flex-shrink-0">
                                    <img src="@/assets/images/users/avatar-7.jpg" alt=""
                                        class="avatar-xs rounded-circle" />
                                </div>
                                <div class="flex-grow-1 ms-3">
                                    <h5 class="fs-13">
                                        <router-link to="/pages/profile">Joseph Parker</router-link> <small
                                            class="text-muted">20 Dec 2021 - 05:47AM</small>
                                    </h5>
                                    <p class="text-muted">I am getting message from customers that when they
                                        place order always get error message .</p>
                                    <b-link href="javascript: void(0);" class="badge text-muted bg-light"><i
                                            class="mdi mdi-reply"></i> Reply</b-link>
                                    <div class="d-flex mt-4">
                                        <div class="flex-shrink-0">
                                            <img src="@/assets/images/users/avatar-10.jpg" alt=""
                                                class="avatar-xs rounded-circle" />
                                        </div>
                                        <div class="flex-grow-1 ms-3">
                                            <h5 class="fs-13">
                                                <router-link to="/pages/profile">Tonya Noble</router-link>
                                                <small class="text-muted">22 Dec 2021 - 02:32PM</small>
                                            </h5>
                                            <p class="text-muted">Please be sure to check your Spam mailbox to
                                                see if your email filters have identified the email from Dell as
                                                spam.</p>
                                            <b-link href="javascript: void(0);"
                                                class="badge text-muted bg-light"><i class="mdi mdi-reply"></i>
                                                Reply</b-link>
                                        </div>
                                    </div>
                                </div>
                            </div>
                        </div>
                        <form class="mt-4">
                            <b-row class="g-3">
                                <b-col lg="12">
                                    <label for="exampleFormControlTextarea1" class="form-label">Leave a
                                        Comments</label>
                                    <textarea class="form-control bg-light border-light"
                                        id="exampleFormControlTextarea1" rows="3"
                                        placeholder="Enter comments"></textarea>
                                </b-col>
                                <b-col cols="12" class="text-end">
                                    <b-button type="button" variant="ghost-secondary" class="btn-icon me-1"><i
                                            class="ri-attachment-line fs-16"></i></b-button>
                                    <b-link href="javascript:void(0);" class="btn btn-success">Post Comments
                                    </b-link>
                                </b-col>
                            </b-row>
                        </form>
                    </div>
                    <div class="tab-pane" id="messages-1" role="tabpanel">
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
                                                    <li>
                                                        <b-link class="dropdown-item"
                                                            href="javascript:void(0);"><i
                                                                class="ri-delete-bin-5-line me-2 align-middle text-muted"></i>Delete
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
                                                    <li>
                                                        <b-link class="dropdown-item"
                                                            href="javascript:void(0);"><i
                                                                class="ri-delete-bin-5-line me-2 align-middle text-muted"></i>Delete
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
                                                    <li>
                                                        <b-link class="dropdown-item"
                                                            href="javascript:void(0);"><i
                                                                class="ri-delete-bin-5-line me-2 align-middle"></i>Delete
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
                                                    <li>
                                                        <b-link class="dropdown-item"
                                                            href="javascript:void(0);"><i
                                                                class="ri-delete-bin-5-line me-2 align-middle"></i>Delete
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
        </b-card>
      </b-col>
    </b-row>
  </Layout>
</template>