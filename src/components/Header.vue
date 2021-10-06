<template>
  <div class="container-fluid">
    <div class="row">
        <div class="col-12 d-flex justify-content-between">
            <img src="../assets/img/logotype.png" alt="Header main red logo">
            <ul>
                <li v-for="(item, index) in headerNavItems" :key="index">{{ item.name }}</li>
            </ul>
        </div>
    </div>
  </div>
</template>

<script>
export default {
    name: 'Header',
    props: {

    },
    data: function() {
        return{
            
            headerLogo: [
                {
                    source: "../assets/img/logotype.png",
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

<style lang="scss">
@import "../style/variables.scss";
@import "../style/general.scss";

ul li {
    list-style-type: none;
    display: inline-block;
}
</style>