<template>
    <h2>점포안내</h2>
</template>

<script>
   /* import {mapState} from 'vuex'

    export default {
        data() {
            return {
                largeName: "",
                smallName: ""
            };
        },
        watch: {
            menus() {
                this.init();
            }
        },
        mounted() {
            console.log("Location Mounted");
            this.init();
        },
        computed: {
            ...mapState(['menus'])
        },
        methods: {
            init() {
                for (let row of this.menus) {
                    if (row.idx == this.largeIdx) {
                        this.largeName = row.name;
                        for (let subRow of row.sub) {
                            if (subRow.idx == this.smallIdx) {
                                this.smallName = subRow.name;
                                break;
                            }
                        }
                        break;
                    }
                }
            }
        },
        props: {
            largeIdx: Number,
            smallIdx: Number
        }
    };*/
</script>

<style scoped>

</style>