<template>
  <div>
    <div class="my_customer-box">
        <img :src="portrait" :alt="name">
        <div class="my_customer-info">
            <p>{{ info }}</p>
            <h4>{{ name }}</h4>
            <span>{{ company }}</span>
        </div>
    </div>
  </div>
</template>

<script>

export default {
  name: 'Customer',
  props: ['name', 'company', 'info', 'portrait']
}
</script>

<style lang="scss">
@import "../style/variables.scss";
@import "../style/general.scss";

.my_customer-box{
  position: relative;
  border-top: 2px solid transparent;
  border-bottom: 2px solid transparent;
  border-right: 6px solid transparent;
  border-left: 6px solid transparent;


  & img{
    height: 100%;
    width: 100%;
    opacity: 0;
  }

  &:hover img{
    opacity: 1;
  }
  &:hover {
    border-bottom: 2px solid $darkBlueBg;
    border-top: 2px solid $darkBlueBg;
    border-left: 6px solid $darkBlueBg;
    border-right: 6px solid $darkBlueBg;
  }

  &:hover .my_customer-info{
    & p, span{
      color: $darkerWhite;
    }
    & h4{
      color: $whiteText;
    }
  }
}

.my_customer-info {
  position: absolute;
  top: 0;
  left: 0;
  padding: 30px;

  & p{
    padding-bottom: 40px;
    color: $greyText;
  }

  & h4{
    font-weight: 600;
  }

  & span{
    color: $greyText;
  }
}

.my_customer-info:hover .my_customer-box img{
  opacity: 1;
}
</style>