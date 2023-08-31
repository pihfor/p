<script>
// import Layout from "../../layouts/main.vue";
// import appConfig from "../../../app.config";

export default {
  page: {
    title: "Home",
    // meta: [{ name: "description", content: appConfig.description }],
  },
  data() {
    return {
      title: "Home",
      items: [
        {
          text: "",
          href: "/",
        },
        {
          text: "Home",
          active: true,
        },
      ],
      thumbsSwiper: null,
    };
  },
//   components: {
//     Layout,
//   },
};
</script>

<template>
  <!-- <Layout> -->

    <div class="profile-foreground">
      <div class="profile-wid-bg">
        <img src="@/assets/images/profile-bg.jpg" alt="" class="profile-wid-img" />
      </div>
    </div>
    <b-row class="mt-5 pt-3">
        <b-col md="3" xxl="3">
            <b-card no-body id="contact-view-detail">
            <b-card-body class="text-center">
                <div class="position-relative d-inline-block">
                <img src="@/assets/images/users/avatar-10.jpg" id="image" alt=""
                    class="avatar-lg rounded-circle img-thumbnail">
                <span class="contact-active position-absolute rounded-circle bg-success"><span
                    class="visually-hidden"></span></span>
                </div>
                <h5 class="mt-4 mb-1" id="name">Hi Ngu! </h5>
                <p class="text-muted" id="#">Lv 300</p>
                <h6 class="mt-2 mb-2" id="name">Acad Year : 2023/2024</h6>
                <ul class="list-inline mb-0">
                <li class="list-inline-item avatar-xs">
                    <b-link href="javascript:void(0);" class="avatar-title bg-soft-success text-success fs-15 rounded">
                    <i class="ri-phone-line"></i>
                    </b-link>
                </li>
                <li class="list-inline-item avatar-xs">
                    <b-link href="javascript:void(0);" class="avatar-title bg-soft-danger text-danger fs-15 rounded">
                    <i class="ri-mail-line"></i>
                    </b-link>
                </li>
                <li class="list-inline-item avatar-xs">
                    <b-link href="javascript:void(0);" class="avatar-title bg-soft-warning text-warning fs-15 rounded">
                    <i class="ri-question-answer-line"></i>
                    </b-link>
                </li>
                </ul>
            </b-card-body>
            <b-card-body class="text-center">
            <b-button  variant="success">Download Student Guide</b-button>
            </b-card-body>
            </b-card>
        </b-col>

        <b-col md="9" xxl="9">
            <b-card no-body id="contact-view-detail" class="bg-white"> 
            <div class="text-center p-4">You've  Completed Fees and Medicals!</div>
            <p class="text-danger text-center"> Report to your  department if the  information below is incorrect</p>
            </b-card>
            <b-card  no-body>
            <b-card-header class="p-3 mb-4 w-100 card-title">
                <h4 class=" "> Basic Information</h4>
            </b-card-header>
            <b-card-body>
                <b-row col="12" class="mb-3">
                    <b-col lg="4">
                        <tr>
                            <th class="text-muted">Name : </th>
                            <td class="text-muted"> Ngu Lumfor Laura</td>
                        </tr>
                    </b-col>
                    <b-col lg="4">
                        <tr>
                            <th class="text-muted">Degree : </th>
                            <td class="text-muted"> Bsc FST</td>
                        </tr>
                    </b-col>
                    <b-col lg="4">
                        <tr>
                            <th class="text-muted">Matricule: </th>
                            <td class="text-muted"> Uba19p0088</td>
                        </tr>
                    </b-col>
                </b-row> 
                <b-row col="12" class="mb-3" >
                    <b-col lg="4">
                        <tr>
                            <th class="text-muted">Gender : </th>
                            <td class="text-muted"> Female</td>
                        </tr>
                    </b-col>
                    <b-col lg="4">
                        <tr>
                            <th class="text-muted">DOB : </th>
                            <td class="text-muted"> 25/03/2001</td>
                        </tr>
                    </b-col>
                    <b-col lg="4">
                        <tr>
                            <th class="text-muted">Place of Birth : </th>
                            <td class="text-muted"> Mankon Bamenda</td>
                        </tr>
                    </b-col>
                </b-row>
                <b-row col="12" class="mb-3" >
                    <b-col lg="4">
                        <tr>
                            <th class="text-muted">Region of Origin: </th>
                            <td class="text-muted"> Mezam</td>
                        </tr>
                    </b-col>
                    <b-col lg="4">
                        <tr>
                            <th class="text-muted">Marital Status : </th>
                            <td class="text-muted"> Single</td>
                        </tr>
                    </b-col>
                    <b-col lg="4">
                        <tr>
                            <th class="text-muted">NID/Passport N<sup>O</sup> : </th>
                            <td class="text-muted"> 0000</td>
                        </tr>
                    </b-col>
                </b-row>
                <b-row col="12" class="mb-3" >
                    <b-col lg="4">
                        <tr>
                            <th class="text-muted">Nationality: </th>
                            <td class="text-muted"> French</td>
                        </tr>
                    </b-col>
                    <b-col lg="4">
                        <tr>
                            <td class="text-muted">Admission Date : </td>
                            <td class="text-muted"> 10/03/2019</td>
                        </tr>
                    </b-col>
                </b-row>
            </b-card-body>
            </b-card>
            <b-card  no-body>

            <b-card-header class="p-3 mb-4 card-title">
                <h5 class=""> Contact</h5>
            </b-card-header>
            <b-card-body>
                <b-row col="12" class="mb-3" >
                    <b-col lg="4">
                        <tr>
                            <th class="text-muted">Email: </th>
                            <td class="text-muted">laurastarr@gmail.com</td>
                        </tr>
                    </b-col>
                    <b-col lg="4">
                        <tr>
                            <th class="text-muted">Phone: </th>
                            <td class="text-muted">+237672293791</td>
                        </tr>
                    </b-col>
                    <b-col lg="4">
                        <tr>
                            <th class="text-muted">Address: </th>
                            <td class="text-muted">Ngomgham/Ngomgham</td>
                        </tr>
                    </b-col>
                </b-row>
            </b-card-body>
            </b-card>
        </b-col>
    </b-row>
  <!-- </Layout> -->
</template>
