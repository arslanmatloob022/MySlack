<template>
  <section class="landing-last-section row">
    <div class="Headings col-lg-12 col-md-12 col-sm-12 col-12">
      <p class="teamsHeading">Teams large and small rely on Slack</p>
      <p class="teamsText">
        Slack securely scales up to support collaboration at the world’s biggest
        companies.
      </p>
      <div class="trysalebuttons">
        <try-sales-buttons></try-sales-buttons>
      </div>
    </div>
    <div class="row states">
      <div class="col-lg-4 col-md-4 col-sm-6 col-6">
        <div class="statesHeading">
          <h1>85%</h1>
          <p class="quote-texts">
            of users say Slack has improved communication
          </p>
        </div>
      </div>
      <div class="col-lg-4 col-md-4 col-sm-6 col-6">
        <div class="statesHeading">
          <h1>86%</h1>
          <p class="quote-texts">
            feel their ability to work remotely has improved*
          </p>
        </div>
      </div>
      <div class="col-lg-4 col-md-4 col-sm-12 col-12">
        <div class="statesHeading">
          <h1>88%</h1>
          <p class="quote-texts">feel more connected to their teams</p>
        </div>
      </div>
    </div>
  </section>
  <section class="second-section section-background-hec">
    <div class="row content section-data">
      <video
        muted
        autoplay
        playsinline
        loop
        role="img"
        class="col-12 col-sm-12 col-md-12 col-lg-6"
      >
        <source
          src="../images/videos/slackfeaturingclients.mp4"
          type="video/mp4"
        />
        <source
          src="../images/videos/slackfeaturingclients.webm"
          type="video/webm"
        />
      </video>
      <div class="col-12 col-sm-12 col-md-12 col-lg-6 section-text">
        <p class="quote-text">
          “Whether you’re a small or large organization, executing anything from
          a discrete modernization program to a digital transformation
          initiative, Slack is an incredibly powerful tool in the hybrid world.”
        </p>
        <div class="clientDetail row">
          <h5 class="name col-lg-12 col-md-12 col-sm-12">
            <b>Jennifer Quinlan</b>
          </h5>
          <p class="designation">
            Managing Partner, IBM iX Americas Leader - Customer and Experience
            Transformation, IBM
          </p>
        </div>
        <p
          class="link-text"
          @mouseover="startUnderlineAnimation(1)"
          @mouseleave="stopUnderlineAnimation(1)"
        >
          See more customer stories<span>&#x2192;</span>
          <span
            class="underline"
            :class="{ 'underline-animate': animateUnderline[1] }"
          ></span>
        </p>
      </div>
    </div>
  </section>
</template>
<script>
import TrySalesButtons from "./Buttons.vue/TrySalesButtons.vue";
export default {
  name: "LandingPageEndContent",
  components: {
    TrySalesButtons,
  },
  data() {
    return {
      animateUnderline: {
        1: false,
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
.landing-last-section {
  width: 100%;
  background-position: center;
  background-repeat: no-repeat;
}
.Headings {
  margin-top: 50px;
  font-family: Georgia, "Times New Roman", Times, serif;
  display: flex;
  flex-direction: column;
  align-items: center;
  resize: both;
}
.teamsHeading {
  color: black;
  margin-top: 10px;
  font-size: calc(36px + 1vw);
  font-weight: calc(800 + 0.5vw);
}
.teamsText {
  font-size: calc(8px + 1vw);
  font-weight: 500;
  margin-top: 14px;
}
.trysalebuttons {
  margin-top: 30px;
  display: flex;
  margin-left: 10%;
  align-items: center;
  width: 40%;
}
.states {
  margin-top: 80px;
}
.statesHeading {
  display: flex;
  justify-content: center;
  flex-direction: column;
  align-items: center;
  color: purple;
}
.quote-texts {
  display: flexbox;
}
@media (max-width: 667px) {
  .quote-texts {
    padding: 10%;
  }
}
.statesHeading h1 {
  font-size: calc(66px + 1vw);
  font-weight: 700;
  cursor: default;
}
.clientDetail {
  overflow: auto;
}
@media (max-width: 667px) {
  .clientDetail,
  .link-text {
    padding-left: 6%;
  }
}

.clientDetail .name {
  float: left;
  text-align: left;
}
.clientDetail .designation {
  text-align: left;
  float: left;
}
.link-text {
  font-size: calc(12px + 1vw);
  float: left;
  position: relative;
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
  background-color: rgb(32, 88, 88);
  transition: width 0.5s ease-in-out;
}
.underline-animate {
  width: 100%;
}
.second-section {
  margin-top: 60px;
  width: 100%;
}
.section-data {
  width: 100%;
  display: flex;
  align-items: center;
  justify-content: space-between;
}
.quote-text {
  margin-top: 10px;
  font-size: calc(16px + 1vw);
  font-family: "Times New Roman", Times, serif;
}
.content video {
  margin-top: 20px;
  margin-bottom: 20px;
  height: 100%;
  float: left;
  margin-left: 0;
  width: 100%;
  border-radius: 0px 200px 200px 0px;
}
.section-background-hec {
  background-color: #faf1e5 !important;
}
</style>
