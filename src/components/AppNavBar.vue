<template>
  <nav
    class="row scrolled navbar navbar-expand-md navbar-dark"
    :class="{
      show: isMenuOpen,
      exapanded: isNavbarExpanded,
      scrolled: isScrolled,
    }"
  >
    <a class="col-lg-2 col-sm-4 col-4 logo-nav">
      <img
        src="../images/Logos/slackProLogo.png"
        alt=""
        style="width: 40px; height: 40px"
      />
      <h1>Slack</h1>
    </a>
    <div
      class="col-lg-6 col-md-6 col-sm-6 col-6 collapse navbar-collapse"
      :class="{ show: isMenuOpen }"
    >
      <ul class="navbar-nav">
        <li class="nav-item">
          <a
            class="nav-link"
            href="#"
            ref="dropdownButton"
            @click="toggleFeaturesDropdown"
            :class="{ 'dropdown-button': true, active: showFeaturesDropdown }"
          >
            <p>Features<span class="arrow" v-html="Featuresarrow"></span></p>
          </a>
        </li>
        <transition name="dropdown-slide">
          <div
            v-if="isDropdownOpen"
            class="dropdown-menu"
            @click="closeDropdown"
            ref="dropdownMenu"
          >
            <div class="dropdown-content">
              <div class="row dropdown">
                <!-- First column -->
                <div class="dropdown-list col-lg-3 col-md-4 col-sm-6 col-4">
                  <div class="row link-tab">
                    <a class="dropdown-link" href="">Channels</a>
                    <p class="link-description-text">Focused project spaces</p>
                  </div>
                  <div class="row link-tab">
                    <a class="dropdown-link" href="">Slack Connect</a>
                    <p class="link-description-text">Shared partner channel</p>
                  </div>
                  <div class="row link-tab">
                    <a class="dropdown-link" href="">Messaging</a>
                    <p class="link-description-text">Organise team chat</p>
                  </div>
                  <div class="row link-tab">
                    <a class="dropdown-link" href="">Huddles</a>
                    <p class="link-description-text">Audio and video calls</p>
                  </div>
                  <div class="row link-tab">
                    <a class="dropdown-link" href="">Clips</a>
                    <p class="link-description-text">Record and share info</p>
                  </div>
                </div>

                <!-- Second Column -->
                <div class="dropdown-list col-lg-3 col-md-4 col-sm-6 col-4">
                  <div class="row link-tab">
                    <a class="dropdown-link" href="">Apps and Integerations</a>
                    <p class="link-description-text">
                      connect to other services
                    </p>
                  </div>
                  <div class="row link-tab">
                    <a class="dropdown-link" href="">Workflow Builders</a>
                    <p class="link-description-text">
                      Automate routine actions
                    </p>
                  </div>
                  <div class="row link-tab">
                    <a class="dropdown-link" href="">Search</a>
                    <p class="link-description-text">Access shared knowledge</p>
                  </div>
                  <div class="row link-tab">
                    <a class="dropdown-link" href="">File Sharing</a>
                    <p class="link-description-text">See and share files</p>
                  </div>
                </div>

                <!-- Third column -->
                <div class="dropdown-list col-lg-3 col-md-4 col-sm-6 col-4">
                  <div class="row link-tab">
                    <a class="dropdown-link" href="">Security</a>
                    <p class="link-description-text">Protect company data</p>
                  </div>
                  <div class="row link-tab">
                    <a class="dropdown-link" href=""
                      >Enterprise Key Management</a
                    >
                    <p class="link-description-text">
                      Control visibility and access
                    </p>
                  </div>
                  <div class="row link-tab">
                    <a class="dropdown-link" href="">Slack Atlas</a>
                    <p class="link-description-text">Profile and org charts</p>
                  </div>
                  <div class="row link-tab">
                    <a class="dropdown-link" href="">Canvas</a>
                    <p class="link-description-text">
                      Text docs right in Slack
                    </p>
                  </div>
                </div>

                <!-- Fourth  MAster column -->
                <div
                  class="dropdown-list col-lg-3 col-md-4 col-sm-6 col-4 master-column"
                >
                  <div class="row link-tab">
                    <h6 class="master-heading">Features</h6>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </transition>
        <li class="nav-item">
          <a
            class="nav-link"
            href="#"
            @click="toggleSolutionsDropdown"
            :class="{ 'dropdown-button': true, active: showSolutionsDropdown }"
          >
            <p>Solutions<span class="arrow" v-html="Solutionsarrow"></span></p>
          </a>
        </li>
        <li class="nav-item">
          <a class="nav-link" href="#">
            <p>Enterprise</p>
          </a>
        </li>
        <li class="nav-item">
          <a
            class="nav-link"
            href="#"
            @click="toggleResourcesDropdown"
            :class="{ 'dropdown-button': true, active: showResourcesDropdown }"
          >
            <p>Resources<span class="arrow" v-html="Resourcesarrow"></span></p>
          </a>
        </li>
        <li class="nav-item">
          <a class="nav-link" href="#">
            <p>Pricing</p>
          </a>
        </li>
      </ul>
    </div>
    <div class="col-lg-4 col-md-6 col-sm-6 col-4 navbar-buttons">
      <i class="uil uil-search"></i>
      <a class="navbtn-signin">
        <P>Sign in</P>
      </a>
      <try-sales-buttons-vue class="nav-Buttons"></try-sales-buttons-vue>
    </div>
    <button
      class="navbar-toggler"
      id="tryBtn"
      type="button"
      @click="toggleMenu"
    >
      <i class="uil uil-bars"></i>
    </button>
  </nav>
</template>

<script>
import TrySalesButtonsVue from "./Buttons.vue/TrySalesButtons.vue";
export default {
  name: "AppNavBar",
  components: {
    TrySalesButtonsVue,
  },
  data() {
    return {
      isDropdownOpen: false,
      isMenuOpen: false,
      showDropdown: false,
      isNavbarExpanded: false,
      Featuresarrow: "&#11167;",
      Solutionsarrow: "&#11167;",
      Resourcesarrow: "&#11167;",
      isScrolled: false,
      targetElement: null,
    };
  },
  mounted() {
    window.addEventListener("scroll", this.handleScroll);
    this.targetElement = document.getElementById("mapSection");
  },
  beforeDestroy() {
    window.removeEventListener("scroll", this.handleScroll);
  },
  methods: {
    toggleMenu() {
      this.isMenuOpen = !this.isMenuOpen;
      this.isNavbarExpanded = !this.isNavbarExpanded;
    },
    toggleFeaturesDropdown() {
      this.isDropdownOpen = !this.isDropdownOpen;
      this.showFeaturesDropdown = !this.showFeaturesDropdown;
      this.Featuresarrow = this.showFeaturesDropdown ? "&#11165;" : "&#11167;";
    },
    closeDropdown() {
      this.isDropdownOpen = false;
    },
    toggleSolutionsDropdown() {
      this.showSolutionsDropdown = !this.showSolutionsDropdown;
      this.Solutionsarrow = this.showSolutionsDropdown
        ? "&#11165;"
        : "&#11167;";
    },
    toggleResourcesDropdown() {
      this.showResourcesDropdown = !this.showResourcesDropdown;
      this.Resourcesarrow = this.showResourcesDropdown
        ? "&#11165;"
        : "&#11167;";
    },
    handleScroll() {
      this.isScrolled = window.pageYOffset > 0;
    },
  },
};
</script>

<style scoped>
/* Dropdown styling */
.dropdown-menu {
  position: absolute;
  border-radius: 10px;
  display: inline-block;
  z-index: 1000;
  width: calc(120% + 1vw);
}

.dropdown-content {
  border-radius: 16px;
  display: grid;
  gap: 10px;
  padding: 10px;
  backdrop-filter: blur(10px);
}
.dropdown {
  width: 100%;
  height: 100%;
}
/*
.dropdown-list {
}
*/

.master-column {
  background-color: #f4ede4;
}
.link-tab:hover {
  /*background-color: #fcf7f1;*/
  transform: scaleY(1.06);
  /* border-radius: 6px;
  box-shadow: 0 0 1px 1px rgba(100, 95, 95, 0.7);*/
  transition: all 0.1s;
}
.dropdown-link {
  text-decoration: none;
  font-family: Arial, Helvetica, sans-serif;
}
.dropdown-link:hover {
  color: purple;
}
.link-description-text {
  font-family: Arial, Helvetica, sans-serif;
}

/* Dropdown Menu anmation*/
.dropdown-slide-enter-active {
  animation: slideDown 0.3s;
}

.dropdown-slide-leave-active {
  animation: slideUp 0.3s;
}

@keyframes slideDown {
  0% {
    opacity: 0;
    transform: translateY(-20px);
  }
  100% {
    opacity: 1;
    transform: translateY(0);
  }
}

@keyframes slideUp {
  0% {
    opacity: 1;
    transform: translateY(0);
  }
  100% {
    opacity: 0;
    transform: translateY(-20px);
  }
}

/* Navbar Styling*/
.navbar {
  background-color: purple;
  display: flex;
  align-items: center;
  height: 70px;
}
.scrolled {
  width: 100%;
  margin: 0;
  position: fixed;
  z-index: 1000;
}
.logo-nav {
  cursor: pointer;
  text-decoration: none;
  display: flex;
  align-items: center;
}

.logo-nav h1 {
  font-family: "Segoe UI", Tahoma, Geneva, Verdana, sans-serif;
  font-weight: bold;
  color: #f4ede4;
  margin-left: 5px;
}

.navbar-nav {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-top: 13px;
}

.navbar-nav .nav-item {
  display: flex;
  align-items: center;
  transition: all 0.9s ease;
}

.navbar-nav .nav-item .nav-link {
  color: #f4ede4;
}

/* Navbar buttons */
.navbar-buttons {
  display: flex;
  align-items: center;
  justify-content: space-between;
}

.navbar-buttons i {
  font-size: 22px;
  font-weight: bolder;
  cursor: pointer;
  color: #f4ede4;
}
.navbar-buttons a {
  text-decoration: none;
  color: #f4ede4;
  margin-top: 14px;
  cursor: pointer;
}

.navbar-buttons .navbar-toggler {
  border: none;
  outline: none;
}

.navbar-toggler-icon {
  background-color: white;
}
@media (min-width: 768px) and (max-width: 1060px) {
  .navbar-nav {
    display: none;
  }
  .nav-Buttons {
    display: none;
  }
}

@media (max-width: 767px) {
  .exapanded {
    height: 326px;
    transition: all 0.5s ease;
  }
  .navbar .navbar-nav {
    flex-direction: column;
  }

  .navbar-toggler {
    width: 40px;
    height: 40px;
    z-index: 1000;
    display: flex;
    justify-content: center;
    align-items: center;
    margin-right: 10px;
    padding: 8px;
    transition: all 0.6s ease;
  }

  .navbar-nav .nav-item {
    margin-bottom: 5px;
    transition: all 0.7s ease;
  }

  .navbar-nav .nav-link {
    padding-left: 0;
  }

  .ml-auto {
    margin-left: auto !important;
  }

  .navbar-buttons {
    display: none;
  }
}
</style>
