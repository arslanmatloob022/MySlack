<template>
  <section class="first-section enterprise-section">
    <div class="row section-data">
      <p class="col-lg-12 col-md-12 col-sm-12 col-12 data-heading">
        Built with enterprises, for enterprises
      </p>
      <p class="col-lg-12 col-md-12 col-sm-12 col-12 sub-heading">
        Slack is secure. It’s flexible. It’s software that people actually enjoy
        using. And it’s here to help your business.
      </p>

      <video
        muted
        playsinline
        autoplay
        loop
        class="col-lg-6 col-md-12 col-sm-12 col-12"
        style="float:left width:100%; height:500px"
      >
        <source
          src="../images/videos/EnterpriseVideos/Scale_with_Slack.mp4"
          type="video/mp4"
        />
        <source
          src="../images/videos/EnterpriseVideos/Scale_with_Slack.webm"
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
}
.enterprise-section {
}
.data-heading {
  font-size: calc(6px + 1vw);
}
.sub-heading {
}
</style>
