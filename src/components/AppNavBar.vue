<template>
  <nav
    class="row navbar navbar-expand-md navbar-dark"
    :class="{ show: isMenuOpen, exapanded: isNavbarExpanded }"
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
            @click="toggleFeaturesDropdown"
            :class="{ 'dropdown-button': true, active: showFeaturesDropdown }"
          >
            <p>Features<span class="arrow" v-html="Featuresarrow"></span></p>
          </a>
        </li>
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
      isMenuOpen: false,
      showDropdown: false,
      isNavbarExpanded: false,
      Featuresarrow: "&#11167;",
      Solutionsarrow: "&#11167;",
      Resourcesarrow: "&#11167;",
    };
  },
  methods: {
    toggleMenu() {
      this.isMenuOpen = !this.isMenuOpen;
      this.isNavbarExpanded = !this.isNavbarExpanded;
    },
    toggleFeaturesDropdown() {
      this.showFeaturesDropdown = !this.showFeaturesDropdown;
      this.Featuresarrow = this.showFeaturesDropdown ? "&#11165;" : "&#11167;";
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
  },
};
</script>

<style scoped>
.navbar {
  background-color: purple;
  display: flex;
  align-items: center;
  height: 70px;
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
