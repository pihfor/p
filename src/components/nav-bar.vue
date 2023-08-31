<!-- <script>
import {
  SimpleBar
} from "simplebar-vue3";

import i18n from "../i18n";

/**
 * Nav-bar Component
 */
export default {
  data() {
    return {
      languages: [{
        flag: require("@/assets/images/flags/us.svg"),
        language: "en",
        title: "English",
      },
      {
        flag: require("@/assets/images/flags/spain.svg"),
        language: "sp",
        title: "Española",
      },
      {
        flag: require("@/assets/images/flags/germany.svg"),
        language: "gr",
        title: "Deutsche",
      },
      {
        flag: require("@/assets/images/flags/italy.svg"),
        language: "it",
        title: "italiana",
      },
      {
        flag: require("@/assets/images/flags/russia.svg"),
        language: "ru",
        title: "русский",
      },
      {
        flag: require("@/assets/images/flags/china.svg"),
        language: "ch",
        title: "中國人",
      },
      {
        flag: require("@/assets/images/flags/french.svg"),
        language: "fr",
        title: "Français",
      },
      {
        flag: require("@/assets/images/flags/ae.svg"),
        language: "ar",
        title: "Arabic",
      },
      ],
      lan: i18n.locale,
      text: null,
      flag: null,
      value: null,
      myVar: 1,
    };
  },
  components: {
    SimpleBar
  },

  methods: {

    // isCustomDropdown() {
    //   //Search bar
    //   var searchOptions = document.getElementById("search-close-options");
    //   var dropdown = document.getElementById("search-dropdown");
    //   var searchInput = document.getElementById("search-options");

    //   searchInput.addEventListener("focus", () => {
    //     var inputLength = searchInput.value.length;
    //     if (inputLength > 0) {
    //       dropdown.classList.add("show");
    //       searchOptions.classList.remove("d-none");
    //     } else {
    //       dropdown.classList.remove("show");
    //       searchOptions.classList.add("d-none");
    //     }
    //   });

    //   searchInput.addEventListener("keyup", () => {
    //     var inputLength = searchInput.value.length;
    //     if (inputLength > 0) {
    //       dropdown.classList.add("show");
    //       searchOptions.classList.remove("d-none");
    //     } else {
    //       dropdown.classList.remove("show");
    //       searchOptions.classList.add("d-none");
    //     }
    //   });

    //   searchOptions.addEventListener("click", () => {
    //     searchInput.value = "";
    //     dropdown.classList.remove("show");
    //     searchOptions.classList.add("d-none");
    //   });

    //   document.body.addEventListener("click", (e) => {
    //     if (e.target.getAttribute("id") !== "search-options") {
    //       dropdown.classList.remove("show");
    //       searchOptions.classList.add("d-none");
    //     }
    //   });
    // },
    // toggleHamburgerMenu() {
    //   var windowSize = document.documentElement.clientWidth;

    //   if (windowSize > 767)
    //     document.querySelector(".hamburger-icon").classList.toggle("open");

    //   //For collapse horizontal menu
    //   if (
    //     document.documentElement.getAttribute("data-layout") === "horizontal"
    //   ) {
    //     document.body.classList.contains("menu") ?
    //       document.body.classList.remove("menu") :
    //       document.body.classList.add("menu");
    //   }

    //   //For collapse vertical menu
    //   if (document.documentElement.getAttribute("data-layout") === "vertical") {
    //     if (windowSize < 1025 && windowSize > 767) {
    //       document.body.classList.remove("vertical-sidebar-enable");
    //       document.documentElement.getAttribute("data-sidebar-size") == "sm" ?
    //         document.documentElement.setAttribute("data-sidebar-size", "") :
    //         document.documentElement.setAttribute("data-sidebar-size", "sm");
    //     } else if (windowSize > 1025) {
    //       document.body.classList.remove("vertical-sidebar-enable");
    //       document.documentElement.getAttribute("data-sidebar-size") == "lg" ?
    //         document.documentElement.setAttribute("data-sidebar-size", "sm") :
    //         document.documentElement.setAttribute("data-sidebar-size", "lg");
    //     } else if (windowSize <= 767) {
    //       document.body.classList.add("vertical-sidebar-enable");
    //       document.documentElement.setAttribute("data-sidebar-size", "lg");
    //     }
    //   }

    //   //Two column menu
    //   if (document.documentElement.getAttribute("data-layout") == "twocolumn") {
    //     document.body.classList.contains("twocolumn-panel") ?
    //       document.body.classList.remove("twocolumn-panel") :
    //       document.body.classList.add("twocolumn-panel");
    //   }
    // },
    // toggleMenu() {
    //   this.$parent.toggleMenu();
    // },
    // toggleRightSidebar() {
    //   this.$parent.toggleRightSidebar();
    // },
    initFullScreen() {
      document.body.classList.toggle("fullscreen-enable");
      if (
        !document.fullscreenElement &&
        /* alternative standard method */
        !document.mozFullScreenElement &&
        !document.webkitFullscreenElement
      ) {
        // current working methods
        if (document.documentElement.requestFullscreen) {
          document.documentElement.requestFullscreen();
        } else if (document.documentElement.mozRequestFullScreen) {
          document.documentElement.mozRequestFullScreen();
        } else if (document.documentElement.webkitRequestFullscreen) {
          document.documentElement.webkitRequestFullscreen(
            Element.ALLOW_KEYBOARD_INPUT
          );
        }
      } else {
        if (document.cancelFullScreen) {
          document.cancelFullScreen();
        } else if (document.mozCancelFullScreen) {
          document.mozCancelFullScreen();
        } else if (document.webkitCancelFullScreen) {
          document.webkitCancelFullScreen();
        }
      }
    },
    setLanguage(locale, country, flag) {
      this.lan = locale;
      this.text = country;
      this.flag = flag;
      document.getElementById("header-lang-img").setAttribute("src", flag);
      i18n.global.locale = locale;
    },
    toggleDarkMode() {
      if (document.documentElement.getAttribute("data-layout-mode") == "dark") {
        document.documentElement.setAttribute("data-layout-mode", "light");
      } else {
        document.documentElement.setAttribute("data-layout-mode", "dark");
      }
    },
    initTopbarComponents() {
      function updateCartPrice() {
        var currencySign = "$";
        var subtotal = 0;
        Array.from(document.getElementsByClassName("cart-item-price")).forEach(function (e) {
          subtotal += parseFloat(e.innerHTML);
        });
        if (document.getElementById("cart-item-total")) {
          document.getElementById("cart-item-total").innerHTML = currencySign + subtotal.toFixed(2);
        }
      }
      if (document.getElementsByClassName("dropdown-item-cart")) {
        var dropdownItemCart = document.querySelectorAll(".dropdown-item-cart").length;
        Array.from(document.querySelectorAll("#page-topbar .dropdown-menu-cart .remove-item-btn")).forEach(function (item) {
          item.addEventListener("click", function () {
            dropdownItemCart--;
            this.closest(".dropdown-item-cart").remove();
            Array.from(document.getElementsByClassName("cartitem-badge")).forEach(function (e) {
              e.innerHTML = dropdownItemCart;
            });
            updateCartPrice();
            if (document.getElementById("empty-cart")) {
              document.getElementById("empty-cart").style.display = dropdownItemCart == 0 ? "block" : "none";
            }
            if (document.getElementById("checkout-elem")) {
              document.getElementById("checkout-elem").style.display = dropdownItemCart == 0 ? "none" : "block";
            }
          });
        });
        Array.from(document.getElementsByClassName("cartitem-badge")).forEach(function (e) {
          e.innerHTML = dropdownItemCart;
        });
        if (document.getElementById("empty-cart")) {
          document.getElementById("empty-cart").style.display = "none";
        }
        if (document.getElementById("checkout-elem")) {
          document.getElementById("checkout-elem").style.display = "block";
        }
        updateCartPrice();
      }

      // notification messages
      if (document.getElementsByClassName("notification-check")) {
        Array.from(document.querySelectorAll(".notification-check input")).forEach(function (element) {
          element.addEventListener("click", function (el) {
            el.target.closest(".notification-item").classList.toggle("active");
          });
        });
      }
    }
  },
  computed: {},
  mounted() {
    document.addEventListener("scroll", function () {
      var pageTopbar = document.getElementById("page-topbar");
      if (pageTopbar) {
        document.body.scrollTop >= 50 || document.documentElement.scrollTop >= 50 ? pageTopbar.classList.add(
          "topbar-shadow") : pageTopbar.classList.remove("topbar-shadow");
      }
    });
    if (document.getElementById("topnav-hamburger-icon"))
      document
        .getElementById("topnav-hamburger-icon")
        .addEventListener("click", this.toggleHamburgerMenu);

    this.isCustomDropdown();
    this.initTopbarComponents();
  },
};
</script> -->
<script>
import {
  SimpleBar
} from "simplebar-vue3";

import i18n from "../i18n";
import UserService from "../helpers/authservice/user.service";

/**
 * Nav-bar Component
 */
export default {
  data() {
    return {
      languages: [{
        flag: require("@/assets/images/flags/us.svg"),
        language: "en",
        title: "English",
      },
      // {
      //   flag: require("@/assets/images/flags/spain.svg"),
      //   language: "sp",
      //   title: "Española",
      // },
      // {
      //   flag: require("@/assets/images/flags/germany.svg"),
      //   language: "gr",
      //   title: "Deutsche",
      // },
      // {
      //   flag: require("@/assets/images/flags/italy.svg"),
      //   language: "it",
      //   title: "italiana",
      // },
      // {
      //   flag: require("@/assets/images/flags/russia.svg"),
      //   language: "ru",
      //   title: "русский",
      // },
      // {
      //   flag: require("@/assets/images/flags/china.svg"),
      //   language: "ch",
      //   title: "中國人",
      // },
      {
        flag: require("@/assets/images/flags/french.svg"),
        language: "fr",
        title: "Français",
      },
      // {
      //   flag: require("@/assets/images/flags/ae.svg"),
      //   language: "ar",
      //   title: "Arabic",
      // },
      ],
      lan: i18n.locale,
      text: null,
      flag: null,
      value: null,
      myVar: 1,
    };
  },
  components: {
    SimpleBar
  },

  methods: {

    handleLogout(){
      UserService.logout().then(
        () => {
          this.$router.push({
            path:'/login'
          })
        }
      ).catch(error =>{
        console.log(error);
      })
    },

    // isCustomDropdown() {
    //   //Search bar
    //   var searchOptions = document.getElementById("search-close-options");
    //   var dropdown = document.getElementById("search-dropdown");
    //   var searchInput = document.getElementById("search-options");

    //   searchInput.addEventListener("focus", () => {
    //     var inputLength = searchInput.value.length;
    //     if (inputLength > 0) {
    //       dropdown.classList.add("show");
    //       searchOptions.classList.remove("d-none");
    //     } else {
    //       dropdown.classList.remove("show");
    //       searchOptions.classList.add("d-none");
    //     }
    //   });

    //   searchInput.addEventListener("keyup", () => {
    //     var inputLength = searchInput.value.length;
    //     if (inputLength > 0) {
    //       dropdown.classList.add("show");
    //       searchOptions.classList.remove("d-none");
    //     } else {
    //       dropdown.classList.remove("show");
    //       searchOptions.classList.add("d-none");
    //     }
    //   });

    //   searchOptions.addEventListener("click", () => {
    //     searchInput.value = "";
    //     dropdown.classList.remove("show");
    //     searchOptions.classList.add("d-none");
    //   });

    //   document.body.addEventListener("click", (e) => {
    //     if (e.target.getAttribute("id") !== "search-options") {
    //       dropdown.classList.remove("show");
    //       searchOptions.classList.add("d-none");
    //     }
    //   });
    // },
    toggleHamburgerMenu() {
      var windowSize = document.documentElement.clientWidth;

      if (windowSize > 767)
        document.querySelector(".hamburger-icon").classList.toggle("open");

      //For collapse horizontal menu
      if (
        document.documentElement.getAttribute("data-layout") === "horizontal"
      ) {
        document.body.classList.contains("menu") ?
          document.body.classList.remove("menu") :
          document.body.classList.add("menu");
      }

      //For collapse vertical menu
      if (document.documentElement.getAttribute("data-layout") === "vertical") {
        if (windowSize < 1025 && windowSize > 767) {
          document.body.classList.remove("vertical-sidebar-enable");
          document.documentElement.getAttribute("data-sidebar-size") == "sm" ?
            document.documentElement.setAttribute("data-sidebar-size", "") :
            document.documentElement.setAttribute("data-sidebar-size", "sm");
        } else if (windowSize > 1025) {
          document.body.classList.remove("vertical-sidebar-enable");
          document.documentElement.getAttribute("data-sidebar-size") == "lg" ?
            document.documentElement.setAttribute("data-sidebar-size", "sm") :
            document.documentElement.setAttribute("data-sidebar-size", "lg");
        } else if (windowSize <= 767) {
          document.body.classList.add("vertical-sidebar-enable");
          document.documentElement.setAttribute("data-sidebar-size", "lg");
        }
      }

      //Two column menu
      if (document.documentElement.getAttribute("data-layout") == "twocolumn") {
        document.body.classList.contains("twocolumn-panel") ?
          document.body.classList.remove("twocolumn-panel") :
          document.body.classList.add("twocolumn-panel");
      }
    },
    toggleMenu() {
      this.$parent.toggleMenu();
    },
    toggleRightSidebar() {
      this.$parent.toggleRightSidebar();
    },
    initFullScreen() {
      document.body.classList.toggle("fullscreen-enable");
      if (
        !document.fullscreenElement &&
        /* alternative standard method */
        !document.mozFullScreenElement &&
        !document.webkitFullscreenElement
      ) {
        // current working methods
        if (document.documentElement.requestFullscreen) {
          document.documentElement.requestFullscreen();
        } else if (document.documentElement.mozRequestFullScreen) {
          document.documentElement.mozRequestFullScreen();
        } else if (document.documentElement.webkitRequestFullscreen) {
          document.documentElement.webkitRequestFullscreen(
            Element.ALLOW_KEYBOARD_INPUT
          );
        }
      } else {
        if (document.cancelFullScreen) {
          document.cancelFullScreen();
        } else if (document.mozCancelFullScreen) {
          document.mozCancelFullScreen();
        } else if (document.webkitCancelFullScreen) {
          document.webkitCancelFullScreen();
        }
      }
    },
    setLanguage(locale, country, flag) {
      this.lan = locale;
      this.text = country;
      this.flag = flag;
      document.getElementById("header-lang-img").setAttribute("src", flag);
      i18n.global.locale = locale;
    },
    toggleDarkMode() {
      if (document.documentElement.getAttribute("data-layout-mode") == "dark") {
        document.documentElement.setAttribute("data-layout-mode", "light");
      } else {
        document.documentElement.setAttribute("data-layout-mode", "dark");
      }
    },
    initTopbarComponents() {
      function updateCartPrice() {
        var currencySign = "$";
        var subtotal = 0;
        Array.from(document.getElementsByClassName("cart-item-price")).forEach(function (e) {
          subtotal += parseFloat(e.innerHTML);
        });
        if (document.getElementById("cart-item-total")) {
          document.getElementById("cart-item-total").innerHTML = currencySign + subtotal.toFixed(2);
        }
      }
      if (document.getElementsByClassName("dropdown-item-cart")) {
        var dropdownItemCart = document.querySelectorAll(".dropdown-item-cart").length;
        Array.from(document.querySelectorAll("#page-topbar .dropdown-menu-cart .remove-item-btn")).forEach(function (item) {
          item.addEventListener("click", function () {
            dropdownItemCart--;
            this.closest(".dropdown-item-cart").remove();
            Array.from(document.getElementsByClassName("cartitem-badge")).forEach(function (e) {
              e.innerHTML = dropdownItemCart;
            });
            updateCartPrice();
            if (document.getElementById("empty-cart")) {
              document.getElementById("empty-cart").style.display = dropdownItemCart == 0 ? "block" : "none";
            }
            if (document.getElementById("checkout-elem")) {
              document.getElementById("checkout-elem").style.display = dropdownItemCart == 0 ? "none" : "block";
            }
          });
        });
        Array.from(document.getElementsByClassName("cartitem-badge")).forEach(function (e) {
          e.innerHTML = dropdownItemCart;
        });
        if (document.getElementById("empty-cart")) {
          document.getElementById("empty-cart").style.display = "none";
        }
        if (document.getElementById("checkout-elem")) {
          document.getElementById("checkout-elem").style.display = "block";
        }
        updateCartPrice();
      }

      // notification messages
      if (document.getElementsByClassName("notification-check")) {
        Array.from(document.querySelectorAll(".notification-check input")).forEach(function (element) {
          element.addEventListener("click", function (el) {
            el.target.closest(".notification-item").classList.toggle("active");
          });
        });
      }
    }
  },
  computed: {},
  mounted() {
    document.addEventListener("scroll", function () {
      var pageTopbar = document.getElementById("page-topbar");
      if (pageTopbar) {
        document.body.scrollTop >= 50 || document.documentElement.scrollTop >= 50 ? pageTopbar.classList.add(
          "topbar-shadow") : pageTopbar.classList.remove("topbar-shadow");
      }
    });
    if (document.getElementById("topnav-hamburger-icon"))
      document
        .getElementById("topnav-hamburger-icon")
        .addEventListener("click", this.toggleHamburgerMenu);

    // this.isCustomDropdown();
    // t,
    // his.initTopbarComponents();
  },
};
</script>
<template>
  <header id="page-topbar"  class="bg-primary">
    <div class="layout-width">
      <div class="navbar-header">
        <div class="d-flex">
          <!-- LOGO -->
          <div class="navbar-brand-box horizontal-logo">
            <router-link to="/" class="logo logo-dark">
              <span class="logo-sm">
                <img src="@/assets/images/logo-sm.png" alt="" height="22" />
              </span>
              <span class="logo-lg">
                <img src="@/assets/images/logo-dark.png" alt="" height="17" />
              </span>
            </router-link>

            <router-link to="/" class="logo logo-light">
              <span class="logo-sm">
                <img src="@/assets/images/logo-sm.png" alt="" height="30" />
              </span>
              <span class="logo-lg">
                <img src="@/assets/images/logo-light.png" alt="" height="80" />
              </span>
            </router-link>
          </div>

          <button type="button" class="
              btn btn-sm
              px-3
              fs-16
              header-item
              vertical-menu-btn
              topnav-hamburger
            " id="topnav-hamburger-icon">
            <span class="hamburger-icon">
              <span></span>
              <span></span>
              <span></span>
            </span>
          </button>

          <!-- App Search-->
        </div>

        <div class="d-flex align-items-center">
          <div class="dropdown d-md-none topbar-head-dropdown header-item">
            <button type="button" class="btn btn-icon btn-topbar btn-ghost-secondary rounded-circle"
              id="page-header-search-dropdown" data-bs-toggle="dropdown" aria-haspopup="true" aria-expanded="false">
              <i class="bx bx-search fs-22"></i>
            </button>
            <div class="dropdown-menu dropdown-menu-lg dropdown-menu-end p-0"
              aria-labelledby="page-header-search-dropdown">
              <form class="p-3">
                <div class="form-group m-0">
                  <div class="input-group">
                    <input type="text" class="form-control" placeholder="Search ..."
                      aria-label="Recipient's username" />
                    <b-button variant="primary" type="submit">
                      <i class="mdi mdi-magnify"></i>
                    </b-button>
                  </div>
                </div>
              </form>
            </div>
          </div>
          <div class="ms-1 header-item d-none d-sm-flex">
            <b-button type="button" variant="ghost-secondary" class="btn-icon btn-topbar rounded-circle"
              data-toggle="fullscreen" @click="initFullScreen">
              <i class="bx bx-fullscreen fs-22"></i>
            </b-button>
          </div>
          <div class="dropdown topbar-head-dropdown ms-1 header-item">
            <button type="button" class="btn btn-icon btn-topbar btn-ghost-secondary rounded-circle"
              id="page-header-notifications-dropdown" data-bs-toggle="dropdown" aria-haspopup="true"
              aria-expanded="false">
              <i class="bx bx-bell fs-22"></i>
              <span class="position-absolute topbar-badge fs-10 translate-middle badge rounded-pill bg-danger">
                3<span class="visually-hidden">unread messages</span></span>
            </button>
            <div class="dropdown-menu dropdown-menu-lg dropdown-menu-end p-0"
              aria-labelledby="page-header-notifications-dropdown">
              <div class="dropdown-head bg-primary bg-pattern rounded-top">
                <div class="p-3">
                  <b-row class="align-items-center">
                    <b-col>
                      <h6 class="m-0 fs-16 fw-semibold text-white">
                        Notifications
                      </h6>
                    </b-col>
                    <b-col cols="auto" class="dropdown-tabs">
                      <b-badge variant="soft-light" class="badge-soft-light fs-13"> 7 New</b-badge>
                    </b-col>
                  </b-row>
                </div>

                <div class="px-2 pt-2">
                  <ul class="nav nav-tabs dropdown-tabs nav-tabs-custom" data-dropdown-tabs="true"
                    id="notificationItemsTab" role="tablist">
                    <li class="nav-item">
                      <b-link class="nav-link active" data-bs-toggle="tab" href="#all-noti-tab" role="tab"
                        aria-selected="false" @click.capture.stop>
                        All (4)
                      </b-link>
                    </li>
                  </ul>
                </div>
              </div>

              <div class="tab-content" id="notificationItemsTabContent">

                <div class="tab-pane fade py-2 ps-2 show active" id="all-noti-tab" role="tabpanel">
                  <SimpleBar data-simplebar style="max-height: 300px" class="pe-2">
                    <div class="text-reset notification-item d-block dropdown-item position-relative">
                      <div class="d-flex">
                        <div class="avatar-xs me-3">
                          <span class="avatar-title bg-soft-info text-info rounded-circle fs-16">
                            <i class="bx bx-badge-check"></i>
                          </span>
                        </div>
                        <div class="flex-1">
                          <b-link href="#!" class="stretched-link">
                            <h6 class="mt-0 mb-2 lh-base">
                              Your <b>Elite</b> author Graphic Optimization
                              <span class="text-secondary">reward</span> is
                              ready!
                            </h6>
                          </b-link>
                          <p class="mb-0 fs-11 fw-medium text-uppercase text-muted">
                            <span><i class="mdi mdi-clock-outline"></i> Just 30 sec ago</span>
                          </p>
                        </div>
                        <div class="px-2 fs-15">
                          <input class="form-check-input" type="checkbox" />
                        </div>
                      </div>
                    </div>

                    <div class="text-reset notification-item d-block dropdown-item position-relative">
                      <div class="d-flex">
                        <img src="@/assets/images/users/avatar-2.jpg" class="me-3 rounded-circle avatar-xs"
                          alt="user-pic" />
                        <div class="flex-1">
                          <b-link href="#!" class="stretched-link">
                            <h6 class="mt-0 mb-1 fs-13 fw-semibold">
                              Angela Bernier
                            </h6>
                          </b-link>
                          <div class="fs-13 text-muted">
                            <p class="mb-1">
                              Answered to your comment on the cash flow forecast's graph 🔔.
                            </p>
                          </div>
                          <p class="mb-0 fs-11 fw-medium text-uppercase text-muted">
                            <span><i class="mdi mdi-clock-outline"></i> 48 min ago</span>
                          </p>
                        </div>
                        <div class="px-2 fs-15">
                          <input class="form-check-input" type="checkbox" />
                        </div>
                      </div>
                    </div>

                    <div class="text-reset notification-item d-block dropdown-item position-relative">
                      <div class="d-flex">
                        <div class="avatar-xs me-3">
                          <span class="avatar-title bg-soft-danger text-danger rounded-circle fs-16">
                            <i class="bx bx-message-square-dots"></i>
                          </span>
                        </div>
                        <div class="flex-1">
                          <b-link href="#!" class="stretched-link">
                            <h6 class="mt-0 mb-2 fs-13 lh-base">
                              You have received <b class="text-success">20</b> new messages in the conversation
                            </h6>
                          </b-link>
                          <p class="mb-0 fs-11 fw-medium text-uppercase text-muted">
                            <span><i class="mdi mdi-clock-outline"></i> 2 hrs
                              ago</span>
                          </p>
                        </div>
                        <div class="px-2 fs-15">
                          <input class="form-check-input" type="checkbox" />
                        </div>
                      </div>
                    </div>

                    <div class="text-reset notification-item d-block dropdown-item position-relative">
                      <div class="d-flex">
                        <img src="@/assets/images/users/avatar-8.jpg" class="me-3 rounded-circle avatar-xs"
                          alt="user-pic" />
                        <div class="flex-1">
                          <b-link href="#!" class="stretched-link">
                            <h6 class="mt-0 mb-1 fs-13 fw-semibold">
                              Maureen Gibson
                            </h6>
                          </b-link>
                          <div class="fs-13 text-muted">
                            <p class="mb-1">
                              We talked about a project on linkedin.
                            </p>
                          </div>
                          <p class="mb-0 fs-11 fw-medium text-uppercase text-muted">
                            <span><i class="mdi mdi-clock-outline"></i> 4 hrs
                              ago</span>
                          </p>
                        </div>
                        <div class="px-2 fs-15">
                          <input class="form-check-input" type="checkbox" />
                        </div>
                      </div>
                    </div>

                    <div class="my-3 text-center">
                      <b-link type="button" variant="soft-success" href="/notifications">
                        View All Notifications
                        <i class="ri-arrow-right-line align-middle"></i>
                      </b-link>
                    </div>
                  </SimpleBar>
                </div>

              </div>
            </div>
          </div>

          <div class="dropdown ms-sm-3 header-item topbar-user">
            <button type="button" class="btn" id="page-header-user-dropdown" data-bs-toggle="dropdown"
              aria-haspopup="true" aria-expanded="false">
              <span class="d-flex align-items-center">
                <img class="rounded-circle header-profile-user" src="@/assets/images/users/avatar-1.jpg"
                  alt="Header Avatar" />
                <span class="text-start ms-xl-2">
                  <span class=" d-none d-xl-inline-block ms-1 fw-medium user-name-text">Ngu Lumfor Laura</span>
                  <span class="d-none d-xl-block ms-1 fs-12 text-muted user-name-sub-text">lv 2</span>
                </span>
              </span>
            </button>
            <div class="dropdown-menu dropdown-menu-end">
              <h6 class="dropdown-header">Welcome Ngu!</h6>
              <router-link class="dropdown-item" to="/"><i
                  class="mdi mdi-account-circle text-muted fs-16 align-middle me-1"></i>
                <span class="align-middle">Profile</span>
              </router-link>
              <b-link class="dropdown-item" href="/logout"><i
                  class="mdi mdi-logout text-muted fs-16 align-middle me-1"></i>
                <span class="align-middle" data-key="t-logout">Logout</span>
              </b-link>
            </div>
          </div>
        </div>
      </div>
    </div>
  </header>
</template>