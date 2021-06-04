<template>
  <div id="heroes">
    <ul>
      <li v-for="(hero, i) in heroes" :key="i" @click="hero.show = !hero.show">
        <h2>{{ hero.name }}</h2>
        <h3 v-show="hero.show">{{ hero.specialty }}</h3>
      </li>
    </ul>
    <button v-on:click="deleteHero">Delete Hero</button>
  </div>
</template>

<script>
export default {
  //props
  props: {
    heroes: {
      type: String
    }
  },
  data() {
    return {};
  },

  methods: {
deleteHero () {
  this.heroes.pop()
}
  },
  //lifecycle hooks
  beforeCreate() {
    alert('beforeCreate');
  },
//can be used to fetch data from the db
  created(){
    alert('created');
  },

  beforeMount(){
    alert('beforeMount');
  },

  mounted() {
    alert('mounted');
  },
beforeUpdate() {
  alert('beforeUpdate');
},
updated(){
  alert('updated');
}

};
</script>

<style scoped>
#heroes {
  width: 100%;
  max-width: 1200px;
  margin: 40px auto;
  padding: 0 20px;
  box-sizing: border-box;
}

ul {
  display: flex;
  flex-wrap: wrap;
  list-style-type: none;
  padding: 0;
}

li {
  flex-grow: 1;
  flex-basis: 300px;
  text-align: center;
  padding: 30px;
  box-shadow: 2px 2px 5px rgb(152, 154, 243);
  /* border: 1px solid #222; */
  margin: 10px;
}
</style>
 