<template>
  <nav class="row navbar navbar-expand-md navbar-dark">
    <a class="col-2 logo-nav">
      <img
        src="../images/Logos/slackProLogo.png"
        alt=""
        style="width: 40px; height: 40px"
      />
      <h1>Slack</h1>
    </a>
    <div class="col-6 collapse navbar-collapse" :class="{ show: isMenuOpen }">
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
    <div class="col-4 navbar-buttons">
      <i class="uil uil-search"></i>
      <a class="navbtn-signin">
        <P>Sign in</P>
      </a>
      <button class="navButtons" id="salesBtn">TALK TO SALES</button>
      <button class="navButtons" id="tryBtn">TRY FOR FREE</button>
    </div>
    <button
      class="navbar-toggler"
      id="tryBtn"
      type="button"
      @click="toggleMenu"
    >
      <span class="uil uil-bars"></i></span>
    </button>
  </nav>
</template>

<script>
export default {
  data() {
    return {
      isMenuOpen: false,
      showDropdown: false,
      Featuresarrow: "&#11167;",
      Solutionsarrow: "&#11167;",
      Resourcesarrow: "&#11167;",
    };
  },
  methods: {
    toggleMenu() {
      this.isMenuOpen = !this.isMenuOpen;
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

.navbar-buttons .navButtons {
  padding: 8px 12px;
  border: 2px solid #f4ede4;
  border-radius: 5px;
  font-family: "Segoe UI", Tahoma, Geneva, Verdana, sans-serif;
  font-weight: 600;
}

.navbar-buttons .navButtons:hover {
  transform: scale(1.02);
}

.navbar-buttons #salesBtn {
  background-color: transparent;
  color: #f4ede4;
}

.navbar-buttons #tryBtn {
  color: rgb(116, 1, 116);
  background-color: #f4ede4;
}

.navbar-toggler-icon {
  background-color: white;
}

@media (max-width: 767px) {
  .navbar .navbar-nav {
    flex-direction: column;
  }

  .navbar-toggler {
    margin-top: 5px;
  }

  .navbar-nav .nav-item {
    margin-bottom: 10px;
  }

  .navbar-nav .nav-link {
    padding-left: 0;
  }

  .ml-auto {
    margin-left: auto !important;
  }
  .col-4 {
    display: none;
  }
  .navbar-buttons {
    display: none;
  }
}
</style>
