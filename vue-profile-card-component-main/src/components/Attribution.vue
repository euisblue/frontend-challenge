<template>
    <div class="attribution">
      Challenge by <a href="https://www.frontendmentor.io?ref=challenge" target="_blank">Frontend Mentor</a>. 
      Coded by <a href="#">{{name}}</a>.
  </div>
</template>

<script>
export default {
  name: 'Attribution',
  props: {
    name: String,
  }
}
</script>

<style scoped>
.attribution { 
  font-size: 11px; 
  text-align: center; 
  margin-top: 3em;
}

.attribution a { 
  color: hsl(228, 45%, 44%);
}
</style>
