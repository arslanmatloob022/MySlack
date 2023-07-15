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
      <div class="col-lg-4 col-md-4 col-sm-6 col-12 statesHeading">
        <h1>85%</h1>
        <p>of users say Slack has improved communication</p>
      </div>
      <div class="col-lg-4 col-md-4 col-sm-6 col-12 statesHeading">
        <h1>86%</h1>
        <p>feel their ability to work remotely has improved*</p>
      </div>
      <div class="col-lg-4 col-md-4 col-sm-6 col-12 statesHeading">
        <h1>88%</h1>
        <p>feel more connected to their teams</p>
      </div>
    </div>
  </section>
  <section class="second-section section-background-hec">
    <div class="row content section-data">
      <video autoplay loop class="col-12 col-sm-12 col-md-12 col-lg-6">
        <source
          src="../images/videos/slackfeaturingclients.webm"
          type="video/webm"
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
  flex-direction: column;
  align-items: center;
  color: purple;
}
.statesHeading h1 {
  font-size: 66px;
  font-weight: 700;
}
.clientDetail {
  overflow: auto;
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
  font-size: 26px;
  font-family: "Times New Roman", Times, serif;
}
.content video {
  height: 100%;
  float: left;
  width: 100%;
  border-radius: 0px 150px 150px 0px;
}
.section-background-hec {
  background-color: #faf1e5 !important;
}
</style>
