<template>
    <div class="honor">
        <my-heared></my-heared>
        <div class="honor-inn">
            <div class="honor-ol">
                <ul class="honor-rep">
                    <li><img src="../../public/img/authorization.png"></li>
                    <li><img src="../../public/img/segmentation.png"></li>
                </ul>
                <ul class="honor-rep">
                    <li><img src="../../public/img/year-centre.png"></li>
                    <li><img src="../../public/img/segmentation.png"></li>
                </ul> 
                <ul class="honor-rep">
                    <li><img src="../../public/img/clinic.png"></li>
                    <li><img src="../../public/img/segmentation.png"></li>
                </ul> 
                <ul class="honor-rep">
                    <li><img src="../../public/img/designated-agency.png"></li>
                    <li><img src="../../public/img/segmentation.png"></li>
                </ul> 
                <ul class="honor-rep">
                    <li><img src="../../public/img/health2012.png"></li>
                    <li><img src="../../public/img/segmentation.png"></li>
                </ul> 
                <ul class="honor-rep">
                    <li><img src="../../public/img/botox.png"></li>
                    <li><img src="../../public/img/segmentation.png"></li>
                </ul> 
                <ul class="honor-rep">
                    <li><img src="../../public/img/breast.png"></li>
                    <li><img src="../../public/img/segmentation.png"></li>
                </ul> 
                <ul class="honor-rep">
                    <li><img src="../../public/img/2017qiang.png"></li>
                    <li><img src="../../public/img/segmentation.png"></li>
                </ul>
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
    
    .honor { width: 100%; }
    .honor-inn { padding: 0 10px; margin-top:10px ; width: 100%; padding-bottom: 120px; }
    .honor-ol {  padding: 38px 0 22px; width: 100%; background-color: #ffffff; }
    .honor-rep { padding-top: 22px; width: 100%; text-align: center; }
    .honor-rep>li:nth-child(1) { height: 353px; padding-bottom: 10px; }
    .honor-rep>li:nth-child(2) { height: 28px; }
</style>