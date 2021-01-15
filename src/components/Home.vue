<template>
  <div class="container-1">
    <b-row cols="2" class="mx-0">
      <b-col>
        <b-row class="small-img-row mx-0">
          <b-img fluid :src="require('../assets/Group6002.svg')"></b-img>
        </b-row>
        <b-row class="info-rows mx-0 pt-5">
          <b-row class="info-title mx-0"
            >DREAM JOBS<br />
            Waiting For You!</b-row
          >
          <b-row class="info-description mx-0 pt-5"
            >Searching and finding your dream job is now easier than ever.
            <br />
            Just browse a job and apply if you need to.</b-row
          >
          <b-row class="mx-0 pt-5" style="padding-bottom: 150px;">
            <b-button pill variant="dark" class="black-button font-18"
              >Get Started</b-button
            >
          </b-row>
        </b-row>
      </b-col>
      <b-col>
        <b-img fluid :src="require('../assets/1920.png')"></b-img>
      </b-col>
    </b-row>
    <div class="absolute-div">
      <div class="image-holder">
        <b-img
          fluid
          :src="require('../assets/all-logos.png')"
          class="relative-img"
        ></b-img>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Home",
};
</script>

<style scoped>
.small-img-row {
  padding-left: 80px;
}

.info-rows {
  padding-left: 150px;
}

.info-title {
  font-size: 86px;
  font-weight: 600;
  /* line-height: 95px; */
}

.info-description {
  font-size: 26px;
  color: var(--text-lighten1);
}

.black-button {
  padding: 20px;
  font-size: 22px !important;
}

.absolute-div {
  position: absolute;
  width: 100vw;
  display: flex;
  justify-content: center;
  align-items: center;
}

.image-holder {
  position: relative;
  box-shadow: 0px 20px 80px #7474741A;
  border-radius: 20px;
  bottom: 90px;
}

.relative-img {
  position: relative;
  border-radius: 20px;
}
</style>