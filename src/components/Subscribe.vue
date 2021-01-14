<template>
  <div class="container-0 container-1 padded-box">
    <div class="subscribe-box">
      <b-row class="subscribe-title mx-0 pb-5" align-h="center">
        Subscribe to Our Newsletter for <br />
        the Weekly Updates.
      </b-row>
      <b-row class="mx-0 pt-2 pb-2" align-h="center">
        <b-img
          fluid
          :src="require('../assets/mail.svg')"
          class="mail-img"
        ></b-img>
        <input type="email" placeholder="Enter your email address here" />
        <b-button pill variant="dark" class="black-button"
          >Subscribe</b-button
        >
      </b-row>
    </div>
  </div>
</template>

<script>
export default {
  name: "Subscribe",
};
</script>

<style scoped>
.padded-box {
  padding-top: 150px;
  padding-bottom: 150px;
}

.subscribe-box {
  background-color: #fab8c4;
  color: white;
  border-radius: 218px;
  padding: 80px 0px;
}

.subscribe-title {
  font-size: 60px;
  text-align: center;
}

input {
  border-radius: 52px;
  padding: 20px;
  font-size: 24px;
  border-color: white;
  width: 650px;
  padding-left: 100px;
}

.mail-img {
  position: relative;
  left: 65px;
}

.black-button {
  padding: 20px;
  font-size: 24px !important;
  position: relative;
  left: -63px;
}
</style>