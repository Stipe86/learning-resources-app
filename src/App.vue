<template>
  <the-header title="RememberMe"></the-header>
  <!-- <add-resources></add-resources> -->
  <the-resources></the-resources>
  <!-- <stored-resources :resources="storedResources"></stored-resources> -->
</template>

<script>
import TheResources from "./components/learning-resources/TheResources.vue";
// import StoredResources from "./components/learning-resources/StoredResources.vue";
// import AddResources from "./components/learning-resources/AddResource.vue";
import TheHeader from "./components/layouts/TheHeader.vue";
export default {
  name: "App",
  components: {
    // StoredResources,
    TheHeader,
    TheResources,
    // AddResources,
  },
  // data() {
  //   return {
  //     storedResources: [
  //       {
  //         id: "official-guide",
  //         title: "Official Guide",
  //         description: "The official Vue.js documentation",
  //         link: "https://vuejs.org",
  //       },
  //       {
  //         id: "google",
  //         title: "Google",
  //         description: "Learn to google...",
  //         link: "https://google.org",
  //       },
  //     ],
  //   };
  // },
};
</script>

<style>
@import url("https://fonts.googleapis.com/css2?family=Roboto:wght@400;700&display=swap");

* {
  box-sizing: border-box;
}

html {
  font-family: "Roboto", sans-serif;
}

body {
  margin: 0;
}
</style>
