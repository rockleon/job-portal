<template>
  <div id="app">
    <b-container fluid class="px-0">
      <b-row class="title-bar mx-0">
        <b-col cols="9">
          <b-img
            fluid
            :src="require('./assets/DREAMJOB.svg')"
            class="logo"
          ></b-img>
          <span class="menu-span font-18">Home</span>
          <span class="menu-span font-18">Job Seekers</span>
          <span class="menu-span font-18">Post A Job</span>
          <span class="menu-span font-18">Contact Us</span>
        </b-col>
        <b-col cols="3" align="end">
          <b-button pill variant="outline-info" class="font-18"
            >Sign Up</b-button
          >
          <b-button pill class="button-primary font-18">Free trial</b-button>
        </b-col>
      </b-row>
      <home />
      <browse-jobs />
      <profile-register />
      <jobseekers />
      <subscribe />
      <end-panel />
    </b-container>
  </div>
</template>

<script>
import Home from "./components/Home";
import BrowseJobs from "./components/BrowseJobs";
import ProfileRegister from "./components/ProfileRegister";
import Subscribe from "./components/Subscribe";
import EndPanel from "./components/EndPanel.vue";
import Jobseekers from './components/Jobseekers.vue';

export default {
  name: "App",
  components: { Home, BrowseJobs, ProfileRegister, Subscribe, EndPanel, Jobseekers },
};
</script>

<style>
:root {
  --primary: #f8f9fb;
  --text: #181818;
  --text-lighten1: #747474;
}

@import url("https://fonts.googleapis.com/css2?family=Inter&display=swap");

#app {
  font-family: "Inter", sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: var(--text);
  background-color: white;
}

.title-bar {
  background-color: var(--primary);
  padding: 40px 80px 30px;
}

.title-bar .logo {
  padding-right: 20px;
}

.menu-span {
  margin-left: 60px;
  color: var(--text-lighten1);
}

.container-0 {
  padding-left: 255px;
  padding-right: 255px;
}

.container-1 {
  background-color: var(--primary);
}

.button-primary {
  background-color: #0f47c0;
  margin-left: 30px;
}

.font-18 {
  font-size: 18px !important;
  font-weight: 500;
}
</style>
