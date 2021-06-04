<template>
  <div>
    <h1>Please fill out our form...</h1>
    <form>
      <div id="form-header">
        < name="for-header"></<!--  -->slot>
./
      </div>
      <div id="form-fields">
        <slot name="form-fields"></slot>
      </div>
      <div id="form-controls">
        <slot name="form-controls"></slot>
      </div>
      <div id="useful-links">
        <slot name="useful-links"></slot>
      </div>
      <ul>
        <li><a href="#">Link 1</a></li>
        <li><a href="#">Link 2</a></li>
        <li><a href="#">Link 3</a></li>
        <li><a href="#">Link 4</a></li>
      </ul>
    </form>
  </div>
</template>

<script>
export default {};
</script>

<style>
</style>