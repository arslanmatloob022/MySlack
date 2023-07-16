<template>
  <!-- First Purple Section -->
  <section class="landing-section">
    <div class="row content section-data purple-section">
      <div class="col-12 col-sm-12 col-md-12 col-lg-6">
        <div class="row">
          <div class="col-lg-12 col-md-12 col-sm-12 col-12 landing-headings">
            <h1 class="first-heading">Made for people.</h1>
            <span><h1 class="second-heading">Built for productivity.</h1></span>
          </div>
        </div>
        <div class="row purple-text">
          <div class="col-lg-10 col-md-12 col-sm-12 col-12">
            <p class="quote-text">
              Connect the right people, find anything you need and automate the
              rest. That’s work in Slack, your productivity platform.
            </p>
          </div>
        </div>
        <div class="row">
          <div class="col-lg-12 col-md-12 col-sm-12 col-12 purple-buttons">
            <Button
              class="col-lg-5 col-md-6 col-sm-12 col-12 email-signup-button"
              >SIGN UP WITH EMAIL</Button
            >
            <Button
              class="col-lg-5 col-md-6 col-sm-12 col-12 google-signup-button"
              ><span><i class="uil uil-google"></i></span>SIGN UP WITH
              Google</Button
            >
          </div>
        </div>
        <div class="row purple-text">
          <p class="quote-text">
            Slack is free to try for as long as you’d like
          </p>
        </div>
      </div>
      <video
        autoplay
        loop
        class="col-12 col-sm-12 col-md-12 col-lg-6"
        style="float:left width:100%; height:500px"
      >
        <source src="../images/videos/SlackLanding.webm" type="video/webm" />
        <source src="../images/videos/SlackLanding.webm" type="video/webm" />
      </video>
    </div>
  </section>

  <!-- Sales Comapnies Section -->
  <section
    class="first-section first-section-companies v--borderless section-background-hec bottom-padding"
  >
    <p class="display-as-subnav u-text--center">
      Trusted by companies all over the world
    </p>
    <div class="nav-bar-comp-logos u-text--center">
      <div class="row first-section-companies__logos">
        <div class="col-lg-1.5 col-md-4 col-sm-4 col-4 logos-bar">
          <img src="../images/Logos/Airbnb.png" alt="Air BnB" />
        </div>
        <div class="col-lg-1.5 col-md-4 col-sm-4 col-4 logos-bar">
          <img src="../images/Logos/AdobePS.png" alt="Adobe PhotoShop" />
        </div>
        <div class="col-lg-1.5 col-md-4 col-sm-4 col-4 logos-bar">
          <img src="../images/Logos/NASA.png" alt="NASA" />
        </div>
        <div class="col-lg-1.5 col-md-4 col-sm-4 col-4 logos-bar">
          <img src="../images/Logos/etsy.png" alt="Etsy" />
        </div>
        <div class="col-lg-1.5 col-md-4 col-sm-4 col-4 logos-bar">
          <img
            src="../images/Logos/newyorktimes.png"
            alt="The New York Times"
          />
        </div>
        <div class="col-lg-1.5 col-md-4 col-sm-4 col-4 logos-bar">
          <img src="../images/Logos/uber.png" alt="Uber" />
        </div>
      </div>
    </div>
  </section>

  <section class="second-section section-background-hec">
    <div class="row content section-data">
      <video
        autoplay
        loop
        class="col-12 col-sm-12 col-md-12 col-lg-6"
        style="float:left width:100%; height:400px"
      >
        <source src="../images/videos/slackMovefaster.webm" type="video/webm" />
        <source src="../images/videos/slackMovefaster.webm" type="video/webm" />
      </video>
      <div class="col-12 col-sm-12 col-md-12 col-lg-6 section-text">
        <h1 class="animated-text">Move faster with your tools in one place</h1>
        <p class="animated-text quote-text">
          Automate away routine tasks with the power of generative AI and
          simplify your workflow with all your favorite apps ready to go in
          Slack
        </p>
        <p
          class="link-text"
          @mouseover="startUnderlineAnimation(1)"
          @mouseleave="stopUnderlineAnimation(1)"
        >
          Learn more about the Slack Plateform.<span>&#x2192;</span>
          <span
            class="underline"
            :class="{ 'underline-animate': animateUnderline[1] }"
          ></span>
        </p>
      </div>
    </div>
  </section>

  <section class="second-section section-background-hec">
    <div class="row content section-data">
      <div class="col-12 col-sm-12 col-md-12 col-lg-6 section-text">
        <h1 class="animated-text">Choose how you want to work</h1>
        <p class="animated-text quote-text">
          In Slack, you’ve got all the flexibility to work when, where and how
          it’s best for you. You can easily chat, send audio and video clips, or
          hop on a huddle to talk things out live.
        </p>
        <p
          class="link-text"
          @mouseover="startUnderlineAnimation(2)"
          @mouseleave="stopUnderlineAnimation(2)"
        >
          Learn more about Flexible Communication<span>&#x2192;</span>
          <span
            class="underline"
            :class="{ 'underline-animate': animateUnderline[2] }"
          ></span>
        </p>
      </div>
      <video
        autoplay
        loop
        class="col-12 col-sm-12 col-md-12 col-lg-6"
        style="float:left width:100%; height:400px"
      >
        <source src="../images/videos/slackChoose.webm" type="video/webm" />
        <source src="../images/videos/slackChoose.webm" type="video/webm" />
      </video>
    </div>
  </section>

  <section class="second-section section-background-hec">
    <div class="row content section-data">
      <video
        autoplay
        loop
        class="col-12 col-sm-12 col-md-12 col-lg-6"
        style="float:left width:100%; height:400px"
      >
        <source src="../images/videos/slackPromovideo.webm" type="video/webm" />
        <source src="../images/videos/slackPromovideo.webm" type="video/webm" />
      </video>
      <div class="col-12 col-sm-12 col-md-12 col-lg-6 section-text">
        <h1 class="animated-text">Bring your team together</h1>
        <p class="animated-text quote-text">
          At the heart of Slack are channels: organized spaces for everyone and
          everything you need for work. In channels, it’s easier to connect
          across departments, offices, time zones and even other companies
        </p>
        <p
          class="link-text"
          @mouseover="startUnderlineAnimation(3)"
          @mouseleave="stopUnderlineAnimation(3)"
        >
          Learn more about Channels<span>&#x2192;</span>
          <span
            class="underline"
            :class="{ 'underline-animate': animateUnderline[3] }"
          ></span>
        </p>
      </div>
    </div>
  </section>
</template>

<script>
import TrySalesButtonsVue from "@/components/Buttons.vue/TrySalesButtons.vue";
export default {
  name: "AppLandingView",
  components: {
    TrySalesButtonsVue,
  },
  data() {
    return {
      animateUnderline: {
        1: false,
        2: false,
        3: false,
      },
    };
  },
  methods: {
    startUnderlineAnimation(linkIndex) {
      this.animateUnderline[linkIndex] = true;
    },
    stopUnderlineAnimation(linkIndex) {
      this.animateUnderline[linkIndex] = false;
    },
  },
};
</script>
<style scoped>
/*purple landing section*/
.purple-section {
  display: flex;
  align-items: center;
}
.landing-headings .first-heading {
  color: #f4ede4;
  font-size: 52px;
  font-weight: 900;
}
.landing-headings .second-heading {
  color: orange;
  font-size: 52px;
  font-weight: 900;
}
.purple-text {
  margin-top: 10px;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
  color: #f4ede4;
}
.purple-buttons button {
  padding: 12px 10px;
  border: 2px solid #f4ede4;
  border-radius: 5px;
  font-family: "Segoe UI", Tahoma, Geneva, Verdana, sans-serif;
  font-weight: 600;
}
.purple-buttons button:hover {
  transform: scale(1.01);
}
.email-signup-button {
  color: rgb(116, 1, 116);
  background-color: #f4ede4;
}
.google-signup-button {
  margin-left: 10px;
  color: #f4ede4;
  background-color: rgb(56, 166, 235);
}
.google-signup-button i {
  margin-right: 8px;
  color: rgb(255, 255, 255);
  font-size: 12px;
}
@media screen and (max-width: 992px) {
  .purple-buttons {
    margin-left: 14px;
  }
  .google-signup-button {
    margin-left: 0px;
    margin-top: 10px;
  }
}
/* Main div Css*/
/* Section Nav */
.landing-section .section-nav {
  background-color: purple;
  display: flex;
  align-items: center;
  height: 70px;
}
.logo-nav {
  cursor: pointer;
  text-decoration: none;
  display: flex;
  justify-content: center;
  align-items: center;
}
.logo-nav h1 {
  font-family: "Segoe UI", Tahoma, Geneva, Verdana, sans-serif;
  font-weight: bold;
  color: #f4ede4;
  margin-left: 4px;
}
.links-nav {
  display: flex;
  align-items: center;
  justify-content: space-around;
}
.links-nav a {
  text-decoration: none;
  font-weight: bold;
  color: #f4ede4;
}
/* Link Text Animation*/
.link-text {
  position: relative;
  display: inline-block;
  cursor: pointer;
  font-weight: bold;
  color: rgb(1, 116, 116);
}

.underline {
  position: absolute;
  bottom: 0;
  left: 0;
  width: 0;
  height: 2px;
  background-color: rgb(9, 175, 175);
  transition: width 0.5s ease-in-out;
}

.underline-animate {
  width: 100%;
}
/* Landing Section */
.landing-section {
  background-color: rgb(116, 7, 116);
}
/* first Section comapanies bar  styling*/
.first-section.v--borderless {
  border: none;
}
.section-background-hec {
  background-color: #f4ede4 !important;
}
.bottom-padding {
  padding-bottom: 0rem !important;
}
.display-as-subnav {
  font-family: Slack-Circular-Pro, "Helvetica Neue", Helvetica, "Segoe UI",
    Tahoma, Arial, sans-serif;
  font-weight: 700;
  line-height: 1.125;
  letter-spacing: 0.8px;
  font-size: 0.875rem;
  margin-bottom: 1rem;
  text-transform: uppercase;
  margin-top: 20px;
}
.u-text--center {
  margin-top: 5px;
  text-align: center !important;
}
p {
  margin: 0;
  margin-bottom: 1rem;
}
.nav-bar-comp-logos {
  margin: 0 auto;
  padding: 0 8vw;
}
.first-section-companies__logos {
  display: flex;
  justify-content: center;
  flex-wrap: wrap;
  justify-content: space-around;
  align-items: center;
}
.first-section-companies__logos .logos-bar {
  max-width: unset;
  display: flex;
}
.first-section-companies__logos .logos-bar img {
  width: 100%;
  height: 40px;
}
@media screen and (min-width: 25rem) {
  .display-as-subnav {
    font-size: calc(0.875rem + (0 * (100vw - 400px) / 624));
  }
}

@media screen and (min-width: 48rem) {
  .nav-bar-comp-logos {
    padding: 0 4vw;
  }
}

@media screen and (min-width: 48rem) {
  .first-section-companies__logos {
    display: flex;
    justify-items: center;
    max-width: 1010px;
    margin-left: auto;
    margin-right: auto;
    justify-content: space-around;
  }
  .first-section-companies__logos .logos-bar {
    max-width: 120px;
    margin: 10px;
    text-align: center;
  }
}

/* Text Animatiions*/
.quote-text {
  width: 100%;
  overflow: auto;
  word-wrap: break-word;
}
.animated-text {
  margin-top: 20px;
  animation: text-animation 3s;
}

@keyframes text-animation {
  0% {
    opacity: 0;
    transform: translateX(30px);
  }
  25% {
    opacity: 0.25;
    transform: translateX(20px);
  }
  50% {
    opacity: 0.5;
    transform: translateX(15px);
  }
  75% {
    opacity: 0.75;
    transform: translateX(10px);
  }
  100% {
    opacity: 1;
    transform: translateX(0px);
  }
}
/*second  section styling*/
.second-section {
  margin-top: 20px;
  width: 100%;
}
.section-data {
  width: 100%;
  display: flex;
  align-items: center;
  justify-content: space-between;
}
.section-text {
  display: flex;
  flex-direction: column;
  align-items: center;
}
.section-text h1 {
  font-weight: bold;
}
.section-text p {
  font-size: 18px;
  font: bold;
}
</style>
