<template>
  <div>
    <div class="my_consulting-box d-flex justify-content-between align-items-top pe-5 pt-5 pb-5">
        <div class="my_consulting-icon">
            <i class="my_red-icon me-5" :class="iconClass"></i>
        </div>
        <div class="my_consulting-info">
            <h6>{{ name }}</h6>
            <p>{{ details }}</p>
        </div>
    </div>
  </div>
</template>

<script>
export default {
    name: 'Consultant',
    props: ['iconClass', 'name', 'details']
}
</script>

<style lang="scss">
@import "../style/variables.scss";
@import "../style/general.scss";

.my_consulting-box{
    width: 85%;
}
.my_consulting-info{

  & h6{
    font-weight: 600;
    text-transform: uppercase;
    font-size: 1.1em;
  }

  & p{
    color: $greyText; 
  }
}

.my_red-icon{
  padding: 15px 15px;
  background-color: $fluoRed;
  color: white;
  font-size: 1.5em;
  border-radius: 50%;
}
</style>