<template>
  <div>
    <app-header v-bind:title="title"></app-header>
    <app-heroes v-bind:heroes="heroes"></app-heroes>
    <app-footer v-bind:title="title"></app-footer>
  </div>
</template>

<script>
import Header from "./components/Header.vue";
import Footer from "./components/Footer.vue";
import Heroes from "./components/Heroes.vue";

export default {
  //registering the component
  components: {
    "app-header": Header,
    "app-footer": Footer,
    "app-heroes": Heroes,
  },

  data() {
    return {
      heroes: [
        { name: "Ryu", specialty: "Karate kick", show: false },
        { name: "John", specialty: "Swords", show: false },
        { name: "Jones", specialty: "Flying", show: false },
        { name: "Clark", specialty: "Super Strength", show: false },
        { name: "Kent", specialty: "Heat Vision", show: false },
        { name: "Barry", specialty: "Super Speed", show: false },
      ],
      title: "Vue Heroes Are Here"
    };
  },
};
</script>

<style scoped>
/* h1{ */
/* color:purple; */

/* } */
</style>
