<template>
    <div class="box">
        <my-heared></my-heared>
        <div class="new-heared">
            <div class="new-body">
                <h1><router-link to="/newnext">乔雅登中国上市 北京叶子荣获首批授权单位</router-link> </h1>
                <p>12 月8日，美国艾尔建公司乔雅登(Juvederm)系列玻尿酸正式进入中国大<br>陆市场，自乔雅登上市以来，先后获得欧洲CE、美国FDA、中国CFDA等各<br>国药监局严格认证...</p>
            </div>
            <div class="new-body">
                <h1>国际整形与再生外科协会第四届全球学术交流会议</h1>
                <p>2015年12月4日—6日，国际整形与再生外科协会第四届全球学术交流会议<br>在北京国际会议中心隆重举行，集结了世界各地的66名国外学者和四百余位<br>国内整形外科医生参会，共有6场精彩的手术演示...</p>
            </div>
            <div class="new-body">
                <h1>全国形体雕塑与脂肪移植技术研讨会在北京叶子隆重召开 </h1>
                <p>　近年来，形体雕塑与自体脂肪移植日益受到广大求美者的青睐，然而在<br>快速发展的浪潮下，诸如乳房肿块、钙化、双目失明甚至死亡的案例却也时有<br>发生。为提高业内医生脂肪移植临床技术水平，培养行业精英...</p>
            </div>
            <div class="new-body">
                <h1>北京叶子荣获“2014中国优秀企业公民”称号 </h1>
                <p>　2015年1月16日，北京叶子整形美容医院荣获，由CCTV-发现之旅《公<br>益的力量》栏目颁发的“2014中国优秀企业公民”荣誉称号。发布会在北<br>京钓鱼台国宾馆隆重举行...</p>
            </div>
            <div class="new-body">
                <h1>北京叶子刘明星主任做客人民网谈冬季如何美肤护肤 </h1>
                <p>随着冬季的到来，天气寒冷干燥，加上空气污染严重，肌肤表面很容易出现<br>各种问题，给爱美人士增添了许多烦恼，那么应该怎样更好地认识自己的肌<br>肤状态，并制定冬季美肤策略呢...</p>
            </div>
            <div class="new-body">
                <h1>叶子作为整行业代表光荣载入《历史上的卫生部》史册 </h1>
                <p>2014年9月，北京叶子被载入中国医疗美容史册，成为国内唯一一家载入中<br>国医疗美容史册的整形医院，这不仅仅是一种行业认可，更是对北京叶子的<br>最高礼赞...</p>
            </div>
        </div>
        <my-footer></my-footer>
    </div>
    
</template>

<script>
    import MyFooter from '@/components/footer'
    import MyHeared from '@/components/heared'
    export default {
        components: {MyFooter,MyHeared},
    }
</script>

<style lang="css" scoped>
    .box { margin-bottom: 115px; width: 100%; }
    h1, p { margin: 0; }
    a { color: #aa854f; }
    .new-heared { margin: 10px 10px 0; padding-bottom: 60px; background-color: #ffffff; }
    .new-body { padding: 60px 0 0 35px; }
    .new-body>h1 { font-weight: normal; font-size: 24px; color: #aa854f; padding-bottom: 20px; } 
    .new-body>p { font-size: 18px; color: #888888; } 

</style>