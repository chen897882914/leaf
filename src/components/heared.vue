<template>
    <div>
        <div class="heared-lo">
            <div class="heared-lo-inn">
                <ul class="heared-put">
                    <li><img src="../../public/img/w-Adidas.png" @click="showToggel"></li>
                    <li><img src="../../public/img/w-logo1.png"></li>
                    <li><img src="../../public/img/w-magnifying.png"></li>
                </ul>
            </div>
        </div>
        
        <div class="navigation-bars">
            <div class="bars-imm">
                <button class="btn prev" @click="prev"><img src="../../public/img/btn-left.png"></button>
                <div class="stage" ref="stage">
                    <div class="stage-line">
                        <ul class="bars-ul" ref="barsUl" :style="{ width: ((navItemWidth * nav.length) + 10) +'px', left: left}">
                            <li v-for="(item, index) in nav" :style="{ width: navItemWidth +'px'}" :class="[index == id ? 'current' : '']"><router-link :to="{ path: item.path, query: { index: index, left: left }}">{{item.name}}</router-link></li>
        <!--
                            <li><router-link to="/environment">典雅环境</router-link></li>
                            <li><router-link to="/honor">叶子荣誉</router-link></li>
        -->
                        </ul>
                    </div>
                </div>
                <button class="btn next" @click="next"><img src="../../public/img/btn-right.png"></button>
            </div>
        </div>
        <my-serve v-show="isShow"></my-serve>
    </div>
</template>

<script>
    import MyServe from '@/components/serve'
    export default {
        components: {MyServe},
        data (){
            return {
                nav:[ {
                    path:'/about',
                    name:'叶子简介'
                },{
                    path:'/environment',
                    name:'典雅环境'
                },{
                    path:'/honor',
                    name:'叶子荣誉'
                },{
                    path:'/new',
                    name:'叶子新闻'
                },{
                    path:'/environment',
                    name:'典雅环境1'
                },{
                    path:'/honor',
                    name:'叶子荣誉end'
                } ],
                navItemWidth: 0,
                current: 0,
                id: parseInt(this.$route.query.index) || 0,
                left: this.$route.query.left || '0px',
                status: true,
                isShow: false
            }
        },
        watch: {
            current () {
                if(this.status === false) {
                    this.left = this.current * (-this.navItemWidth) +'px'
                }
            }   
        },
        mounted () {
            this.$nextTick(() => {
                const stage = this.$refs['stage']
                const vw = stage.clientWidth - 3
                this.navItemWidth = vw / 3   
                this.current = parseInt(this.left.replace('px', '') * -1 / this.navItemWidth)
                this.$nextTick(() => {
                    this.status = false
                })
            })
        },
        methods: {
            prev () {
                if(this.current > 0){
                    this.setAni()
                    this.current --
                }
            },
            next () {
                if(this.current < this.nav.length - 3){
                    this.setAni()
                    this.current ++
                }
            },
            setAni () {
                this.$refs['barsUl'].style.transition = 'left 300ms ease-in-out'
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
    .heared-lo { background-color: #aa854f; }
    .heared-lo-inn {  width: 100%;}
    .heared-put { display: flex;  }
    .heared-put>li:nth-child(1) { padding: 30px 0 30px 30px; }
    .heared-put>li:nth-child(2) { width: 100%; text-align: center; padding: 15px 0; }
    .heared-put>li:nth-child(3) {  right: 0; padding: 30px 30px 30px 0; }
    
    .navigation-bars { background-color: #ffffff; }
    .bars-imm { width: 100%; position: relative; }
    .bars-ul {   width: 1000%; font-size: 24px; position: absolute; left: 0; top: 0; }
    .bars-ul>li { float: left; border-right: 2px solid #efefef; text-align: center; }
    .bars-ul>li.current a { color: red; }
    
    .stage { margin: 0 auto; width: 84%; height: 70px; padding: 20px 0; }
    .stage-line { width: 100%; height: 35px; position: relative; overflow: hidden;  border-left: 2px solid #efefef; }
    
    .bars-ul, a { color: #888888; }
    .btn {  background-color: none; border: 0; outline: inherit; width: 30px; height: 30px; position: absolute; left: 10px; top: 50%; margin-top: -15px; }
    .next { right: 10px; left: auto; }
</style>