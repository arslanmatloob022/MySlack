<template>
  <section class="first-section enterprise-section">
    <div class="row section-data">
      <div class="col-lg-6 col-md-12 col-sm-12 col-12">
        <div class="row text-content">
          <p class="col-lg-12 col-md-12 col-sm-12 col-12 data-heading">
            Built with enterprises, for enterprises
          </p>
          <p class="col-lg-12 col-md-12 col-sm-12 col-12 sub-heading">
            Slack is secure. It’s flexible. It’s software that people actually
            enjoy using. And it’s here to help your business.
          </p>
        </div>
        <div class="row slack-support">
          <p class="support-text col-lg-12 col-md-12 col-sm-12 col-12">
            Learn how Slack supports organizations of all sizes:
          </p>

          <div class="col-lg-6 col-md-6 col-sm-12 col-12 link-icon">
            <i class="uil uil-check-circle"
              ><span><a href="#" class="support-link">SCALE</a></span></i
            >
          </div>

          <div class="col-lg-6 col-md-6 col-sm-12 col-12 link-icon">
            <i class="uil uil-check-circle"
              ><span><a href="#" class="support-link">SCALE</a></span></i
            >
          </div>

          <div class="col-lg-6 col-md-6 col-sm-12 col-12 link-icon">
            <i class="uil uil-check-circle"
              ><span><a href="#" class="support-link">SEQURITY</a></span></i
            >
          </div>

          <div class="col-lg-6 col-md-6 col-sm-12 col-12 link-icon">
            <i class="uil uil-check-circle"
              ><span><a href="#" class="support-link">ENGAGEMENT</a></span></i
            >
          </div>

          <div class="col-lg-6 col-md-6 col-sm-12 col-12 link-icon">
            <i class="uil uil-check-circle"
              ><span><a href="#" class="support-link">PLATFORM</a></span></i
            >
          </div>

          <div class="col-lg-6 col-md-6 col-sm-12 col-12 link-icon">
            <i class="uil uil-check-circle"
              ><span
                ><a href="#" class="support-link">SLACK CONNECT</a></span
              ></i
            >
          </div>
        </div>
      </div>

      <video
        muted
        playsinline
        autoplay
        class="col-lg-6 col-md-12 col-sm-12 col-12"
        style="float:left width:100%; height:500px"
      >
        <source
          src="../images/videos/EnterpriseVideos/Stackedblocks.webm"
          type="video/mp4"
        />
        <source
          src="../images/videos/EnterpriseVideos/Stackedblocks.mp4"
          type="video/webm"
        />
      </video>
    </div>
  </section>
</template>
<script>
export default {
  name: "EnterpriseView",
};
</script>

<style scoped>
.first-section {
  margin-top: 70px;
}

.enterprise-section {
}
.section-data {
  margin-top: 150px;
}
.text-content {
  padding-left: calc(50px + 1vw);
}
.data-heading {
  text-align: left;
  font-family: "Times New Roman", Times, serif;
  font-size: calc(28px + 1vw);
  font-weight: 800;
}
.sub-heading {
  text-align: left;
  font-family: "Franklin Gothi Medium", "Arial Narrow", Arial, sans-serif;
  font-size: calc(12px + 1vw);
}
.slack-support {
  margin-top: 10%;
  padding-left: calc(50px + 1vw);
}
.support-text {
  color: black;
  font-size: calc(7px + 1vw);
  text-align: left;
}
.link-icon {
  text-align: left;
}
.link-icon i {
  font-size: calc(4px + 1vw);
  color: rgb(15, 15, 15);
}
.support-link {
  color: black;
  text-decoration: underline;
  font-family: "Franklin Gothic Medium", "Arial Narrow", Arial, sans-serif;
}
</style>
