
<template>
  <div>
    <div id="layout-wrapper">
      <NavBar />
      <!-- ========== App Menu ========== -->
      <div class="app-menu navbar-menu">
        <!-- LOGO -->
        <div class="navbar-brand-box">
          <!-- Dark Logo-->
          <router-link to="/" class="logo logo-dark">
            <span class="logo-sm">
              <img src="@/assets/images/logo-sm.png" alt="" height="22" />
            </span>
            <span class="logo-lg">
              <img src="@/assets/images/logo-dark.png" alt="" height="17" />
            </span>
          </router-link>
          <!-- Light Logo-->
          <router-link to="/" class="logo logo-light">
            <span class="logo-sm">
              <img src="@/assets/images/logo-sm.png" alt="" height="22" />
            </span>
            <span class="logo-lg">
              <img src="@/assets/images/logo-light.png" alt="" height="17" />
            </span>
          </router-link>
          <button type="button" class="
              btn btn-sm
              p-0
              fs-20
              header-item
              float-end
              btn-vertical-sm-hover
            " id="vertical-hover">
            <i class="ri-record-circle-line"></i>
          </button>
        </div>
        <div id="scrollbar">
          <b-container>
            <ul class="navbar-nav h-100" id="navbar-nav">
              <li class="menu-title">
                <span data-key="t-menu"> {{ $t("t-menu") }}</span>
              </li>

              <li class="nav-item">
                <router-link to="/" class="nav-link custom-abc">
                  <i class="ri-home-line"></i>
                  Home
                </router-link>
              </li>
              <li class="nav-item">
                <b-link class="nav-link menu-link" href="#Courses" data-bs-toggle="collapse" role="button"
                  aria-expanded="false" aria-controls="Courses">
                  <i class="bx bx-book"></i>
                  <span>Courses</span>
                </b-link>
                <div class="collapse menu-dropdown" id="Courses">
                  <ul class="nav nav-sm flex-column">
                    <li class="nav-item">
                      <router-link to="/courses" class="nav-link custom-abc">
                        Courses
                      </router-link>
                    </li>
                    <li class="nav-item">
                      <router-link to="/courseRegistration" class="nav-link custom-abc">
                        Course Registration
                      </router-link>
                    </li>
                    <li class="nav-item">
                      <router-link to="/formb" class="nav-link">
                        Form B
                      </router-link>
                    </li>
                    <li class="nav-item">
                      <router-link to="/sampleformb" class="nav-link">
                        Sample Form B
                      </router-link>
                    </li>
                  </ul>
                </div>
              </li>
              <!-- end Courses-->
              <li class="nav-item">
                <b-link class="nav-link menu-link" href="#Results" data-bs-toggle="collapse" role="button"
                  aria-expanded="false" aria-controls="Results">
                  <i class="bx bxs-file"></i>
                  <span> Results</span>
                </b-link>
                <div class="collapse menu-dropdown" id="Results">
                  <ul class="nav nav-sm flex-column">
                    <li class="nav-item">
                      <router-link to="/results" class="nav-link">
                        Results
                      </router-link>
                    </li>
                    <li class="nav-item">
                      <router-link to="/transcript" class="nav-link">
                        draft Transcript
                      </router-link>
                    </li>
                    <li class="nav-item">
                      <router-link to="/application" class="nav-link">
                        Transcript Application
                      </router-link>
                    </li>
                  </ul>
                </div>
              </li>
              <li class="nav-item">
                <router-link to="/complains" class="nav-link custom-abc">
                  <i class=" bx bx-file"></i>
                  Complains
                </router-link>
              </li>
              <li class="nav-item">
                <router-link to="#" class="nav-link custom-abc">
                  <i class=" bx bx-calendar"></i>
                  Time Table
                </router-link>
              </li>
              <li class="nav-item">
                <router-link to="/fee" class="nav-link custom-abc">
                  <i class=" bx bx-money"></i>
                  Fee
                </router-link>
              </li>
            </ul>
          </b-container>
          <!-- Sidebar -->
        </div>
        <!-- Left Sidebar End -->
        <!-- Vertical Overlay-->
        <div class="vertical-overlay"></div>
      </div>
      <!-- ============================================================== -->
      <!-- Start Page Content here -->
      <!-- ============================================================== -->

      <div class="main-content">
        <div class="page-content">
          <!-- Start Content-->
          <b-container fluid>
            <slot />
          </b-container>
        </div>
        <Footer />
      </div>
      <RightBar />
    </div>
  </div>
</template>

<script>
import NavBar from "@/components/nav-bar";
import RightBar from "@/components/right-bar";
import Footer from "@/components/footer";

export default {
  watch: {
    $route: {
      handler: "onRoutechange",
      immediate: true,
      deep: true,
    },
  },
  methods: {
    onRoutechange(ele) {
      this.initActiveMenu(ele.path);
    },
    initActiveMenu(ele) {
      setTimeout(() => {
        if (document.querySelector("#navbar-nav")) {
          let a = document
            .querySelector("#navbar-nav")
            .querySelector('[href="' + ele + '"]');

          if (a) {
            a.classList.add("active");
            let parentCollapseDiv = a.closest(".collapse.menu-dropdown");
            if (parentCollapseDiv) {
              parentCollapseDiv.classList.add("show");
              parentCollapseDiv.parentElement.children[0].classList.add(
                "active"
              );
              parentCollapseDiv.parentElement.children[0].setAttribute(
                "aria-expanded",
                "true"
              );
              if (
                parentCollapseDiv.parentElement.closest(
                  ".collapse.menu-dropdown"
                )
              ) {
                parentCollapseDiv.parentElement
                  .closest(".collapse")
                  .classList.add("show");
                if (
                  parentCollapseDiv.parentElement.closest(".collapse")
                    .previousElementSibling
                )
                  parentCollapseDiv.parentElement
                    .closest(".collapse")
                    .previousElementSibling.classList.add("active");
              }
            }
          }
        }
      }, 1000);
    },
  },
  components: {
    NavBar,
    RightBar,
    Footer
  },
};
</script>
