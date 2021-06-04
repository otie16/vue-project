<template>
  <div>
    <app-header
      v-bind:title="title"
      v-on:changeTitle="updateTitle($event)"
    ></app-header>
    <app-heroes v-bind:heroes="heroes"></app-heroes>
    <app-footer v-bind:title="title"></app-footer>
    <form-helper>
      <div slot="form-header">
        <h3>This is the title of the form</h3>
        <p>Information about the form</p>
      </div>

      <div slot="form-fields">
        <input type="text" placeholder="name" required />
        <input type="password" placeholder="password" required />
      </div>

      <div slot="form-controls">
        <button @click="handleSubmit">Submit</button>
      </div>
    </form-helper>
  </div>
</template>

<script>
import Header from "./components/Header.vue";
import Footer from "./components/Footer.vue";
import Heroes from "./components/Heroes.vue";
import FormHelper from "./components/FormHelper.vue";

export default {
  //registering the component
  components: {
    "app-header": Header,
    "app-heroes": Heroes,
    "app-footer": Footer,
    "form-helper": FormHelper,
  },

  data() {
    return {
      a_title: "I am a dynamic slot",
      heroes: [
        { name: "Ryu", specialty: "Karate kick", show: false },
        { name: "John", specialty: "Swords", show: false },
        { name: "Jones", specialty: "Flying", show: false },
        { name: "Clark", specialty: "Super Strength", show: false },
        { name: "Kent", specialty: "Heat Vision", show: false },
        { name: "Barry", specialty: "Super Speed", show: false },
      ],
      title: "Vue Heroes Are Here",
    };
  },
  methods: {
    updateTitle(updatedTitle) {
      this.title = updatedTitle;
    },
  },
};
</script>

<style scoped>
</style>
