<template>
    <div class="navi_inner">
        <div class="navi_btns">
            <router-link v-for="(store_gnb, index) in store_gnb" v-bind:to="store_gnb.to">{{store_gnb.name}}</router-link>
        </div>
    </div>
</template>

<script>
    import axios from 'axios'

    export default {
        name: "SubGnb",
        data(){
            return{
                store_gnb:[]
            }
        },
        mounted() {
            axios.get("/store_gnb.json").then((result) => {
                this.store_gnb = result.data;
            });
        },
    }
</script>

<style scoped>
    .navi_inner {position:relative; height:60px; background-color:rgba(45,45,45,0.88);}
    .navi_inner .navi_btns {height:60px; line-height:60px; margin:0 auto; font-size:0; text-align:left}
    .navi_inner .navi_btns a {position:relative; font-size:15px; color:#949494; margin:0 20px; display: inline-block; text-transform: uppercase; transition:color 0.3s;}
    .navi_inner .navi_btns a:after {content:""; position:absolute; bottom:17px; left:0; width:100%; height:1px; background-color:#bea36b; opacity:0;}
    .navi_inner .navi_btns a:first-child {margin-left:40px;}
    .navi_inner .navi_btns a:hover {color:#fff;}
    .navi_inner .navi_btns a.on {color:#fff;}
    .navi_inner .navi_btns a.on:after {opacity:1;}
</style>