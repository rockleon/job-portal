<template>
  <div class="container-0 container-1 padded-box">
    <b-row cols="2" class="mx-0">
      <b-col class="pl-0">
        <b-row class="panel-title mx-0"
          >Build and Boost<br />
          Your Great Profile</b-row
        >
        <b-row class="panel-description mx-0 pt-5"
          >Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer nec
          odio. Praesent libero. Sed cursus ante dapibus diam. Sed nisi. Nulla
          quis sem at nibh elementum imperdiet.</b-row
        >
        <b-row class="mx-0 pt-5">
          <b-button pill variant="dark" class="black-button font-18"
            >Register Now</b-button
          >
        </b-row>
      </b-col>
      <b-col class="pr-0" align="end">
        <b-img fluid :src="require('../assets/People.png')"></b-img>
      </b-col>
    </b-row>
  </div>
</template>

<script>
export default {
  name: "ProfileRegister",
};
</script>

<style scoped>
.padded-box {
  padding-top: 150px;
  padding-bottom: 150px;
}

.topic-title {
  font-size: 80px;
  font-weight: 600;
  margin-top: 50px;
}

.panel-title {
  font-size: 80px;
  font-weight: 600;
  line-height: 100px;
  padding-top: 50px;
}

.panel-description {
  font-size: 26px;
  color: var(--text-lighten1);
}

.black-button {
  padding: 20px;
  font-size: 22px !important;
}
</style>