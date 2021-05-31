<template>
  <footer>
      <p>{{ copyright }}</p>
  </footer>
</template>

<script>


export default {
  //registering the component
 

  data() {
    return {
        copyright: 'Copyright 2021 Vue Learn'
    }
  },
};
</script>

<style scoped>
footer{
    background:#222;
    padding:60px
}
p{
    color: lightgreen;
    text-align: center;
}
</style>
