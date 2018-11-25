<template>
    <div class="box">
        <div class="project" :style="{height:projectHeight + 'px'}">
            <div class="project-bg">
                <div class="one-level">
                    <ul class="one-level-ul"  id="multi-ul">
                        <li class="right-hight" v-for="(item, index) in left" :class="[index == present ? 'present' : '' ]" @click="clickTwo(index)">{{item}}</li>
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
            rightHeight: 0,
            multiUl: null,
            left: ['眼部整形','鼻部整形','胸部整形','微整形','面部精雕','抗衰除皱','身体塑型','皮肤美容','艺术纹绣','牙齿美容','毛发种植','私密整形','无痛脱毛','其它整形','修复中心',],
            present: 0,
            leftservice: [
                [
                    {name:'双眼皮'},{name:'开眼角'},{name:'祛眼袋'},{name:'重睑修复'},{name:'眼袋修复'},{name:'眼周年轻化'},{name:'上眼窝凹陷'},{name:'上睑下垂矫正'}
                ],
                [
                    {name:'3D立体隆鼻'},{name:'假体隆鼻'}, {name:'歪鼻矫正'}, {name:'鼻基底填充'}, {name:'鼻背骨缩窄'},
                    {name:'驼峰鼻矫正'},{name:'鼻头综合整形'}, {name:'鼻翼缩小提升'}, {name:'自体肋软骨隆鼻'}, {name:'隆鼻修复'},{name:'注射隆鼻'}
                ],
                [
                  {name: '数字化动感丰胸'},
                  {name: '副乳切除'},
                  {name: '巨乳缩小'},
                  {name: '垂乳提升'},
                  {name: '自体脂肪丰乳'},
                  {name: '乳头乳晕整形'},
                  {name: '男士乳房矫正'},
                  {name: '乳房包膜松解'},
                  {name: '隆胸材料取出'},
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
                ],
                [
                    {
                        name: '手术-脸型轮廓',
                        child: [
                            {name: '精致脸型雕塑'},
                            {name: '隆下巴 '},
                            {name: '颏综合整形 '},
                            {name: '颧骨颧弓整形'},
                            {name: '下颏材料取出'},
                        ]
                    },
                    {
                        name: '注射-面部填充',
                        child: [
                            {name: '丰额头'},
                            {name: '太阳穴 '},
                            {name: '丰眉弓'},
                            {name: '注射隆鼻 '},
                            {name: '丰面颊'},
                            {name: '丰唇'},
                            {name: '丰耳垂'},
                            {name: '丰下巴'},
                        ]
                    },
                    {
                        name: '注射-瘦脸',
                        child: [
                            {name: '瘦脸'},
                            {name: '颏肌'},
                        ]
                    }
                ],
                [
                    {
                        name: '手术',
                        child: [
                            {name: 'SMAS驻颜除皱'},
                            {name: '内窥镜除皱'},
                            {name: '拉皮修复'},
                            {name: '埋线提升'},
                        ]
                    },
                    {
                        name: '注射',
                        child: [
                            {name: 'PRP焕颜抗衰'},
                            {name: '额纹'},
                            {name: '眉间纹'},
                            {name: '鱼尾纹'},
                            {name: '鼻背纹'},
                            {name: '法令纹'},
                            {name: '嘴角纹 '},
                            {name: '口角提升'},
                            {name: '下颌缘提升'},
                        ]
                    },
                    {
                        name: '激光',
                        child: [
                            {name: '全面部细小皱纹'},
                            {name: '颈部皱纹'},
                            {name: '妊娠纹'},
                            {name: '肥胖纹'},
                        ]
                    }
                ],
                [
                    {
                        name: '吸脂塑型',
                        child: [
                            {name: 'S形雕塑美体'},
                            {name: '面部吸脂'},
                            {name: '躯干吸脂'},
                            {name: '四肢吸脂'},
                            {name: '吸脂修复'},
                            {name: '腹壁整形 '},
                            {name: '肚脐整形'},
                        ]
                    },
                    {
                        name: '自体脂肪塑型',
                        child: [
                            {name: '自体脂肪丰乳'},
                            {name: '自体脂肪丰臀'},
                            {name: '自体脂肪填充面部'},
                            {name: '矫正轻度X.O形腿'},
                            {name: '吸脂术后凹陷填充'},
                        ]
                    },
                    {
                        name: '注射',
                        child: [
                            {name: '瘦脸'},
                            {name: '瘦小腿'},
                            {name: '颏肌'},
                        ]
                    }
                ],
                [
                    {
                        name: '焕颜净肤',
                        child: [
                            {name: 'SMAS驻颜除皱'},
                            {name: '内窥镜除皱'},
                            {name: '拉皮修复'},
                            {name: '埋线提升'},
                        ]
                    },
                    {
                        name: '医学靓肤',
                        child: [
                            {name: 'DNA美肤祛痘'},
                            {name: '扁平疣'},
                            {name: '色素痣'},
                            {name: '太田痣'},
                            {name: '睑黄瘤'},
                            {name: '汗管瘤'},
                            {name: '褐青色痣'},
                        ]
                    },
                    {
                        name: '无龄美肌',
                        child: [
                            {name: '全面部细小皱纹'},
                            {name: '颈部皱纹'},
                            {name: '妊娠纹'},
                            {name: '肥胖纹'},
                        ]
                    }
                ],
                [
                    {name: '自然仿生绘眉'},
                    {name: '纹绣眉毛修复术'},
                    {name: '纹绣男士补眉术'},
                    {name: '魅惑浓密睫毛线'},
                    {name: '水润柔唇'},
                    {name: '漂阴唇/乳晕'},
                ],
                [
                    {
                        name: '牙齿美白',
                        child: [
                            {name: '冷光皓洁美齿'},
                            {name: '超声波清洁'},
                            {name: '喷砂清洁'},
                        ]
                    },
                    {
                        name: '美学修复',
                        child: [
                            {name: '高仿生美容冠'},
                            {name: '补牙'},
                            {name: '龅牙矫正'},
                            {name: '根管治疗'},
                            {name: '美容性冠修复'},
                        ]
                    },
                    {
                        name: '安全种植',
                        child: [
                            {name: 'ITI舒感种植牙'},
                            {name: '即刻种植'},
                            {name: '缺失种植'},
                            {name: '全口种植'},
                        ]
                    }
                ],
                [
                    {name: '胡须种植'},
                    {name: '眉毛种植'},
                    {name: '睫毛种植'},
                    {name: '阴毛种植'},
                    {name: '发际线种植'},
                    {name: '头部毛发种植'},
                ],
                [
                    {name: '阴蒂整形'},
                    {name: '阴唇缩小'},
                    {name: '处女膜修复'},
                    {name: '阴道缩紧'},
                ],
                [
                    {name: '腋毛'},
                    {name: '腿毛'},
                    {name: '臂毛'},
                    {name: '唇毛'},
                    {name: '发际线'},
                    {name: '比基尼'},
                    {name: '络腮胡'},
                ],
                [
                    {name: '眉部整形'},
                    {name: '微创除腋臭'},
                    {name: '唇部整形'},
                    {name: '耳部整形'},
                    {name: '腋臭多汗症'},
                    {name: '疤痕针'},
                    {name: '玻尿酸溶解酶'},
                ],
                [
                    {name: '重睑修复'},
                    {name: '眼袋修复'},
                    {name: '隆胸材料取出 '},
                    {name: '隆鼻修复'},
                    {name: '下颏材料取出'},
                    {name: '拉皮修复'},
                    {name: '吸脂修复'},
                    {name: '处女膜修复'},
                    {name: '奥美定取出'},
                    {name: '玻尿酸溶解酶'},
                ]
            ],
        }
    },
    mounted () {
        console.log (document.querySelector('.heared-lo'))
        this.bodyHeight = document.documentElement.clientHeight
        this.hearedHeight = document.querySelector('.heared-lo') ? document.querySelector('.heared-lo').clientHeight  : 80
        this.footerHeight = document.querySelector('.relation-me').clientHeight
        this.projectHeight = this.bodyHeight - this.hearedHeight - this.footerHeight - 10
        this.multiUl = document.querySelector('#multi-ul')
        
    },
    methods: {
        clickTwo:function (index){
            this.present = index
            this.rightHeight = document.querySelector('.right-hight').clientHeight + 2
            this.liheight = Math.floor(this.projectHeight /  this.rightHeight) - 2
            if (index>this.liheight) {
                var diff = index-this.liheight
                if (index > this.left.length - 3 ){
                    diff =  this.left.length - 3 - this.liheight
                }
                this.multiUl.style.marginTop = (-1 * diff * (this.rightHeight)) + 'px'
                
            }else {
                this.multiUl.style.marginTop =  '0px'
            }
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