<template>
    <div id="STORE_COMMON_KEYVISUAL" class="gu_sub_kv">
        <bg />
        <div class="contentsWrap">
            <div class="contents">
                <subgnb />
                <div class="titleArea">
                    <pagetitle />
                </div>
            </div>
        </div>
    </div>
</template>

<script>
    import bg from '@/components/Bg.vue'
    import subgnb from '@/components/SubGnb.vue'
    import pagetitle from '@/components/Title.vue'

    export default {
        components: {
            bg,
            subgnb,
            pagetitle
        }
    }
</script>

<style scoped>
    .contentsWrap{position:relative; top:-156px}
    .contents{width:1280px; margin:0 auto;}
    .titleArea{display:table-cell; height:328px; width:1280px; background:#f6f6f6; vertical-align:middle; }
    h2{font-size:50px; font-weight:normal;}
</style>