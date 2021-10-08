<template>
<!-- Footer section completely built up on bootstrap framework. It has two different zones:
    one with a list containing his relatives hyperlinks made by component, the other with final terms of usage
    and an 'absolute' positionated user-tool, made to allow chatting and navigation trought the page -->
  <div class="container">
    <div class="row">
      <div class="col-12 d-flex justify-content-between">
        <div class="my_footer-logo pt-5">
          <img src="../assets/img/logotype-2-300x50.png" alt="header logo image">
        </div>
        <div class="my_footer-nav pt-5">
          <ul>
            <li v-for="(item, index) in navBarItems" :key="index">
              <navItem :name="item.name" />
            </li>
          </ul>
        </div>
        <div class="my_footer-socials pt-5">
          <ul>
            <li><a href="#"><i class="fab fa-instagram"></i></a></li>
            <li><a href="#"><i class="fab fa-linkedin-in"></i></a></li>
            <li><a href="#"><i class="fab fa-facebook-f"></i></a></li>
            <li><a href="#"><i class="fab fa-twitter"></i></a></li>
          </ul>
        </div>
      </div>
      <div class="col-12">
        <hr class="my_divider mt-4 mb-3">
      </div>
      <div class="col-12 ">
        <div class="my_footer-end d-flex justify-content-between align-items-center pb-2">
          <div class="d-flex flex-column">
            <span>Terms of Use</span>
            <span>Privacy Environmental Policy</span>
          </div>
          <div class="d-flex justify-content-between align-items-baseline pb-2">
            <span>Copyright 2020 Phlox Consulting. All Rights Reserved.</span>
          </div>
          <div class="my_navigation-tool">
            <a href="#"><i class="fas fa-arrow-up ms-3"></i></a>
            <a href="#"><i class="far fa-comment ms-3"></i></a>
          </div>

        </div>
      </div>
    </div>
  
  </div>
</template>

<script>
import navItem from './navItem.vue';
import navBarItems from '../data/navBarItems.js';

export default {
    name : 'Footer',
    props : {
    },
    components: {
      navItem,
    },
    data: function(){
      return {
        navBarItems,
      }
    }
}
</script>

<style lang="scss">
@import "../style/variables.scss";
@import "../style/general.scss";

.my_divider{
  color: $darkerWhite;
}

.my_footer-logo{
  
  & img{
    height: 20px;
  }
}
.my_footer-nav{

  & ul {
  list-style-type: none;
  }

  & ul li{
  display: inline-block;
  }
 
  & ul li a{
  text-decoration: none;
  color: $greyText;
  font-size: 0.9em;
  padding-left: 20px;
    
    &:hover{
    color: $whiteText;
    }
  }
}

.my_footer-socials {

  & ul{
    list-style-type: none;
  }

  & ul li {
    display: inline;
  }

  & ul li a{
    text-decoration: none;
    color: $whiteText;
    padding-left: 15px;
  }
}

.my_footer-end{
  position: relative;
  color: $greyText;

  & span {
    font-size: 0.9em;
  }
}

.fa-arrow-up{
  color: $darkBlueBg;
  padding: 10px;
  background-color: $whiteText;
  border-radius: 50%;
  font-size: 0.5em;
}

.fa-comment{
  color: $whiteText;
  padding: 15px;
  background-color: $blueBg;
  border-radius: 50%;
  font-size: 1.5em;
  transform: scaleX(-1);
}

.my_navigation-tool{
  position: absolute;
  bottom: 15px;
  right: -110px;
}
</style>