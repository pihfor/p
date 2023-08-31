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
  components: {
    // Layout,
  },
};
</script>

<template>
  <div>
    <b-card>
      <b-card-header>
        <div class="d-md-flex align-items-center">
        <h5 class="card-title mb-md-0 flex-grow-1">COURSE REGISTRATION</h5>
        </div>
      </b-card-header>
    </b-card>

    <b-row>
      <b-col lg="12" >
        <div>
          <b-card class="mt-3">
            <b-card-body>
                <div class="p-3 W-100 bg-info text-light text-md-center">Course Registration closes on Sat 12/12/2023 11:59PM</div>
            </b-card-body>
            <b-card-body class="borderless">
              <ul class="nav nav-tabs nav-tabs-custom nav-success" role="tablist">
                <li class="nav-item">
                  <b-link class="nav-link fs-14 active" data-bs-toggle="tab" href="#register" role="tab">
                    <i class="ri-list-unordered d-inline-block d-md-none"></i>
                    <span class="d-none d-md-inline-block">Register Courses</span>
                  </b-link>
                </li>
                <li class="nav-item">
                  <b-link class="nav-link fs-14" data-bs-toggle="tab" href="#finalcourses" role="tab">
                    <i class="ri-folder-4-line d-inline-block d-md-none"></i>
                    <span class="d-none d-md-inline-block">Final Courses</span>
                  </b-link>
                </li>
              </ul>
            </b-card-body> 

            <div class="tab-content text-muted">
              <div class="tab-pane active" id="register" role="tabpanel">
                <b-row>
                  <b-col xxl="12">
                    <b-card no-body>
                      <b-card-body class="border border-end-0 border-start-0">
                          <form action="#" method="post">
                              <div class="row align-items-end">
                                  <div class="col-12 col-md-2">
                                      <div class="mb-3">
                                          <select class="form-select" name="school" id="school">
                                              <option selected>Select School</option>
                                              <option value="">School of  Business</option>
                                              <option value="">School of Engineering</option>
                                              <option value="">School of Law</option>
                                          </select>
                                      </div>
                                  </div>                 
                                  <div class="col-12 col-md-2">
                                      <div class="mb-3">
                                          <select class="form-select" name="department" id="department">
                                              <option selected>Select Department</option>
                                              <option value="">CEN</option>
                                              <option value="">FST</option>
                                              <option value="">ABT</option>
                                              <option value="">CPT</option>
                                              <option value="">NFBT</option>
                                              <option value="">EEE</option>
                                              <option value="">CE</option>
                                              <option value="">ABT</option>
                                          </select>
                                      </div>
                                  </div>
                                  <div class="col-12 col-md-2">
                                      <div class="mb-3">
                                          <select class="form-select" name="semester" id="semester">
                                              <option selected>Select Semester</option>
                                              <option value="">First</option>
                                              <option value="">Second</option>
                                              <option value="">Resit</option>
                                          </select>
                                      </div>
                                  </div>    
                                  <div class="col-12 col-md-2">
                                      <div class="mb-3">
                                          <select class="form-select" name="type" id="type">
                                              <option selected>Select Course Type</option>
                                              <option value="">Elective</option>
                                              <option value="">Required</option>
                                              <option value="">Major</option>
                                              <option value="">Minor</option>
                                          </select>
                                      </div> 
                                  </div>

                                  <div class="col-12 col-md-4 text-md-end">
                                      <div class="mb-3">
                                          <button type="submit" class="btn btn-primary">Get Courses</button>
                                      </div> 
                                  </div>  
                              </div>
                          </form>
                      </b-card-body>
                      <b-card-body>
                        <div class="table-responsive">
                          <table class="table table-borderless mb-0 w-100">
                            <tbody>
                              <tr class="bg-light text-muted">
                                <th scope="col">S/n</th>
                                <th scope="col">Course Type</th>
                                <th scope="col">Course Title</th>
                                <th scope="col">Course code</th>
                                <th scope="col">lecturer</th>
                                <th scope="col">Action</th>
                              </tr>
                              <tr class="border">
                                <td>1</td>
                                <td>Major</td>
                                <td>computer graphics</td>
                                <td>cenp909</td>
                                <td>Mr Fusong Victor</td>
                                <td>
                                  <b-button variant="success">
                                    Add
                                  </b-button>
                                </td>
                              </tr>
                              <tr class="border">
                                <td>2</td>
                                <td>Major</td>
                                <td>computer graphics</td>
                                <td>cenp909</td>
                                <td>Mr Fusong Victor</td>
                                <td>
                                  <b-button variant="success">
                                    Add
                                  </b-button>
                                </td>
                              </tr>
                              <tr class="border">
                                <td>3</td>
                                <td>Major</td>
                                <td>computer graphics</td>
                                <td>cenp909</td>
                                <td>Mr Fusong Victor</td>
                                <td>
                                  <b-button variant="success">
                                    Add
                                  </b-button>
                                </td>
                              </tr>
                              <tr class="border">
                                <td>4</td>
                                <td>Major</td>
                                <td>computer graphics</td>
                                <td>cenp909</td>
                                <td>Mr Fusong Victor</td>
                                <td>
                                  <b-button variant="success">
                                    Add
                                  </b-button>
                                </td>
                              </tr>
                              <tr class="border">
                                <td>5</td>
                                <td>Major</td>
                                <td>computer graphics</td>
                                <td>cenp909</td>
                                <td>Mr Fusong Victor</td>
                                <td>
                                  <b-button variant="success">
                                    Add
                                  </b-button>
                                </td>
                              </tr>
                              <tr class="border">
                                <td>6</td>
                                <td>Major</td>
                                <td>computer graphics</td>
                                <td>cenp909</td>
                                <td>Mr Fusong Victor</td>
                                <td>
                                  <b-button variant="success">
                                    Add
                                  </b-button>
                                </td>
                              </tr>
                            </tbody>
                          </table>
                        </div>
                      </b-card-body>
                    </b-card>
                  </b-col>
                </b-row>
              </div>
            </div>

            <div class="tab-content text-muted">
              <div class="tab-pane" id="finalcourses" role="tabpanel">
                  <b-row>
                  <b-col xxl="12">
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
                                <td>
                                  <b-button variant="danger">
                                    Drop
                                  </b-button>
                                </td>
                              </tr>
                              <tr class="border">
                                <td>2</td>
                                <td>computer graphics</td>
                                <td>cenp909</td>
                                <td>Mr Fusong Victor</td>
                                <td>
                                  <b-button variant="danger">
                                    Drop
                                  </b-button>
                                </td>
                              </tr>
                              <tr class="border">
                                <td>3</td>
                                <td>computer graphics</td>
                                <td>cenp909</td>
                                <td>Mr Fusong Victor</td>
                                <td>
                                  <b-button variant="danger">
                                    Drop
                                  </b-button>
                                </td>
                              </tr>
                            </tbody>
                          </table>
                        </div>
                      </b-card-body>
                    </b-card>
                  </b-col>
                </b-row>
              </div>
            </div>
          </b-card>
        </div>
      </b-col>
    </b-row>
  </div>
</template>
