<template>
  <div>

    <section class="jumbotron">
      <div class="container-fluid">
        <div class="row">
          <div class="col-12">
            <div class="my_jumbo-box d-flex flex-column justify-content-between">
              <div class="d-flex align-items-center">
                <div class="my_decoration-line"></div>
                <h6>Alwats the best way you need it</h6>
              </div>
              <h2>the best business consulting</h2>
              <div class="d-flex justify-content-start align-items-center pt-5">
                <button class="my_btn">read more</button>
                <a href="#"><i class="fas fa-play"></i></a>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>

    <section class="my_consulting pb-5 pt-5">

      <div class="d-flex justify-content-between align-items-center pb-5">
        <div class="my_consulting-title">
          <h5>our consultants can help you</h5>
        </div>
        <div class="my_decoration-line-md">
        </div>
      </div>

      <div class="container">     
        <div class="row">
          <div class="col-6" v-for="(consultant, index) in consultantData" :key="index">
            <Consultant :iconClass="consultant.iconClass" :name="consultant.name" :details="consultant.details"/>
          </div>
        </div>
      </div>

    </section>

    <section class="my_about-us pb-5">
      
      <div class="d-flex justify-content-between">
        <div class="my_about-img"><img src="../assets/img/business-people-working-together-on-project-and-5FHSKBL.jpg" alt=""></div>
        <div class="my_about-info d-flex flex-column">
        
          <div class="d-flex align-items-center">
            <div class="my_decoration-line">
            </div>
            <h6 class="pe-3 text-uppercase">About us</h6>
          </div>
          <h2>We make your strategy work</h2>
          <p>When, while lovely valley teems with vapour around meand eridian sun strikes the upper impenetrable foliage of my trees, and but a thousand unknown plants are noticed when i hear the buzz of the little world among the stalks, and grow familiar indescribable forms of the insect .and flies, then i feel the presence of the Almighty.</p>
        
        </div>
      </div>
      <div class="my_business-box">
        <div class="d-flex justify-content-evenly">
          <div class="my_business-title">
            <h3>We help to deliver the business case</h3>
          </div>
          <div class="my_business-info">
            <p>When, while lovely valley teems with vapour around meand meridian sun strikes the upper impenetrable foliage of my trees, and but a thousand unknown</p>
          </div>
        </div>
        <div class="d-flex justify-content-end">
            <button class="my_red-btn">get started</button>
        </div>
      </div>

    </section>

    <section class="my_projects pt-5">
      
      <div class="container">
        <div class="row">
          <div class="col-12">
            <div class="d-flex align-items-center">
              <div class="my_decoration-line"></div>
              <h6 class="pe-3 text-uppercase">project</h6>
            </div>
            
            <div class="my_project-title d-flex justify-content-between">
            
              <h3>our Experiment trusted consultants <br> help clients</h3>
              <div class="d-flex">
                <div class="my_arrow-box me-2">
                  <i class="fas fa-long-arrow-alt-left"></i>
                </div>
                <div class="my_arrow-box">
                  <i class="fas fa-long-arrow-alt-right"></i>
                </div>
              </div>
            </div>
          </div>
        </div>
        <div class="row">
          <div class="col-4">
            <div class="my_project-box">
              <img src="../assets/img/DRY-1-790x592.jpg" alt="DRY project img">
              <div class="my_project-info d-flex justify-content-between align-items-center">
                <div>
                  <h5>Purinky Products</h5>
                  <span>uncategorized</span>
                </div>
                <div>
                  <i class="fas fa-plus"></i>
                </div>
              </div>
            </div>
          </div>
          <div class="col-4">
            <div class="my_project-box">
              <img src="../assets/img/221bf0b7-8134-43bb-936a-5acbe42db64a-790x592.jpg" alt="DRY project img">
              <div class="my_project-info d-flex justify-content-between align-items-center">
                <div>
                  <h5>Purinky Products</h5>
                  <span>uncategorized</span>
                </div>
                <div>
                  <i class="fas fa-plus"></i>
                </div>
              </div>
            </div>
          </div>
          <div class="col-4">
            <div class="my_project-box">
              <img src="../assets/img/z1el4c4p-790x592.jpg" alt="DRY project img">
              <div class="my_project-info d-flex justify-content-between align-items-center">
                <div>
                  <h5>Purinky Products</h5>
                  <span>uncategorized</span>
                </div>
                <div>
                  <i class="fas fa-plus"></i>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>

    </section>

    <section class="my_customer-title pt-5 pb-3">
      <div class="container">
        <div class="row">
          <div class="col-12">
            <div class="d-flex justify-content-between align-items-center">
              <div class="flex-grow-1 text-center">
                <h6>Testimonial</h6>
              </div>
              <div class="my_decoration-line">
              </div>
            </div>
          </div>
          <div class="col-12">
            <h3 class="text-end"> What's the customer say <br> about our work</h3>
          </div>
        </div>
      </div>
    </section>

    <section class="my_customer mb-5">
      <div class="container">

        <div class="row">
          <div class="col-4" v-for="(customer, index) in customerData" :key="index">
            <Customer :info="customer.info" :name="customer.name" :company="customer.company" :portrait="customer.portrait"/>
          </div>
        </div>
      
      </div>
    </section>
      
    <section class="my_news pt-5 pb-5">
      <div class="container">
        <div class="row">
          <div class="col-12">
            <div class="d-flex align-items-center">
              <div class="my_decoration-line"></div>
              <h6>Blog</h6>
            </div>
          </div>
          <div class="col-12 mb-4">
            <div class="d-flex justify-content-between align-items-center">
              <h3>The recent news you must read it</h3>
              <button class="my_btn">view all</button>
            </div>
          </div>
        </div>
        <div class="row">
          <div class="col-6" v-for="(news, index) in newsData" :key="index">
            <News :source="news.source" :date="news.date" :author="news.author" :title="news.title" :details="news.details"/>
          </div>
        </div>
      </div>

    </section>

    <section class="my_work p-5">
      <div class="container">
        <div class="row">
          <div class="col-12 text-center">
            <h2>let's talk about work</h2>
          </div>
          <div class="col-12 text-center">
            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Nobis iste numquam nisi quaerat tenetur aperiam, nihil vero animi quo labore eos explicabo velit, voluptate dolore nesciunt facere consequuntur commodi tempora?</p>
          </div>
          <div class="col-12 text-center">
            <button class="my_dark-btn">Get Started</button>
          </div>
        </div>
      </div>
    </section>

  </div>
</template>

<script>
import Consultant from './Consultant.vue';
import consultantData from '../data/consultantData.js';
import Customer from './Customer.vue';
import customerData from '../data/customerData.js';
import News from './News.vue';
import newsData from '../data/newsData.js';

export default {
  name: 'Main',
  props: {
  },
  components: {
    Customer,
    Consultant,
    News,
  },
  data: function() {
    return {
      customerData,
      consultantData,
      newsData,
    }
  }
}
</script>

<style lang="scss">
@import "../style/variables.scss";
@import "../style/general.scss";

.jumbotron{
  background-image: url("../assets/img/portrait-of-young-architect-woman-on-meeting-KFZCE3A.jpg");
  background-repeat: no-repeat;
  background-position-x: right;
  background-position-y: 20% ;
  background-size: 65%;
}

.my_jumbo-box{
  margin: 12% 0px 0px 15%;
  padding-bottom: 150px;
  color: white;
  width: 500px;

  & h6{
    text-transform: uppercase;
    color: $darkerWhite;
  }

  & h2{
    font-weight: bold;
    font-size: 6em;
    text-transform: uppercase;
    line-height: 80px;
  }
}

.my_btn{
  text-transform: uppercase;
  font-size: 1.1em;
  letter-spacing: 2px;
  color: $darkBlueBg;
  padding: 17px 55px 17px 55px;
  background-color: $fluoGreen;
  border: 4px solid transparent;

  &:hover{
    background-color: $fluoRed;
    border: 4px solid $darkBlueBg;
    color: $whiteText;
  }
}

.my_dark-btn{
  text-transform: uppercase;
  font-size: 1.1em;
  letter-spacing: 2px;
  color: $whiteText;
  padding: 17px 55px 17px 55px;
  background-color: $darkBlueBg;
  border: 4px solid transparent;
  margin-bottom: 120px;

  &:hover{
    background-color: $fluoRed;
    border: 4px solid $darkBlueBg;
    color: $whiteText;
  }
}

.my_red-btn{
  text-transform: uppercase;
  font-size: 1.1em;
  letter-spacing: 2px;
  color: $whiteText;
  padding: 17px 55px 17px 55px;
  background-color: $fluoRed;
  border: 4px solid transparent;

  &:hover{
    background-color: $darkBlueBg;
    border: 4px solid $fluoGreen;
    color: $whiteText;
  }
}

.fas.fa-play {
  margin-left: 35px;
  color: $fluoGreen;
  padding: 15px 15px;
  border: 2px solid white;
  border-radius: 50%;
}

.my_decoration-line{
  height: 1px;
  width: 50px;
  border: 1px solid $darkerFluoGreen;
  margin-right: 20px;
}

.my_consulting{
    background-color: white;
}

.my_consulting-title{
  margin-left: 25%;
  margin-right: 50px;
  text-transform: uppercase;
  width: 650px;

  & h5{
    font-weight: 600;
    font-size: 1.2em;
  }
}

.my_decoration-line-md{
  height: 1px;
  width: 100%;
  border: 1.5px solid $darkerFluoGreen;
}


.my_about-us{
  color: white;
}

.my_about-info{

  padding: 300px 300px 0px 100px;

  & h6{
    color: $darkerWhite;
  }

  & h2{
    text-transform: uppercase;
    font-size: 4rem;
    font-weight: 600;
    padding-bottom: 50px;
  }

  & p{
    color: $greyText;
    width: 70%;
  }
}

.my_business-box{
  background-color: $darkerFluoGreen;
  width: 85%;
}

.link-element{
  padding: 17px 55px 17px 55px;
  background-color: $fluoRed;
  text-transform: uppercase;
  display: inline-block;
}

.my_business-title{
  width: 400px;
  padding: 100px 0px 50px 0px;
  color: $darkBlueBg;

  & h3{
    text-transform: uppercase;
    font-weight: 600;
    font-size: 2em;
  }
}

.my_business-info{
  width: 500px;
  padding: 100px 0px 50px 0px;
  
  & p{
    color: $greyBg;
    font-size: 1.1em;
  }
}

.my_projects{

  & h6{
    color: $darkerWhite;
  }

  & h3{
    text-transform: uppercase;
    color: $whiteText;
    font-weight: 600;
  }

  & img{
    width: 100%;
    height: 100%;
  }
}

.my_project-box{
  position: relative;
  margin: 30px 0px;
  border: 4px solid transparent;

  &:hover{
    border: 4px solid $darkBlueBg;
  }

  &:hover .my_project-info{
    opacity: 1;
  }

  &:hover img{
    filter: grayscale(100%) brightness(20%) sepia(100%) hue-rotate(-63deg) saturate(900%) contrast(1);;
  }
}

.my_project-info{
  position: absolute;
  bottom: 0;
  left: 0;
  padding: 20px;
  opacity: 0;

  & i{
    background-color: $darkBlueBg;
    padding: 20px;
    color: $whiteText;
    margin-left: 150px;
  }

  & h5{
    color: $whiteText;
    font-weight: bold;
    margin: 0;
  }

  & span{
    color: $darkerWhite;
  }
}

.my_arrow-box{
  height: 50px;
  width: 50px;
  background-color: $greyBg;
  padding: 10px 0px 5px 15px;
  font-size: 1.2em;
  color: $whiteText;
}

.my_customer-title{
  & h6{
     color: $darkerWhite;
     text-transform: uppercase;
  }

  & h3{
  text-transform: uppercase;
  color: $whiteText;
  font-weight: 600;
  }

  & .my_decoration-line{
    margin: 0px;
  }
}

.my_customer{
  background: linear-gradient(to left, white 85%, transparent 0);
}

.my_news {
  
  & h6{
    color: $darkerWhite;
    text-transform: uppercase;
    margin: 0px;
  }

  & h3{
  text-transform: uppercase;
  color: $whiteText;
  font-weight: 600;
  margin: 0px;
  }
}

.my_work{
  background-image: url('../assets/img/business-people-working-together-on-project-and-B3MZ4TX.jpg');
  background-size: cover;
  background-position: center;
  background-repeat: no-repeat;
  margin-top: 150px;

  & h2{
    text-transform: uppercase;
    color: $whiteText;
    font-size: 2.7em;
    padding-top: 120px;
  }

  & p {
    color: $darkerWhite;
    padding: 0px 200px 20px 200px;
  }
}


</style>
