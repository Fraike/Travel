<template>
    <div>
        <div class="banner" @click="handleBannerClick">
            <img class="banner-img" src="//img1.qunarzz.com/sight/p0/1805/6f/6f885ea8b30c67bca3.water.jpg_600x330_f2f668e4.jpg" alt="">
            <div class="banner-info">
                <div class="banner-title">世界之窗(AAAAA景区)</div>
                <div class="banner-number"><span class="iconfont banner-icon ">&#xe611;</span>39</div>
            </div>
        </div>
        <common-gallary :imgs="imgs" v-show="showGallary" @close="handleGallaryClose"></common-gallary>
    </div>
</template>

<script>
import CommonGallary from 'common/gallary/Gallary'
    export default{
        name: 'DetailBanner',
        data () {
            return {
                showGallary: false,
                imgs: ['http://img1.qunarzz.com/sight/p0/1505/c2/c24454425bc956ab.water.jpg_r_800x800_c8e61ea0.jpg',
                'http://img1.qunarzz.com/sight/p0/1601/84/844dc50f4c47c86890.water.jpg_r_800x800_867f68aa.jpg']
            }
        },
        methods: {
            handleBannerClick () {
                this.showGallary = true
            },
            handleGallaryClose () {
                this.showGallary = false
            }
        },
        components: {
            CommonGallary
        }
    }
</script>

<style lang="stylus" scoped>
    .banner 
        position:relative
        overflow: hidden
        height: 0
        padding-bottom: 55%
        .banner-img 
            width: 100%
        .banner-info  
            display: flex  
            position: absolute
            left: 0
            right: 0
            bottom: 0
            line-height: .6rem
            color: #fff
            background-image: linear-gradient(top, rgba(0,0,0,0), rgba(0,0,0,.8))
            .banner-title
                flex: 1
                font-size: .32rem
                padding: 0 .2rem
            .banner-number
                margin-top: .14rem
                padding: 0 .4rem
                height: .32rem
                line-height: .32rem
                border-radius: .2rem
                background: rgba(0,0,0,.8)
                font-size: .24rem
                .banner-icon    
                    font-size: .24rem

</style>
