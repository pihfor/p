<script>
// import Layout from "../../../layouts/main.vue";
// import appConfig from "../../../../app.config";

export default {
  page: {
    title: "Course Registration",
    // meta: [{ name: "description", content: appConfig.description }],
  },
  data() {
    return {
      title: "Course Registration",
      items: [
        {
          text: "",
          href: "/",
        },
        {
          text: "Course Registration",
          active: true,
        },
      ],
      thumbsSwiper: null,
    };
  },
  // components: {
  //   Layout,
  // },
};
</script>

<template>
  <div>
    <b-card no-body>
        <b-card-header class=" d-md-flex border-0">
            <div class="d-md-flex align-items-center">
                <h5 class="card-title mb-3 mb-md-0 flex-grow-1">COURSES</h5>
            </div>
        </b-card-header>
    </b-card>
    <b-card>
      <b-card-header>
        <b-row class="align-items-end">
          <div class="col-12 col-md-2 mb-3">
            <select name="year" id="year" class="form-select">
              <option value="2023/2024">Select year</option>
              <option value="2023/2024">2023/2024</option>
              <option value="2023/2024">2022/2023</option>
              <option value="2023/2024">2021/2022</option>
              <option value="2023/2024">2020/2021</option>
              <option value="2023/2024">2019/2020</option>
              <option value="2023/2024">2018/2019</option>
            </select>
          </div>
          <div class="col-12 col-md-2 mb-3">
            <select name="year" id="year" class="form-select">
              <option value="2023/2024">Select Semester</option>
              <option value="2023/2024">First</option>
              <option value="2023/2024">Second</option>
              <option value="2023/2024">Resit</option>
            </select>
          </div>
          <div class="col-12 col-md-2 mb-3">
            <b-button variant="success">Done</b-button>
          </div>
        </b-row>
      </b-card-header>
      <b-card-body>
        <b-row>
                <b-col xxl="12">
                  <b-card no-body>
                    <b-card-body>
                      <h1 class="card-title p-3 bg-info text-white">My Courses</h1>
                    </b-card-body>
                  </b-card>

                  <b-card no-body>
                    <b-card-body>
                      <div class="table-responsive">
                        <table class="table table-borderless mb-0 w-100">
                          <tbody>
                            <tr class="bg-light text-muted">
                              <th scope="col">S/n</th>
                              <th scope="col">Course Title</th>
                              <th scope="col">Course code</th>
                              <th scope="col">lecturer</th>
                              <th scope="col">Action</th>
                            </tr>
                            <tr class="border">
                              <td>1</td>
                              <td>computer graphics</td>
                              <td>cenp909</td>
                              <td>Mr Fusong Victor</td>
                              <td colspan="2">
                                <b-link href="/single">
                                  <i class="las la-eye text-primary"></i>
                                </b-link>
                              </td>
                            </tr>
                            <tr class="border">
                              <td>2</td>
                              <td>computer graphics</td>
                              <td>cenp909</td>
                              <td>Mr Fusong Victor</td>
                              <td colspan="2">
                                <b-link href="/single" >
                                  <i class="las la-eye text-primary"></i>
                                </b-link>
                              </td>
                            </tr>
                            <tr class="border">
                              <td>3</td>
                              <td>computer graphics</td>
                              <td>cenp909</td>
                              <td>Mr Fusong Victor</td>
                              <td colspan="2">
                                <b-link href="/single">
                                  <i class="las la-eye text-primary"></i>
                                </b-link>
                              </td>
                            </tr>
                          </tbody>
                        </table>
                      </div>
                    </b-card-body>
                  </b-card>
                </b-col>
              </b-row>
      </b-card-body>
    </b-card>
  </div>
</template>