<template>
  <section class="landing-section">
    <div class="row content section-data">
      <div class="col-12 col-sm-12 col-md-12 col-lg-6 section-text">
        <h1 class="animated-text">Bring your team together</h1>
        <p class="animated-text quote-text">
          At the heart of Slack are channels: organized spaces for everyone and
          everything you need for work. In channels, it’s easier to connect
          across departments, offices, time zones and even other companies
        </p>
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
  <section
    class="first-section first-section-companies v--borderless section-background-hec bottom-padding"
  >
    <p class="display-as-subnav u-text--center">
      Trusted by companies all over the world
    </p>
    <div class="nav-bar-comp-logos u-text--center">
      <div class="first-section-companies__logos">
        <div class="logos-bar">
          <img src="../images/Logos/Airbnb.png" alt="Air BnB" />
        </div>
        <div class="logos-bar">
          <img src="../images/Logos/AdobePS.png" alt="Adobe PhotoShop" />
        </div>
        <div class="logos-bar">
          <img src="../images/Logos/NASA.png" alt="NASA" />
        </div>
        <div class="logos-bar">
          <img src="../images/Logos/etsy.png" alt="Etsy" />
        </div>
        <div class="logos-bar">
          <img
            src="../images/Logos/newyorktimes.png"
            alt="The New York Times"
          />
        </div>
        <div class="logos-bar">
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
      </div>
    </div>
  </section>
</template>

<script></script>
<style>
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
    max-width: 170px;
    margin: 10px;
    text-align: center;
  }
}

/* Text Animatiions*/
.quote-text {
  width: 80%;
  overflow: auto;
  word-wrap: break-word;
}
.animated-text {
  animation: text-animation 3s;
}

@keyframes text-animation {
  0% {
    opacity: 0;
    transform: translateX(20px);
  }
  50% {
    opacity: 1;
    transform: translateX(0);
  }
  100% {
    opacity: 0;
    transform: translateX(-20px);
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
