<template>
  <div>
    <div class="my_news-box">
        <img :src="source" :alt="title">
        <div class="my_news-info d-flex flex-column justify-content-evenly">
            <div class="d-flex">
                <span>{{ date }}</span>
                <span>by {{ author }}</span>
            </div>
            <h5 class="pb-3">{{ title }}</h5>
            <p>{{ details }}</p>
        </div>
    </div>
  </div>
</template>

<script>

export default {
    name: 'News',
    props: ['date', 'author', 'title', 'source', 'details'],
}
</script>

<style lang="scss">
@import "../style/variables.scss";
@import "../style/general.scss";

.my_news-box{
  position: relative;
  z-index: 1;
  border: 2px solid $darkBlueBg;

  & img{
    width: 100%;
    height: 100%;
  }
}

.my_news-info {
  position: absolute;
  bottom: -80px;
  right: 0px;
  background-color: $whiteText;
  width: 520px;
  padding: 30px 100px 30px 60px;

  & span{
    color: $fluoRed;
    font-size: 0.9em;
    padding: 0px 20px 5px 0px;
  }

  & h5{
    font-size: 1.4em;
  }

  & p{
    font-size: 0.9em;
    color: $greyText;
  }
}

</style>