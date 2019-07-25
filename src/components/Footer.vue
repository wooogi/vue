<template>
    <div id="footer">
        <div class="section">
            <h2><img src="https://www.shinsegae.com/resources/site/img/common/footer/logo.png" alt="SHINSEGAE"></h2>
            <ul class="footMenu">
                <li><a href="javascript:;">회사소개 </a></li>
                <li><a href="javascript:;">법인영업 </a></li>
                <li><a href="javascript:;">백화점 </a></li>
                <li><a href="javascript:;">신문고 </a></li>
                <li class="last"><a href="javascript:;">사이트맵</a></li>

                <li><a href="javascript:;">개인정보처리방침</a></li>
                <li><a href="javascript:;">영상정보처리기기 </a></li>
                <li><a href="javascript:;">운영·관리방침 </a></li>
                <li><a href="javascript:;">이용약관 </a></li>
                <li><a href="javascript:;">신세계포인트 </a></li>
                <li><a href="javascript:;">이용약관</a></li>
            </ul>
            <div class="sns">
                <a href="https://shinsegaeblog.com" target="_blank" rel="noopener noreferrer" class="blog" title="새 창">신세계백화점 블로그 바로가기</a>
                <a href="https://web.facebook.com/shinsegae.dep?fref=ts&amp;_rdc=1&amp;_rdr" target="_blank" rel="noopener noreferrer" class="facebook" title="새 창">신세계백화점 페이스북 바로가기</a>
                <a href="https://www.instagram.com/only_shinsegae/" target="_blank" rel="noopener noreferrer" class="insta" title="새 창">신세계백화점 인스타그램 바로가기</a>
                <a href="http://www.youtube.com/user/ShinsegaeDep" target="_blank" rel="noopener noreferrer" class="youtube" title="새 창">신세계백화점 유튜브 바로가기</a>
                <a href="javaScript:sbotOpen();" target="_blank" rel="noopener noreferrer" class="sbot" title="새 창">신세계백화점 sbot 바로가기</a>
            </div>
        </div>
        <div class="bottom">
            <span class="info kr_g_600">(주)신세계 대표이사 : 장재영  |  주소 : 서울특별시 중구 소공로 63(충무로 1가)  |  개인정보관리책임자 : 이성환 담당  |  대표전화 : 1588-1234</span>
            <span class="copyright en_gill_400">COPYRIGHT © 2019 SHINSEGAE. ALL<br> RIGHTS RESERVED.</span>
        </div>
    </div>
</template>

<script>
    export default {
        name: "foot"
    }
</script>

<style scoped>
    #footer {position:relative; width:100%; background-color:#232323; color:#fff; padding:50px 0 56px;}
    #footer .top {padding-bottom:50px;}
    #footer .top > div {display: inline-block; font-size:0; vertical-align: top;}
    #footer .top .logo {margin-right:38px;}
    #footer .top .btns_another {color:#949494; font-size:14px; width:58%;}
    #footer .top .btns_another a {display: inline-block; padding:0 12px; margin-bottom:20px;transition: all .2s;}
    #footer .top .btns_another a:hover {color:#fff;}
    #footer .top .btns_sns_family {float:right;}
    #footer .top .btns_sns_family > div {display: inline-block; vertical-align: top;}
    #footer .top .btns_sns_family .family { position: relative;width:160px; text-align: center; margin-top: -10px; z-index: 11;}
    #footer .top .btns_sns_family .family .depth1 {font-size:12px; color:#999999; display: inline-block; line-height:1;border:1px solid transparent; padding: 8px 0;box-sizing:border-box;width:100%; transition:all .2s ease-in-out;}
    #footer .top .btns_sns_family .family .depth1:after {content:""; width:123px; height:100%; border-bottom:1px solid #828282; display: block; position: absolute;bottom:0;left:50%;box-sizing:border-box;transition:all .1s;
        transform:translateX(-50%);
        -ms-transform:translateX(-50%);
        -moz-transform:translateX(-50%);
        -webkit-transform:translateX(-50%);
        -o-transform:translateX(-50%);}
    #footer .top .btns_sns_family .family .depth1:before {content:""; width:100%; height:0; display: block; position: absolute;bottom:1px;left:50%;box-sizing:border-box;transition:all .1s ease-in-out;
        transform:translateX(-50%);
        -ms-transform:translateX(-50%);
        -moz-transform:translateX(-50%);
        -webkit-transform:translateX(-50%);
        -o-transform:translateX(-50%);}
    #footer .top .btns_sns_family .family .depth1.on:after {content:'';width:100%;}
    #footer .top .btns_sns_family .family .depth1.on:before {content:'';height:100%;border-left:1px solid #828282;border-right:1px solid #828282;transition-delay:.1s;}
    #footer .top .btns_sns_family .family .depth1.on:hover {background:#323232;color:#fff;transition:all .1s ease-in-out;}
    #footer .top .btns_sns_family .family .depth1 img {vertical-align: middle; margin-left:36px;transition:all .2s ease-in-out;}
    #footer .top .btns_sns_family .family .depth1.on img {transform:rotate(180deg);-ms-transform:rotate(180deg);transition:all .2s ease-in-out;}
    #footer .top .btns_sns_family .family ul {top:inherit;bottom:32px;left:0;width:100%;border:1px solid #828282;color:#949494; font-size: 12px; position: absolute;background:#232323; box-sizing: border-box; display: none; text-align: left;}
    #footer .top .btns_sns_family .family ul.on { display: block
    ;}
    #footer .top .btns_sns_family .family ul li a { display: inline-block; width: 100%; padding: 10px 20px;box-sizing: border-box;transition:all .2s;}
    #footer .top .btns_sns_family .family ul li a:hover {color:#fff;background:#323232;transition:all .2s;}
    #footer .top .btns_sns_family .sns {margin-left:30px;}
    .sns{text-align:left}
    .sns a {display: inline-block; font-size:0; vertical-align: top; margin:0 10px;}
    .sns a:last-child {margin-right:0; margin-left: 14px;}
    .sns a:before {transition: all .2s;}
    .footMenu{text-align:left}
    #footer{min-width:1120px; }
    #footer .bottom{text-align:left;}
    #footer .sns{position:absolute; right:0px; top:0px}
    #footer .bottom span {font-size:12px; color:#8A8A8A;}
    #footer .bottom .copyright {margin-left:1%;letter-spacing: 1px}
    #footer .bottom .ico_wa {position:absolute; top:20px; right:0; opacity:0.6;}
    #footer .section{position:relative; width:1120px; margin:0 auto; box-sizing: border-box; padding-left:210px; padding-right:210px; padding-bottom:70px}
    #footer h2{position:absolute; left:0; top:0}
    #footer .footMenu li{display:inline-block; margin-right:20px; margin-bottom:15px}
    #footer .footMenu li a{font-size: 14px; color:#949494}
    #footer .bottom{width:1120px; margin:0 auto; padding-top:30px; border-top:1px solid #313131}
</style>