<template>
    <div>
        <div class="box">
            <div class="header">
                <div class="face">
                    <div class="img-stage" ref="stage" @mouseover="stopImg" @mouseout="playImg">
                        <div class="img-behind" >
                            <ul class="roll-put" :style="{ width: ((navItemWidth * img.length) + 10) +'px', left: current * (-navItemWidth) +'px'}">
                                <li v-for="list in img" :style="{ width: navItemWidth +'px'}"><img :src='list.myimg'></li>
                            </ul>
                        </div>
                        <div class="btn-li">
                            <ul class="btn-ul">
                                <li v-for="item in img.length" :class="[current == item - 1 ? 'current' : '']" @click="move(item - 1)"></li>
                            </ul>
                        </div>
                    </div>
                </div>
                <div class="menu" >
                    <img src="../../public/img/Adidas.png" @click="showToggel">
                </div>
               
                <div class="headline">
                    <img src="../../public/img/logo1.png">
                </div>
                <div class="search">
                    <img src="../../public/img/magnifying.png">
                </div>
            </div>
            <div class="navigation">
                <div class="neck">
                    <ul class="nevus">
                        <li class="put"><img src="../../public/img/leaf.png"></li>
                        <li><router-link to="/about">关于叶子</router-link></li>
                    </ul>
                </div>
                <div class="neck">
                    <ul class="nevus">
                        <li class="put"><img src="../../public/img/specialist.png"></li>
                        <li>叶子专家</li>
                    </ul>
                </div>
                <div class="neck">
                    <ul class="nevus">
                        <li class="put"><img src="../../public/img/safeguard.png"></li>
                        <li>安全保障</li>
                    </ul>
                </div>
                <div class="neck">
                    <ul class="nevus">
                        <li class="put"><img src="../../public/img/path.png"></li>
                        <li>来院路线</li>
                    </ul>
                </div>
            </div>
            <div class="option">
                <div class="option-inn">
                    <div class="plastic">
                        <ul class="part">
                            <li><img src="../../public/img/eye.png"></li>
                            <li>眼部整形</li>
                        </ul>
                    </div>
                    <div class="plastic">
                        <ul class="part">
                            <li><img src="../../public/img/nose.png"></li>
                            <li>鼻部整形</li>
                        </ul>
                    </div>
                    <div class="plastic">
                        <ul class="part">
                            <li><img src="../../public/img/needle.png"></li>
                            <li>微整形</li>
                        </ul>
                    </div>
                    <div class="plastic">
                        <ul class="part">
                            <li><img src="../../public/img/face.png"></li>
                            <li>面部精雕</li>
                        </ul>
                    </div>
                    <div class="plastic">
                        <ul class="part">
                            <li><img src="../../public/img/chest.png"></li>
                            <li>胸部整形</li>
                        </ul>
                    </div>

                    <div class="plastic">
                        <ul class="part">
                            <li><img src="../../public/img/anti-aging.png"></li>
                            <li>抗衰除皱</li>
                        </ul>
                    </div>
                    <div class="plastic">
                        <ul class="part">
                            <li><img src="../../public/img/plasticity.png"></li>
                            <li>身体塑性</li>
                        </ul>
                    </div>
                    <div class="plastic">
                        <ul class="part">
                            <li><img src="../../public/img/skin.png"></li>
                            <li>皮肤美容</li>
                        </ul>
                    </div>
                    <div class="plastic">
                        <ul class="part">
                            <li><img src="../../public/img/art.png"></li>
                            <li>艺术纹绣</li>
                        </ul>
                    </div>
                    <div class="plastic">
                        <ul class="part">
                            <li><img src="../../public/img/tooth.png"></li>
                            <li>牙齿美容</li>
                        </ul>
                    </div>

                    <div class="plastic">
                        <ul class="part">
                            <li><img src="../../public/img/privacy.png"></li>
                            <li>私密整形</li>
                        </ul>
                    </div>
                    <div class="plastic">
                        <ul class="part">
                            <li><img src="../../public/img/hair.png"></li>
                            <li>毛发种植</li>
                        </ul>
                    </div>
                    <div class="plastic">
                        <ul class="part">
                            <li><img src="../../public/img/unhairing.png"></li>
                            <li>无痛脱毛</li>
                        </ul>
                    </div>
                    <div class="plastic">
                        <ul class="part">
                            <li><img src="../../public/img/else.png"></li>
                            <li>其它项目</li>
                        </ul>
                    </div>
                    <div class="plastic">
                        <ul class="part">
                            <li><img src="../../public/img/repair.png"></li>
                            <li>修复中心</li>
                        </ul>
                    </div>
                </div>
            </div>
            <div class="hot">
                <h1>热门项目</h1>
            </div>
            <div class="subject">
                <div class="sub">

                </div>
            </div> 
            <div class="subject">
                <div class="sub">

                </div>
            </div>
            <div class="subject">
                <div class="sub">

                </div>
            </div>
            <div class="about-me">
                <div class="hot">
                    <h2>关于叶子</h2>
                </div>
                <div class="synopsis">
                    <ul class="syns">
                        <li>叶子简介</li>
                        <li>经营理念</li>
                        <li>典雅环境</li>
                        <li>叶子荣誉</li>
                        <li>叶子新闻</li>
                    </ul>
                </div>
            </div>
            <div class="about-me">
                <div class="hot">
                    <h2>叶子专家</h2>
                </div>
                <div class="synopsis">
                    <ul class="syns">
                        <li>叶子简介</li>
                        <li>经营理念</li>
                        <li>典雅环境</li>
                        <li>叶子荣誉</li>
                        <li>叶子新闻</li>
                    </ul>
                </div>
            </div>
            <div class="about-me">
                <div class="hot">
                    <h2>解决方案</h2>
                </div>
                <div class="synopsis">
                    <ul class="syns">
                        <li>叶子简介</li>
                        <li>经营理念</li>
                        <li>典雅环境</li>
                        <li>叶子荣誉</li>
                        <li>叶子新闻</li>
                    </ul>
                </div>
            </div>
            <div class="safeguard">
                <div class="hot">
                    <h2>安全保障</h2>
                </div>
    <!--
                <div class="synopsis">
                    <ul class="syns">
                        <li>叶子简介</li>
                        <li>经营理念</li>
                        <li>典雅环境</li>
                        <li>叶子荣誉</li>
                        <li>叶子新闻</li>
                    </ul>
                </div>
    -->
            </div>
            <div class="path-inn">
                <div class="path">
                    <button>来院路线</button>
                </div>
                <div class="relation">
                    <ul class="rela">
                        <li>Copyright © 2015 北京叶子整形美容医院</li>
                        <li>（京）医广【2014】第07-18-0184号</li>
                        <li><span class="split">京ICP备07504320号</span><span class="split">京卫网审[2014]第0071号</span></li>
                        <li></li>
                    </ul>
                </div>
            </div>
            <my-footer></my-footer>
        </div>
        <my-serve v-show="isShow" style="top: 80px;"></my-serve>
    </div>
</template>

<script>
    import MyFooter from '@/components/footer'
    import MyServe from '@/components/serve'
export default {
    name: 'Chen',
    components: { MyFooter, MyServe },
    data () {
        return {
            img:[{
                myimg:require('../../public/img/roll1.png'),
            }, {
                myimg:require('../../public/img/roll2.jpg'),
            }, {
                myimg:require('../../public/img/roll1.png'),
            }],
            navItemWidth: 0,
            current: 0,
            timer: null,
            isShow: false
        }
    },
    mounted () {
            this.$nextTick(() => {
                const stage = this.$refs['stage']
                const vw = stage.clientWidth
                this.navItemWidth = vw  
                this.playImg()
            })
        },
        methods: {
            move (index) {
                this.current = index    
            },
            stopImg () {
                if (this.timer) {
                    clearInterval(this.timer)
                }    
            },
            playImg () {
                this.timer = setInterval(() => {
                    this.current ++
                    if(this.current >= this.img.length){
                        this.current = 0    
                    }
                }, 3000)    
            },
            showToggel:function (){
                this.isShow = !this.isShow
            },
            showToggel:function (){
                this.isShow = !this.isShow
                if(this.isShow === true){
                    document.querySelector('html').style.overflow = 'hidden'
                    document.querySelector('body').style.overflow = 'hidden'
                
                }else{
                    document.querySelector('html').style.overflow = 'auto'
                    document.querySelector('body').style.overflow = 'auto'
                }
            }
        }
}
</script>
<style lang="css" scoped>
   
   
    .box { margin: 0 auto; width: 100%; }
    .header { margin: 0; padding: 0; width: 100%; position: relative; display: flex; }
    .face { width: 100%; margin: 0; padding: 0; float: left; }
    .face img { display: block; width: 100%; height: 100%; }
    
    .img-stage { width: 100%; position: relative; height: 414px; overflow: hidden; padding: 0; }
    .img-behind { width: 1000%; height: 100%;  }
    .roll-put { width: 100%; position: absolute; height: 100%; transition: left 300ms ease-in-out; }
    .roll-put>li { float: left; height: 100%; width: 100%; }
    
    .btn-li { margin: 0 auto; width: 100%; float: left; position: absolute; bottom: 30px;}
    .btn-ul { text-align: center; display: block; float: left; padding-left: 45%;}
    .btn-ul>li { width: 10px; height: 10px; border: 1px #ffffff solid; border-radius: 100%; opacity: 0.6; float: left; margin: 0 2px; }
    .btn-ul>li.current { background-color: #ffffff; opacity: 1; }
    .menu { margin: 0; padding: 30px 30px; float: left; position: absolute; }
    .headline { margin: 22px 0 0 280px; position: absolute; }
    .search { margin: 0; padding: 30px 30px; position: absolute; right: 0; top: 0; }
    
   
    
    .navigation { margin: 0; padding: 10px 10px 0; width: 100%; float: left; }
    .neck { padding-right: 3px; border-right: 3px #eeeeee solid; padding: 0; width: 25%; height: 164px; float: left; background-color: #ffffff; }
    .neck:last-child { border: 0; }
    .nevus { padding: 30px 10px; }
    .nevus>li { font-size: 24px; color: #aa854f; text-align: center; }
    .nevus, a { color: #aa854f; }
    .put img { margin: 0 auto; }
    
    .option { width: 100%; float: left; padding: 10px; }
    .option-inn { width: 100%; background-color: #ffffff; float: left; clear: both; padding: 30px 0 10px; }
    .plastic { width: 20%; height: 156px; float: left;  }
    .plastic ul { width: 96px; text-align: center; display: block; margin: 0 auto;  }
    .part >li { font-size: 24px; color: #888888; padding-bottom: 6px; }
    
    .hot { margin: 0; padding: 0; float: left; width: 100%; }
    .hot h1 { margin: 20px 0 20px; font-weight: normal; font-size: 24px; color: #888888; padding-left: 10px;}
    
    .subject { margin: 0; padding: 10px 10px 0; float: left; width: 100%; }
    .sub { background-color: #ffffff; width: 100%; height: 320px; }
    
    .about-me { margin: 0; padding: 30px 0 10px; width: 100%; float: left; border-bottom: 1px solid #adadad; }
    .synopsis { margin-left: 10px; float: left; }
    .hot h2 { margin: 0; font-weight: normal; font-size: 24px; color: #888888; padding: 0 10px 30px; }
    .syns li { font-size: 18px; color: #9d9d9d; padding-bottom: 20px; }
    .safeguard { margin: 0; padding: 30px 0 0; float: left; width: 100%; border-bottom: 1px solid #adadad; }
    
    .path-inn { margin-bottom: 100px; width: 100%; float: left; }
    .path { margin: 0 auto; padding-top: 60px; width: 100%; float: left; }
    .path button { margin: 0 auto; display: block; padding: 0 10px; height: 50px; border: 0; background-color: #074223; font-size: 24px; color: #ffffff; border-radius: 10px;}
    
    .relation { margin: 0; padding: 30px 0; display: block; float: left; width: 100%; text-align: center; }
    .split { padding: 0 10px; }
    .rela li:first-child { font-size: 14px; color: #9d9e9e; }
    .rela li:nth-child(2), .rela li:nth-child(3) { font-size: 14px; color: #888888; }
</style> 
