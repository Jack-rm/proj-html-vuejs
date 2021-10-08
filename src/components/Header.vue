<template>

    <!-- Component thought to re-create the header section, it has his own scss values cause of the 'fixed' position.
        It has been made fully transparent according to design project with his relative logo image inside-->
  <div class="container">
    <div class="row">
        <div class="col-12 d-flex justify-content-between">
            <div class="my_logo-box">
                <img src="../assets/img/logotype.png" alt="Header main red logo">
            </div>
            <div class="my_nav-bar">
                <ul>
                    <li v-for="(item, index) in headerNavItems" :key="index"><a href="#">{{ item.name.toUpperCase() }}</a></li>
                </ul>
            </div>
        </div>
    </div>
  </div>
</template>

<script>
// Datas of this component are not extracted from a different file, but built inside of it.
// Made as a first attempt, this decision seams food according to the peculiare structure and features of the Header itself 

export default {
    name: 'Header',
    props: {

    },
    data: function() {
        return{
            
            headerLogo: [
                {
                    source: require('../assets/img/logotype.png'),
                    alt: 'Header main red logo',
                }
            ],
            headerNavItems: [
                {
                    name: 'Home',
                },
                {
                    name: 'About',
                },
                {
                    name: 'Projects',
                },
                {
                    name: 'Services',
                },
                {
                    name: 'Blog',
                },
                {
                    name: 'Contact',
                },
            ],
        }
    },
}
</script>

<style lang="scss" scoped>
@import "../style/variables.scss";
@import "../style/general.scss";

.container{
    background-color: transparent !important;
    position: fixed;
    left: 50%;
    transform: translateX(-50%);
    z-index: 2;
}

.my_logo-box{
    padding-top: 20px;
    padding-bottom: 20px;
    
    & img{
    height: 20px;
    }
}


.my_nav-bar{
    padding-top: 20px;

    & ul {
    list-style-type: none;
    }

    & ul li {
    border-top: 3px solid transparent;
    display: inline;
    padding-top: 20px;
    margin-left: 20px;

        &:hover{
        border-top: 3px solid $whiteText;
        }
    }
    
    & ul li a{
    text-decoration: none;
    color: $darkerWhite;
        
        &:hover{
            color: $whiteText;
        }
    }
}


</style>