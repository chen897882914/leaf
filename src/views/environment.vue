<template>
    <div class="environment">
        <my-heared></my-heared>
        <div class="ba-color">
            <div class="environment-heared">
                <div>
                    <ul class="narrate">
                        <li>不求外在奢华，唯筑典雅舒适 </li>
                        <li>别致空间、典雅装饰，源于我们对美的信仰与追求 </li>
                        <li>安心就诊、星级卧房，源于我们对您的尊重与承诺</li>
                        <li>整体全进口设备、专业高素质人员配备</li>
                        <li>每一份用心都体现了北京叶子的品质</li>
                        <li>每一次体验都凝聚了北京叶子的期待</li>
                    </ul>
                </div>
            </div>
            <div class="panel">
                <div class="move-pic">
                    <ul class="picture-ol">
                        <li><img src="../../public/img/lobby.png"></li>
                        <li>大厅</li>
                    </ul>
                </div>
            </div>
            <div class="panel">
                <div class="move-pic">
                    <ul class="picture-ol">
                        <li><img src="../../public/img/rest-area.png"></li>
                        <li>大厅休息区</li>
                    </ul>
                </div>
            </div>
            <div class="panel">
                <div class="move-pic">
                    <ul class="picture-ol">
                        <li><img src="../../public/img/experts-wall.png"></li>
                        <li>大厅专家墙</li>
                    </ul>
                </div>
            </div>
            <div class="panel">
                <div class="move-pic">
                    <ul class="picture-ol">
                        <li><img src="../../public/img/vip-consult.png"></li>
                        <li>VIP咨询室</li>
                    </ul>
                </div>
            </div>
            <div class="panel">
                <div class="move-pic">
                    <ul class="picture-ol">
                        <li><img src="../../public/img/consulting-room.png"></li>
                        <li>咨询室</li>
                    </ul>
                </div>
            </div>
            <div class="panel">
                <div class="move-pic">
                    <ul class="picture-ol">
                        <li><img src="../../public/img/laboratory-room.png"></li>
                        <li>化验室</li>
                    </ul>
                </div>
            </div>
            <div class="panel">
                <div class="move-pic">
                    <ul class="picture-ol">
                        <li><img src="../../public/img/skin-treatment.png"></li>
                        <li>皮肤治疗中心</li>
                    </ul>
                </div>
            </div>
            <div class="panel">
                <div class="move-pic">
                    <ul class="picture-ol">
                        <li><img src="../../public/img/skin-treatment-room.png"></li>
                        <li>VIP皮肤治疗室</li>
                    </ul>
                </div>
            </div>
            <div class="panel">
                <div class="move-pic">
                    <ul class="picture-ol">
                        <li><img src="../../public/img/operating-room.png"></li>
                        <li>手术室</li>
                    </ul>
                </div>
            </div>
            <div class="panel">
                <div class="move-pic">
                    <ul class="picture-ol">
                        <li><img src="../../public/img/inpatient-ward.png"></li>
                        <li>病房</li>
                    </ul>
                </div>
            </div>
            <div class="panel">
                <div class="move-pic">
                    <ul class="picture-ol">
                        <li><img src="../../public/img/vip-inpatient-ward.png"></li>
                        <li>VIP病房</li>
                    </ul>
                </div>
            </div>
            <div class="panel">
                <div class="move-pic">
                    <ul class="picture-ol">
                        <li><img src="../../public/img/recovery.png"></li>
                        <li>康复休息区</li>
                    </ul>
                </div>
            </div>
            <div class="panel">
                <div class="move-pic">
                    <ul class="picture-ol">
                        <li><img src="../../public/img/nurses-station.png"></li>
                        <li>护理站</li>
                    </ul>
                </div>
            </div>
            <div class="panel">
                <div class="move-pic">
                    <ul class="picture-ol">
                        <li><img src="../../public/img/injection-room.png"></li>
                        <li>注射室</li>
                    </ul>
                </div>
            </div>
            <div class="panel">
                <div class="move-pic">
                    <ul class="picture-ol">
                        <li><img src="../../public/img/good-teeth.png"></li>
                        <li>美齿中心</li>
                    </ul>
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
    .ebvironment { width: 100%;}
    .ba-color { background-color: #ffffff; padding-bottom: 160px; }
    .environment-heared { margin-top: 10px; padding: 60px 0 40px;  }
    .narrate { text-align: center; }
    .narrate>li { text-align: center; padding-bottom: 20px; font-size: 24px; color:#888888; }
    
    .panel { position: relative; padding-bottom: 10px; }
    .move-pic { text-align: center;}
    .picture-ol>li:nth-child(1) { flex: 1; height: 460px; }
    .picture-ol>li:nth-child(2) { position: absolute; top: 0; padding: 15px 89px 0; font-size: 24px; color: #ffffff; font-weight: 1000; }
</style>