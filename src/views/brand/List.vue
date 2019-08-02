<template>
    <div class="contentsTypeA">
        <h2>쇼핑 정보</h2>
        <div id="snb">
            <ul>
                <li><a href="javascript:;">강남점</a></li>
                <li><a href="javascript:;">논현점</a></li>
                <li><a href="javascript:;">잠실점</a></li>
            </ul>
            <ul id="shoppingList">
                <li v-for="(eventList, index) in eventList">
                    <router-link v-bind:to="eventList.to">
                        <div class="imgArea">
                            <img
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
        name: "brand",
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
    .contentsWrap{position:relative; top:-156px}
    .contents{width:1280px; margin:0 auto;}
    .titleArea{display:table-cell; height:328px; width:1280px; background:#f6f6f6; vertical-align:middle; }
    h2{font-size:50px; font-weight:normal;}
</style>