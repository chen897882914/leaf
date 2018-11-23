<template>
<div>
    21313213
    <ul>
        <li v-for="(item,index) in nav">
            <a :href="item.url">{{item.name}}</a>
            <ul v-if="item.members">
                <li v-for="value in item.members">
                    <a :href="value.url">{{value.name}}</a>
                </li>
            </ul>
        </li>
    </ul>
</div>
</template>

<script>
//new Vue({
//            el: '.page',
//            data: {
//                nav:[{
//                    "name": "首页",
//                    "url": "index.html"
//
//                },{
//                    "name": "关于我们",
//                    "url": "index.html",
//                    "members":[{"name": "项目简介", "url": "about.html"},
//                        {"name": "师资团队", "url": "about.html"},
//                        {"name": "联系我们", "url": "about.html"},
//                        {"name": "使用手册", "url": "about.html"}]
//                },{
//                    "name": "课程中心",
//                    "url": "index.html",
//                    "members":[{"name": "项目简介", "url": "about.html"},
//                        {"name": "师资团队", "url": "about.html"},
//                        {"name": "联系我们", "url": "about.html"},
//                        {"name": "使用手册", "url": "about.html"}]
//                },{
//                    "name": "教材读本",
//                    "url": "index.html",
//                    "members":[{"name": "项目简介", "url": "about.html"},
//                        {"name": "师资团队", "url": "about.html"},
//                        {"name": "联系我们", "url": "about.html"},
//                        {"name": "使用手册", "url": "about.html"}]
//                },
//                ]
//            }
//
//
//        })
    </script>