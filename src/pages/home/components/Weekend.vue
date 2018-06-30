<template>
    <div>
        <div class="title">周末去哪儿</div>
        <ul>
            <li class="item border-bottom" v-for="item of recommandList" :key="item.id">
                <div class="item-img-wrapper">
                    <img class="item-img" :src="item.imgUrl" alt="">
                </div>
                <div class="item-info">
                    <p class="item-title">{{item.title}}</p>
                    <p class="item-desc">{{item.desc}}</p>
                </div>
            </li>
        </ul>
    </div>
</template>

<script>
export default {
    name: 'HomeWeekend',
    data () {
        return {
            recommandList: [{
                        id:'0001',
                        imgUrl:'http://img1.qunarzz.com/sight/source/1505/4b/d04aa63b1b0ab3.jpg_r_640x214_a3a9c5b6.jpg',
                        title: '大连圣亚海洋世界',
                        desc: '浪漫大连首站，浪漫的海洋主题公园'
                    },
                    {
                        id:'0002',
                        imgUrl:'http://img1.qunarzz.com/sight/p0/1511/34/34170b200db08a5a90.img.jpg_150x150_ef0af2af.jpg',
                        title: '大连圣亚海洋世界',
                        desc: '浪漫大连首站，浪漫的海洋主题公园'
                    },
                    {
                        id:'0003',
                        imgUrl:'http://img1.qunarzz.com/sight/p0/1511/34/34170b200db08a5a90.img.jpg_150x150_ef0af2af.jpg',
                        title: '大连圣亚海洋世界',
                        desc: '浪漫大连首站，浪漫的海洋主题公园'
                    }
             ]
        }
    }
}
</script>

<style lang="stylus" scoped>
    @import '~styles/mixins.styl'
    .title
        margin-top: .2rem
        line-height: .8rem
        background: #eee
        text-indent: .2rem
    .item-img-wrapper 
        overflow: hidden
        height: 0
        padding-bottom: 33.9%
        .item-img 
            width: 100%
    .item-info  
        padding: .1rem
        .item-title     
            line-height: .54rem
            font-size: .32rem
            ellipsis()
        .item-desc  
            line-height: .4rem
            color: #ccc
            ellipsis()




</style>


