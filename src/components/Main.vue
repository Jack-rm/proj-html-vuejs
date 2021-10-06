<template>
  <div>

    <h2>{{ msg }}</h2> 

  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  }
}
</script>

<style lang="scss">
@import "../style/variables.scss";
@import "../style/general.scss";


</style>
