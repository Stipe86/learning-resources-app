<template>
  <ul>
    <learning-resource
      v-for="res in resources"
      :key="res.id"
      :title="res.title"
      :description="res.description"
      :link="res.link"
      @deleteResource="deleteResource(res.id)"
    ></learning-resource>
  </ul>
</template>

<script>
import LearningResource from "./LearningResource.vue";

export default {
  components: {
    LearningResource,
  },

  inject: ["resources"],

  methods: {
    // deleteResource(resId) {
    //   this.resources = this.resources.filter((res) => res.id !== resId);
    //   console.log(this.resources.length);
    // },

    deleteResource(resId) {
      const resIndex = this.resources.findIndex((res) => res.id === resId);
      this.resources.splice(resIndex, 1);
    },
  },
};
</script>

<style scoped>
ul {
  list-style: none;
  margin: 0;
  padding: 0;
  margin: auto;
  max-width: 40rem;
}
</style>
