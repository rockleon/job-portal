<template>
  <div>
    <div class="container-0 end-panel">
      <b-row no-gutters>
        <b-col cols="2" class="col-vertical">
          <span class="span-title">Categories</span>
          <span class="span-item">Content Writer</span>
          <span class="span-item">Backend Developer</span>
          <span class="span-item">Creative Director</span>
          <span class="span-item">UI Designer</span>
          <span class="span-item ochre">More...</span>
        </b-col>
        <b-col cols="2" class="col-vertical">
          <span class="span-title">Resource</span>
          <span class="span-item">Contact Support</span>
          <span class="span-item">Application</span>
          <span class="span-item">FAQ</span>
          <span class="span-item">Careers</span>
        </b-col>
        <b-col cols="2" class="col-vertical">
          <span class="span-title">Company</span>
          <span class="span-item">About Us</span>
          <span class="span-item">Job Seminar</span>
          <span class="span-item">Blog</span>
          <span class="span-item">News</span>
        </b-col>
        <b-col cols="2" class="col-vertical">
          <span class="span-title">Legals</span>
          <span class="span-item">Copyright</span>
          <span class="span-item">Privacy</span>
          <span class="span-item">Disclaimer</span>
          <span class="span-item">Terms</span>
        </b-col>
        <b-col cols="4" class="col-vertical">
          <span class="span-logo ochre">DREAMJOB.</span>
          <span class="span-item"
            >Design & Development loremdolor sit amet, consetetur sadipscing
            elitr, sed diam nonumy.</span
          >
        </b-col>
      </b-row>
    </div>
    <b-row no-gutters class="footer" align-h="center"
      >Copyright © 2020 DREAMJOB. All rights reserved.</b-row
    >
  </div>
</template>

<script>
export default {
  name: "EndPanel",
};
</script>

<style scoped>
.end-panel {
  background-color: #1b2e3d;
  color: white;
  padding-top: 90px;
  padding-bottom: 60px;
}

.span-title {
  font-size: 22px;
  margin-bottom: 30px;
}

.span-item {
  font-size: 18px;
  margin-bottom: 20px;
}

.col-vertical {
  display: flex;
  flex-direction: column;
}

.span-logo {
  font-size: 32px;
  margin-bottom: 15px;
}

.ochre {
  color: #ffda55;
}

.footer {
  background-color: #101e2a;
  color: white;
  font-size: 18px;
  padding: 32px 0px;
}
</style>