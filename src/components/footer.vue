<template>
    <div class="relation-me">
        <div class="foot-left">
            <div class="footer">
                <ul class="foot-btn">
                    <li><img :src="icons.HomeIcon"></li>
                    <li><router-link to="/">首页</router-link></li>
                </ul>
            </div>
            <div class="footer">
                <ul class="foot-btn">
                    <li><img :src="icons.ProjectIcon"></li>
                    <li>项目</li>
                </ul>
            </div>
            <div class="footer">
                <ul class="foot-btn">
                    <li><img src="../../public/img/phone.png"></li>
                    <li>电话</li>
                </ul>
            </div>
            <div class="footer">
                <ul class="foot-btn">
                    <li><img src="../../public/img/consult.png"></li>
                    <li>咨询</li>
                </ul>
            </div>
        </div>
    </div>
</template>
<script>
    import HomeIcon from '../../public/img/home.png'
    import ProjectIcon from '../../public/img/project.png'
    export default {
        props: ['navlist'],
        data () {
            return {
                icons: {
                    HomeIcon,    
                    ProjectIcon 
                }
            }
        }
    }
</script>
<style lang="css" scoped>
    .relation-me { width: 100%; max-width: 828px; border-top: 1px solid #adadad; bottom: 0; position: fixed; z-index: 31; }
    .footer { margin: 0; padding: 10px 60px; display: inline-block; }
    .foot-left { margin: 0 auto; width: 100%;  display: block; text-align: center; background-color: #ffffff; text-align: center; }
    .foot-btn li { font-size: 24px; color: #888888; }
    a { color: #888888; }
</style>