<template>
  <div class="container-0 padded-div">
    <b-row class="topic-title mx-0 mb-4" align-h="center" style="margin-top:150px;"
      >Browse Jobs By Category</b-row
    >
    <b-row cols="3" class="mx-0 mb-3">
      <b-col v-for="(category, index) in categoriesToDisplay" :key="index">
        <category-card
          :title="category.title"
          :tile="category.tile"
          :icon="category.icon"
          :description="category.description"
          class="hover-card"
        />
      </b-col>
    </b-row>
    <b-row class="mx-0 py-5" align-h="center">
      <b-button
        pill
        variant="dark"
        class="black-button font-18"
        @click="showAllCards = !showAllCards"
        >{{ showAllCards ? "Hide Categories" : "See All Categories" }}</b-button
      >
    </b-row>
  </div>
</template>

<script>
import CategoryCard from "./CategoryCard";

const blueTile = require("../assets/tiles/blue.svg");
const redTile = require("../assets/tiles/red.svg");
const yellowTile = require("../assets/tiles/yellow.svg");

const designIcon = require("../assets/icons/001-vector-design.svg");
const flaskIcon = require("../assets/icons/002-flask.svg");
const officeIcon = require("../assets/icons/003-office-building.svg");
const deskIcon = require("../assets/icons/004-desk.svg");
const clipboardIcon = require("../assets/icons/005-clipboard.svg");
const briefcaseIcon = require("../assets/icons/006-briefcase.svg");

const categories = [
  {
    title: "Design & Development",
    tile: blueTile,
    icon: designIcon,
    description:
      "Design & Development loremdolor sit amet, consetetur sadipscing elitr, sed diam nonumy.",
  },
  {
    title: "Science & Technologies",
    tile: redTile,
    icon: flaskIcon,
    description:
      "Design & Development loremdolor sit amet, consetetur sadipscing elitr, sed diam nonumy.",
  },
  {
    title: "Office Administrative",
    tile: yellowTile,
    icon: deskIcon,
    description:
      "Design & Development loremdolor sit amet, consetetur sadipscing elitr, sed diam nonumy.",
  },
  {
    title: "Property Development",
    tile: yellowTile,
    icon: officeIcon,
    description:
      "Design & Development loremdolor sit amet, consetetur sadipscing elitr, sed diam nonumy.",
  },
  {
    title: "Business Development",
    tile: blueTile,
    icon: briefcaseIcon,
    description:
      "Design & Development loremdolor sit amet, consetetur sadipscing elitr, sed diam nonumy.",
  },
  {
    title: "Admin && Accountant",
    tile: redTile,
    icon: clipboardIcon,
    description:
      "Design & Development loremdolor sit amet, consetetur sadipscing elitr, sed diam nonumy.",
  },
  {
    title: "Marketing",
    tile: redTile,
    icon: clipboardIcon,
    description:
      "Design & Development loremdolor sit amet, consetetur sadipscing elitr, sed diam nonumy.",
  },
  {
    title: "HR & Recruitment",
    tile: yellowTile,
    icon: deskIcon,
    description:
      "Design & Development loremdolor sit amet, consetetur sadipscing elitr, sed diam nonumy.",
  },
  {
    title: "Teaching & Training",
    tile: blueTile,
    icon: designIcon,
    description:
      "Design & Development loremdolor sit amet, consetetur sadipscing elitr, sed diam nonumy.",
  },
];

export default {
  name: "BrowseJobs",
  components: { CategoryCard },
  data() {
    return {
      categories,
      showAllCards: false,
    };
  },
  computed: {
    categoriesToDisplay() {
      let length = 6;
      if (this.showAllCards) length = 9;
      return this.categories.slice(0, length);
    },
  },
};
</script>

<style scoped>
.padded-div {
  padding-top: 40px;
  padding-bottom: 20px;
}

.topic-title {
  font-size: 60px;
  font-weight: 600;
  margin-top: 50px;
}

.black-button {
  padding: 20px;
  font-size: 22px !important;
}

.hover-card {
  box-shadow: 0px 15px 20px #7474741a;
  transition: all .3s ease-in-out;
}
.hover-card:hover {
  box-shadow: 0px 30px 40px #74747440;
  transform: translate3d(0px, -1px, 0px);
  cursor: pointer;
}
</style>