<template>
    <div id="container" class="main">
        <div id="top">
            <video class="video-1" style="-webkit-transform: translate(-50%, -50%);-moz-transform: translate(-50%, -50%);-ms-transform: translate(-50%, -50%);-o-transform: translate(-50%, -50%);transform: translate(-50%, -50%);position:absolute;top:50%;left:50%;min-width:100%;min-height:100%;height:auto;" autoplay="" loop="" muted=""><source src="https://www.cjlogistics.com/static/pc/global/template/video/main_1122.mp4" type="video/mp4"></video>
        </div>
        <div id="mainConte">
            <h2>Shopping News &amp; Event</h2>
            <div class="copy">
                <span class="info">
                    <span>잠깐!</span> 지금 로그인 하시고 고객님의 구매 패턴, 취향에 기반한 쇼핑 정보를 만나보세요.
                </span>
            </div>
            <ul class="eventList">
                <li v-for="(eventList, index) in eventList">
                    <router-link v-bind:to="eventList.to">
                        <div class="imgArea">

                        </div>
                        <div class="topInfo">
                            <span>{{eventList.brand}}</span> | <span>{{eventList.store}}</span>
                        </div>
                        <strong>{{eventList.title}}</strong>
                        <div class="fotInfo">
                            <span>{{eventList.data}}</span> | <span>{{eventList.address}}</span>
                        </div>
                    </router-link>
                </li>
            </ul>
        </div>
    </div>
</template>

<script>
    import axios from 'axios'

    export default {
        name: "Main",
        data(){
            return {
                eventList:[]
            }
        },
        mounted() {
            axios.get("/main_list.json").then((result) => {
                this.eventList = result.data;
            });
        }
    }
</script>

<style scoped>
    .main img{width:100%}
    #top{background:#999; position:relative; overflow:hidden; min-height: 850px;}
    #top:after{content:''; position:absolute; left:0px; top:0px; width:100%; height:100%; background:rgba(0,0,0,0.6); }
    #mainConte{width:1280px; margin:0 auto; padding-top:180px; }
    #mainConte h2{font-size:60px; font-weight:normal; color:##232323}
    .copy{text-align:center; margin-top:50px}
    .copy .info{display: inline-block; margin-left: 5px; font-size: 16px; color: #666666;}
    .copy .info span{color: #222; font-size: 17px;}
    .eventList{margin-top:50px; text-align:center;}
    .eventList li{display:inline-block; width:31%; margin-bottom:30px; margin-left:3%; border:1px solid #8A8A8A}
    .eventList li:nth-child(3n+1){margin-left:0}

</style>