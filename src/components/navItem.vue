<template>
  <div>
      <a href="#">{{ name.toUpperCase() }}</a>
  </div>
</template>

<script>
export default {
    name: 'navItem',
    props: ['name']
}
</script>

<style lang="scss">
@import "../style/variables.scss";
@import "../style/general.scss";

</style>
    