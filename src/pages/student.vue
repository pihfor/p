<script>
import Layout from "../layouts/main.vue";
import appConfig from "../../app.config";
export default {
  page: {
    title: "Student",
    meta: [{ name: "description", content: appConfig.description }],
  },
  data() {
    return {
    };
  },
  components: {
    Layout,
  },
};
</script>
<template>
    <Layout>

        <!-- <b-container>
            <ul class="navbar-nav h-100" id="navbar-nav">
              <li class="menu-title">
                <span data-key="t-menu"> {{ $t("t-menu") }}</span>
              </li>

              <b-row>

                <b-link :to="`/`"  class=" "
                    :class="['tab-button']"
                >
                <i class="ri-home-line"></i>
                  Home
                </b-link>

                <b-link :class="['tab-button']" to="/fee" class="mx-3 my-5 py-5">
                  <i class=" bx bx-money"></i>
                  Fee
                </b-link>

                <b-link :to="`/`"  class="mx-3 my-5 py-5 "
                    :class="['tab-button']"
                >
                <i class="ri-home-line"></i>
                  Home
                </b-link> -->


                <!-- <b-link  to="/" class="nav-link custom-abc"  
                    :class="['tab-button']">
                  <i class="ri-home-line"></i>
                  Home
                </b-link>
              </b-row>
              <li class="nav-item">
                <b-link class="nav-link menu-link" href="#Courses" data-bs-toggle="collapse" role="button"
                  aria-expanded="false" aria-controls="Courses">
                  <i class="bx bx-book"></i>
                  <span>Courses</span>
                </b-link>
                <div class="collapse menu-dropdown" id="Courses">
                  <ul class="nav nav-sm flex-column">
                    <li class="nav-item">
                      <b-link 
                    :class="['tab-button']" to="/courses" class="nav-link custom-abc">
                        Courses
                      </b-link>
                    </li>
                    <li class="nav-item">
                      <b-link 
                    :class="['tab-button']" to="/courseRegistration" class="nav-link custom-abc">
                        Course Registration
                      </b-link>
                    </li>
                    <li class="nav-item">
                      <b-link 
                    :class="['tab-button']" to="/formb" class="nav-link">
                        Form B
                      </b-link>
                    </li>
                    <li class="nav-item">
                      <b-link 
                    :class="['tab-button']" to="/sampleformb" class="nav-link">
                        Sample Form B
                      </b-link>
                    </li>
                  </ul>
                </div>
              </li>
              end Courses
              <li class="nav-item">
                <b-link 
                    :class="['tab-button']" class="nav-link menu-link" href="#Results" data-bs-toggle="collapse" role="button"
                  aria-expanded="false" aria-controls="Results">
                  <i class="bx bxs-file"></i>
                  <span> Results</span>
                </b-link>
                <div class="collapse menu-dropdown" id="Results">
                  <ul class="nav nav-sm flex-column">
                    <li class="nav-item">
                      <b-link 
                    :class="['tab-button']" to="/results" class="nav-link">
                        Results
                      </b-link>
                    </li>
                    <li class="nav-item">
                      <b-link 
                    :class="['tab-button']" to="/transcript" class="nav-link">
                        draft Transcript
                      </b-link>
                    </li>
                    <li class="nav-item">
                      <b-link 
                    :class="['tab-button']" to="/application" class="nav-link">
                        Transcript Application
                      </b-link>
                    </li>
                  </ul>
                </div>
              </li>
              <li class="nav-item">
                <b-link 
                    :class="['tab-button']" to="/complains" class="nav-link custom-abc">
                  <i class=" bx bx-file"></i>
                  Complains
                </b-link>
              </li>
              <li class="nav-item">
                <b-link 
                    :class="['tab-button']" to="#" class="nav-link custom-abc">
                  <i class=" bx bx-calendar"></i>
                  Time Table
                </b-link>
              </li>
              <li class="nav-item">
                <b-link 
                    :class="['tab-button']" to="/fee" class="nav-link custom-abc">
                  <i class=" bx bx-money"></i>
                  Fee
                </b-link>
              </li>
            </ul>
          </b-container>-->
        <div id="layout-wrapper" >
           <b-row>
            
            <b-row>
              <router-view></router-view>
              </b-row>
            </b-row>  
        </div> 
    </Layout>
</template>