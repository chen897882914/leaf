<template>
    <div class="box">
        <my-heared></my-heared>
        <div class="headline">
            <div class="bor-bot">
                <ul class="title-bar">
                    <li>乔雅登中国上市</li>
                    <li>北京叶子荣获首批授权单位</li>
                </ul>
                <ul class="read-day">
                    <li>2015-12-09</li>
                    <li>阅读 1176</li>
                </ul>
            </div>
            <div class="center-pad">
                <div class="new-put">
                    <img src="../../public/img/new-1.jpg">
                </div>
                <div class="new-tell">
                    <p>12月8日，美国艾尔建公司乔雅登(Juvederm)系列玻尿酸正式进入中国大陆市场，自乔雅登上市以来，先后获得欧洲CE、美国FDA、中国CFDA等各国药监局严格认证，在全球100多个国家临床使用中，累计销量超过2700万支，是目前国内唯一CFDA认证的超过一年以上的玻尿酸。</p>
                </div>
                <div class="new-put">
                    <img src="../../public/img/new-2.jpg">
                </div>
                <div class="new-tell">
                    <p>乔雅登与其他玻尿酸的最大不同在于构造。乔雅登是黏稠的流体、浓度较高，疼痛较低、且容易塑形与固定形态、触感柔软与组织更容易融合、维持时间较长等，注射后皮肤丰满，面部皱纹被抚平，脸颊呈现苹果般的曲线，让爱美人士拥有完美面部轮廓，青春再现。</p>
                </div>
                <div class="new-tell">
                    <p>北京叶子为艾尔建公司长期合作伙伴和指定的注射机构。本次，北京叶子为艾尔建公司在北京地区首批授权指定注射机构，同时我院业务院长鲁礼新、注射医生汪环受邀参加了乔雅登首次注射医师的授证培训。</p>
                </div>
                <div class="new-tell">
                    <p>北京叶子整形美容医院一直坚持引进国际上先进的医学美容理念，致力于把先进的整形美容产品带给广大的爱美人士，帮助每一位爱美者升级美丽。</p>
                </div>
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
    .box { width: 100%; margin-bottom: 115px; }
    img { width: 100%; }
    
    .headline { margin: 10px 10px 0; background-color: #ffffff; }
    .bor-bot { margin: 0 35px; border-bottom: 1px solid #efefef; }
    .title-bar { font-size: 32px; color: #aa854f; padding-top: 60px; }
    .read-day { font-size: 18px; color: #888888; padding: 20px 0; }
    .read-day>li:nth-child(1) { float: left; padding-right: 40px; }
    .center-pad { padding: 30px 0 60px; }
    .new-put { width: 100%; padding: 30px 35px 0; }
    .new-tell { padding: 30px 35px 0; }
    .new-tell p { margin: 0; font-size: 24px; color: #888888; text-indent: 48px; }
    .new-tell p::first-letter { font-size: 32px; }
</style>