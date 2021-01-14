<template>
  <div class="card-container">
    <b-row class="mx-0">
      <div class="tile" :style="`background: transparent url(${tile})`">
        <b-img fluid :src="icon"></b-img>
      </div>
    </b-row>
    <b-row class="card-title mx-0 mt-4">{{ title }}</b-row>
    <b-row class="card-description mx-0 mt-4">{{ description }}</b-row>
  </div>
</template>

<script>
export default {
  name: "CategoryCard",
  props: ["title", "description", "tile", "icon"],
};
</script>

<style scoped>
.card-container {
  width: 100%;
  padding: 40px;
  margin-top: 30px;
  border-radius: 20px;
}

.tile {
  width: 80px;
  height: 80px;
  display: flex;
  justify-content: center;
  align-items: center;
}

.card-title {
  font-size: 36px;
  font-weight: 500;
}

.card-description {
  font-size: 20px;
  color: var(--text-lighten1);
}
</style>