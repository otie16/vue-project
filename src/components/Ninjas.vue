<template>
  <div id= "ninjas">
    <ul>
      <li v-for="(hero, i) in heroes" :key="i" @click = "hero.show = !hero.show">
        <h2>{{ hero.name }}</h2>
        <h3 v-show="hero.show">{{ hero.specialty }}</h3>
        </li>
    </ul>
  </div>
</template>

<script>
export default {
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
    };
  },
};
</script>

<style scoped>
#ninjas{
width: 100%;
max-width: 1200px;
margin: 40px auto;
padding:0 20px;
box-sizing: border-box;
}

ul{
  display: flex;
  flex-wrap: wrap;
  list-style-type: none;
  padding: 0;
}

li{
  flex-grow: 1;
  flex-basis: 300px;
  text-align: center;
  padding: 30px;
  border: 1px solid #222;
  margin: 10px;
}
</style>
