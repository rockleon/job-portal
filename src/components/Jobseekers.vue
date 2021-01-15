<template>
  <div class="horizontal-div">
    <div class="side-div">
      <b-img fluid :src="require('../assets/checks.svg')"></b-img>
    </div>
    <div class="main-div">
      <b-row class="mx-0">
        <b-col cols="6" class="img-col pl-0">
          <b-img
            fluid-grow
            rounded="circle"
            :src="reviews[reviewIndex].url"
          ></b-img>
        </b-col>
        <b-col cols="6" class="pr-0">
          <b-row class="panel-title mx-0"
            >What our<br />
            Jobseekers Said.</b-row
          >
          <b-row class="panel-description mx-0 pt-5"
            >"{{ reviews[reviewIndex].review }}"</b-row
          >
          <b-row class="mx-0 pt-5 name-title">{{
            reviews[reviewIndex].name
          }}</b-row>
          <b-row class="panel-description mx-0">{{
            reviews[reviewIndex].role
          }}</b-row>
          <b-row class="mx-0 pt-4">
            <b-img
              fluid
              class="arrow-img"
              :src="require('../assets/arrow-left.svg')"
              style="margin-right: 30px"
              @click="previousSlide"
            ></b-img>
            <b-img
              fluid
              class="arrow-img"
              :src="require('../assets/arrow-right.svg')"
              @click="nextSlide"
            ></b-img>
          </b-row>
        </b-col>
      </b-row>
    </div>
    <div class="side-div">
      <b-img
        fluid
        :src="require('../assets/Shape.svg')"
        style="margin-top: 90px"
      ></b-img>
      <b-img fluid :src="require('../assets/checks-dark.svg')"></b-img>
    </div>
  </div>
</template>

<script>
const reviews = [
  {
    url: require("../assets/Ellipse.jpg"),
    name: "Erik Shanon",
    role: "React Developer",
    review:
      "Lorem ipsum dolor sit amet, adipiscing elit. Integer nec odio. Praesent libero. Sed cursus ante dapibus diam. Sed nisi. Nulla quis sem at nibh elementum imperdiet.",
  },
  {
    url: require("../assets/People.png"),
    name: "Marshal Mathers",
    role: "Cloud Computing Engineer",
    review:
      "Sed ut perspiciatis unde omnis iste natus error, veritatis et quasi architecto beatae vitae dicta sunt explicabo. Nemo enim ipsam voluptatem quia voluptas.",
  },
  {
    url: require("../assets/tiles/red.svg"),
    name: "Mat Henry",
    role: "Data Analyst",
    review:
      "At vero eos et accusamus et iusto odio dignissimos ducimus qui blanditiis praesentium voluptatum deleniti atque corrupti quos dolores et quas.",
  },
  {
    url: require("../assets/tiles/blue.svg"),
    name: "Noel Shak",
    role: "Freelance",
    review:
      "Et harum quidem rerum facilis est et expedita distinctio. Nam libero tempore, cum soluta nobis est eligendi optio cumque nihil impedit quo.",
  },
];

export default {
  name: "Jobseekers",
  data() {
    return {
      reviews,
      reviewIndex: 0,
    };
  },
  methods: {
    nextSlide() {
      console.log("next");
      this.reviewIndex = (this.reviewIndex + 1) % 4;
    },
    previousSlide() {
      let index = this.reviewIndex - 1;
      if (index === -1) index = 3;
      this.reviewIndex = index;
    },
  },
};
</script>

<style scoped>
.horizontal-div {
  display: flex;
  flex-direction: row;
  padding: 60px 0px;
}

.side-div {
  width: 225px;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
}

.main-div {
  width: calc(100vw - 450px);
}

.img-col {
  display: flex;
  align-items: center;
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

.name-title {
  font-size: 32px;
}

.arrow-img:hover {
  cursor: pointer;
}
</style>