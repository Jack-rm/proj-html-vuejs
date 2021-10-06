<template>
  <div>

  <section class="jumbotron">
    <div class="container-fluid">
      <div class="row">
        <div class="col-12">
          <p>scritte</p>
        </div>
      </div>
    </div>
  </section>
  <section>
    <p>ciao</p>
  </section>

  </div>
</template>

<script>
export default {
  name: 'Main',
  props: {

  }
}
</script>

<style lang="scss">
@import "../style/variables.scss";
@import "../style/general.scss";

.jumbotron{
  background-color: $darkBlueBg;
  background-image: url("../assets/img/portrait-of-young-architect-woman-on-meeting-KFZCE3A.jpg");
  background-repeat: no-repeat;
  background-position-x: right;
  background-position-y: 20% ;
  background-size: 65%;
  height: 100vh;
}


</style>
