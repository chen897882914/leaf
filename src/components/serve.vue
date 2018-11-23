<template>
    <div class="box">
        <div class="project" :style="{height:projectHeight + 'px'}">
            <div class="project-bg">
                <div class="one-level">
                    <ul class="one-level-ul">
                        <li v-for="(item, index) in left" :class="[index == present ? 'present' : '' ]" @click="clickTwo(index)">{{item}}</li>
                    </ul>
                </div>
                <div class="two-level">
                    <div  v-for="(menu, index) in leftservice" v-show="index == present">
                        <ul class="multi-ul" v-if="checkLevel(menu) == true">
                            <template v-for="(sub, subindex) in menu">
                                <li class="title"><span>{{sub.name}}</span></li>
                                <li class="sub" v-for="(g, gidx) in sub.child">{{g.name}}</li>
                            </template>
                        </ul>
                        <ul class="the-service-items" v-else>
                            <li v-for="(sub, subindex) in menu">{{sub.name}}</li>
                        </ul>
                    </div>
                    
<!--
                    <ul class="the-service-items" v-for="(item, index) in leftservice" v-show="index == present">
                        <li v-for="(sub, subindex) in leftservice[index]">{{sub.name}}</li>
                        <li>开眼角</li>
                        <li>祛眼袋</li>
                        <li>重睑修复</li>
                        <li>眼袋修复</li>
                        <li>眼周年轻化</li>
                        <li>上眼窝凹陷</li>
                        <li>上睑下垂矫正</li>
                    </ul>
-->
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    data () {
        return {
            bodyHeight: 0,
            hearedHeight: 0,
            footerHeight: 0,
            projectHeight: 0,
            left: ['眼部整形','鼻部整形','胸部整形','微整形','面部精雕','抗衰除皱','身体塑型','皮肤美容','艺术纹绣','牙齿美容','毛发种植','私密整形','无痛脱毛','其它整形','修复中心',],
            present: 0,
            leftservice: [
                [
                    {name:'双眼皮'},{name:'开眼角'},{name:'祛眼袋'},{name:'重睑修复'},{name:'眼袋修复'},{name:'眼周年轻化'},{name:'上眼窝凹陷'},{name:'上睑下垂矫正'}
                ],
                [
                    {name:'111'},{name:'222'}, {name:'333'}, {name:'444'}, {name:'555'}
                ],
                [
                    {
                        name: '面部年轻化',
                        child: [
                            {name: '额纹'},
                            {name: '眉间纹'},
                            {name: '鱼尾纹'},
                            {name: '鼻背纹'},
                            {name: '法令纹'},
                            {name: '嘴角纹'},
                            {name: '口角提升'},
                            {name: '下颌缘提升'}
                        ]
                    },
                    {
                        name: '面部轮廓精雕',
                        child: [
                            {name: '丰额头'},
                            {name: '太阳穴'},
                            {name: '丰眉弓'},
                            {name: '注射隆鼻'},
                            {name: '丰面颊'},
                            {name: '丰唇'},
                            {name: '丰耳垂'},
                            {name: '丰下巴'},
                        ]
                    },
                    {
                        name: '形体轮廓紧致',
                        child: [
                            {name: '瘦脸'},
                            {name: '瘦小腿'},
                            {name: '颏肌'},
                        ]
                    }
                ]
            ],
        }
    },
    mounted () {
        this.bodyHeight = document.documentElement.clientHeight
        this.hearedHeight = document.querySelector('.heared-lo').clientHeight
        this.footerHeight = document.querySelector('.relation-me').clientHeight
        this.projectHeight = this.bodyHeight - this.hearedHeight - this.footerHeight - 10
    },
    methods: {
        clickTwo:function (index){
            this.present = index
        },
        checkLevel: function(item){
            let res = false;
            for(let i=0; i<item.length; i++){
                const sub = item[i]; 
                if(sub.child){
                    res = true;
                    break;
                }
            }
            return res;
        }
    }
}
</script>

<style lang="css" scoped>
    .box { background-color: #efefef; margin: 98px 0 0; padding: 10px 10px; position: absolute; left: 0; top: 0; width: 100%; z-index: 30; }
    .project {  width: 100%; border-bottom: 10px solid #efefef;  overflow: auto; }
    .project-bg { display: flex; background-color: #ffffff; }
    .one-level { padding: 10px 0; width: 190px; }
    .one-level-ul>li { padding: 10px 30px; font-size: 28px; color: #888888; background-color: #e5daca; }
    .one-level-ul>li.present { background-color: #ffffff; color: #aa854f; border-bottom: 2px solid #aa854f; }
    .two-level { flex: 1; padding: 20px; }
    .the-service-items { font-size: 24px; color: #888888; text-align: center; border-collapse: collapse; float: left; width: 100%; border-top: 1px solid #888888; border-left: 1px solid #888888; }
    .the-service-items>li { float: left; border-right: 1px solid #888888; border-bottom: 1px solid #888888; width: 50%; padding: 20px 0; }
    .multi-ul { float: left; width: 100%; border-left:1px solid #888888; }
    .multi-ul>li:first-child span { padding-top: 0; }
    .multi-ul .title { width: 100%; float: left; clear: both; font-size: 24px; color: #888888; border-bottom: 1px solid #888888;  }
    .multi-ul .title span { display: block; margin-left: -1px; background: #ffffff; padding: 20px 0; font-weight: bold; }
    .multi-ul .sub { border-right: 1px solid #888888; border-bottom: 1px solid #888888; width: 50%; float: left; text-align:center; padding: 10px 30px; font-size: 24px; color: #888888; }
</style>