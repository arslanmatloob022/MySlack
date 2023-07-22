<template>
  <section class="footerSection">
    <div class="footerTop">
      <h1 class="footer-heading">See all you accomplish with Slack</h1>
      <div class="buttons">
        <try-sales-buttons class="trysalebtn"></try-sales-buttons>
      </div>
    </div>

    <div class="footerMenu row">
      <div class="col-lg-2 col-md-4 col-sm-12 col-12 footerLogo">
        <img src="../images/Logos/slackProLogo.png" />
      </div>

      <!-- Why Slack section -->
      <div class="col-lg-2 col-md-4 col-sm-6 col-6 menuText">
        <div class="row">
          <h6 class="col-lg-12 footHeading">WHY SLACK?</h6>
        </div>
        <div class="row">
          <p class="col-lg-12">Channels</p>
        </div>
        <div class="row">
          <p class="col-lg-12">Engagement</p>
        </div>
        <div class="row">
          <p class="col-lg-12">Scale</p>
        </div>
        <div class="row">
          <p class="col-lg-12">Watch Demo</p>
        </div>
      </div>
      <!-- Product Line -->
      <div class="col-lg-2 col-md-4 col-sm-6 col-6 menuText">
        <div class="row">
          <h6 class="col-lg-12 footHeading">PRODUCT</h6>
        </div>
        <div class="row">
          <p class="col-lg-12">Integrations</p>
        </div>
        <div class="row">
          <p class="col-lg-12">Enterprise</p>
        </div>
        <div class="row">
          <p class="col-lg-12">Solutions</p>
        </div>
      </div>

      <!-- Resources List -->
      <div class="col-lg-2 col-md-4 col-sm-6 col-6 menuText">
        <div class="row">
          <h6 class="col-lg-12 footHeading">RESOURCES</h6>
        </div>
        <div class="row">
          <p class="col-lg-12">Partners</p>
        </div>
        <div class="row">
          <p class="col-lg-12">Developers</p>
        </div>
        <div class="row">
          <p class="col-lg-12">Community</p>
        </div>
        <div class="row">
          <p class="col-lg-12">Apps</p>
        </div>
        <div class="row">
          <p class="col-lg-12">BLog</p>
        </div>
        <div class="row">
          <p class="col-lg-12">Help Center</p>
        </div>
        <div class="row">
          <p class="col-lg-12">Events</p>
        </div>
      </div>
      <!-- Company Section -->
      <div class="col-lg-2 col-md-4 col-sm-6 col-6 menuText">
        <div class="row">
          <h6 class="col-lg-12 footHeading">COMPANY</h6>
        </div>
        <div class="row">
          <p class="col-lg-12">About Us</p>
        </div>
        <div class="row">
          <p class="col-lg-12">Leadership</p>
        </div>
        <div class="row">
          <p class="col-lg-12">News</p>
        </div>
        <div class="row">
          <p class="col-lg-12">Media Kit</p>
        </div>
        <div class="row">
          <p class="col-lg-12">Careers</p>
        </div>
      </div>

      <!-- Pricing section -->
      <div class="col-lg-2 col-md-4 col-sm-6 col-6 menuText">
        <div class="row">
          <h6 class="col-lg-12 footHeading">PRICING</h6>
        </div>
        <div class="row">
          <p class="col-lg-12">Plans</p>
        </div>
        <div class="row">
          <p class="col-lg-12">Paid vs. Free</p>
        </div>
      </div>
    </div>
  </section>
  <section class="footerRibbon row">
    <div class="col-lg-3 col-md-6 col-sm-6 col-6 ribbonSection">
      <h6 class="developer">Developed By:</h6>
      <h5>Arslan Matloob</h5>
    </div>
    <div class="col-lg-3 col-md-6 col-sm-6 col-6 ribbonSection">
      <i class="uil uil-envelope"> </i
      ><a href="mailto:raoarslanmatloob@gmail.com">Send Email</a>
    </div>
    <div class="col-lg-3 col-md-6 col-sm-6 col-6 ribbonSection">
      <i class="uil uil-linkedin"> </i>
      <a href="www.linkedin.com/in/raoarslanmatloob">My LinkedIn</a>
    </div>
    <div class="col-lg-3 col-md-6 col-sm-6 col-6 ribbonSection">
      <i class="uil uil-phone"></i>
      <a href="tel:+9230076626555 ">Phone Number</a>
    </div>
  </section>
</template>

<!-- This is Script Section -->
<script>
import TrySalesButtons from "./Buttons.vue/TrySalesButtons.vue";
export default {
  name: "AppFooter",
  components: {
    TrySalesButtons,
  },
};
</script>

<!-- This is Styling Section -->
<style scoped>
.footerSection {
  margin-top: 20px;
  width: 100%;
  height: auto;
  overflow: hidden;
}
.footerTop {
  height: 280px;
  width: 100%;
  background-color: purple;
  border-radius: 0% 0% 50% 50%;
  display: flex;
  flex-direction: column;
  align-items: center;
  transform: scaleX(1.1);
}
.footerTop h1 {
  margin-top: 40px;
  font-family: "Franklin Gothic Medium", "Arial Narrow", Arial, sans-serif;
  color: white;
  font-size: calc(36px + 1vw);
}
.buttons {
  margin-top: 40px;
  width: 30%;
}
.footer-heading {
  text-align: center;
  word-wrap: break-word;
}
.trysalebtn {
  width: 100%;
}

/* Footer menu stylings*/
.footerMenu {
  width: 100%;
  height: auto;
  margin-top: 40px;
}
.footerLogo img {
  height: 60px;
  width: 60px;
}
.footHeading {
  font-weight: bold;
}
.menuText {
  margin-top: 10px;
  text-align: left;
}
@media (max-width: 667px) {
  .menuText {
    padding-left: 40px;
  }
}
.menuText .row p {
  display: inline-block;
  cursor: pointer;
}

/* footer ribbon styling*/
.footerRibbon {
  background-color: whitesmoke;
  height: auto;
}
.ribbonSection {
  display: flex;
  justify-content: center;
  align-items: center;
}
.developer {
  text-decoration: wavy;
  color: blueviolet;
}
.ribbonSection h5 {
  font-weight: bold;
  color: purple;
  font-family: "Trebuchet MS", "Lucida Sans Unicode", "Lucida Grande",
    "Lucida Sans", Arial, sans-serif;
}
.ribbonSection i {
  margin-right: 8px;
  font-size: 24px;
  color: purple;
}
.ribbonSection a {
  text-decoration: none;
}
</style>
