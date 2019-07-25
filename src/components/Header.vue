<template>
    <div id="header">
        <h1>
            <router-link to="/"><img src="https://www.shinsegae.com/resources/site/img/common/gnb/gnb_logo.png" alt="SHINSEGAE"></router-link>
        </h1>
        <ul>
            <li v-for="(gnb, index) in gnb">
                <router-link v-bind:to="gnb.to">{{gnb.name}}</router-link>
            </li>
        </ul>
    </div>
</template>

<script>
    import axios from 'axios'

    export default {
        name: "Header",
        data(){
            return {
                gnb:[]
            }
        },
        mounted() {
            axios.get("/gnb.json").then((result) => {
                this.gnb = result.data;
            });
        }
    }
</script>

<style scoped>
    #header{position:relative; border-bottom:1px solid #dedede; text-align:center; height:70px; line-height:70px; min-width:1120px}
    #header h1{position:absolute; left:50px; top:50%; transform:translateY(-50%); line-height:normal}
    #header h1 a{display:block; line-height:23px}
    #header ul li{display:inline-block; margin:0 10px}
    #header ul li a {font-size: 14px; color: #444444;}
</style>