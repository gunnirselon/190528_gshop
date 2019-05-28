<template>
  <section class="msite">
    <!--首页头部-->
    <header class="header">
          <span class="header_search">
          </span>
      <span class="header_title">
            <span class="header_title_text ellipsis"><i class="iconfont icon-jiancha">点我达</i></span>
          </span>
      <span class="header_login">
            <span class="header_login_text">登录|注册</span>
          </span>
    </header>
    <!--首页导航-->
    <nav class="msite_nav">
      <div class="swiper-container">
        <div class="swiper-wrapper">
          <div class="swiper-slide">
            <a href="javascript:" class="link_to_food">
              <div class="food_container">
                <img src="./images/nav/if_apple_2003193.png">
              </div>
              <span>苹果</span>
            </a>
            <a href="javascript:" class="link_to_food">
              <div class="food_container">
                <img src="./images/nav/if_grapes_2003194.png">
              </div>
              <span>葡萄</span>
            </a>
            <a href="javascript:" class="link_to_food">
              <div class="food_container">
                <img src="./images/nav/if_lemon_2003191.png">
              </div>
              <span>柠檬</span>
            </a>
            <a href="javascript:" class="link_to_food">
              <div class="food_container">
                <img src="./images/nav/if_mango_2003198.png">
              </div>
              <span>芒果</span>
            </a>
            <a href="javascript:" class="link_to_food">
              <div class="food_container">
                <img src="./images/nav/if_pear_2003196.png">
              </div>
              <span>梨子</span>
            </a>
            <a href="javascript:" class="link_to_food">
              <div class="food_container">
                <img src="./images/nav/if_strawberry_2003199.png">
              </div>
              <span>草莓</span>
            </a>
            <a href="javascript:" class="link_to_food">
              <div class="food_container">
                <img src="./images/nav/if_orange_2003192.png">
              </div>
              <span>桔子</span>
            </a>
            <a href="javascript:" class="link_to_food">
              <div class="food_container">
                <img src="./images/nav/if_watermelon_2003190.png">
              </div>
              <span>西瓜</span>
            </a>
          </div>
          <div class="swiper-slide">
            <a href="javascript:" class="link_to_food">
              <div class="food_container">
                <img src="./images/nav/if_pomegranate_2003195.png">
              </div>
              <span>石榴</span>
            </a>
            <a href="javascript:" class="link_to_food">
              <div class="food_container">
                <img src="./images/nav/if_pineapple_2003197.png">
              </div>
              <span>菠萝</span>
            </a>
            <a href="javascript:" class="link_to_food">
            <div class="food_container">
              <img src="./images/nav/if_apple_2003193.png">
            </div>
            <span>苹果</span>
            </a>
            <a href="javascript:" class="link_to_food">
              <div class="food_container">
                <img src="./images/nav/if_grapes_2003194.png">
              </div>
              <span>葡萄</span>
            </a>
            <a href="javascript:" class="link_to_food">
              <div class="food_container">
                <img src="./images/nav/if_lemon_2003191.png">
              </div>
              <span>柠檬</span>
            </a>
            <a href="javascript:" class="link_to_food">
              <div class="food_container">
                <img src="./images/nav/if_mango_2003198.png">
              </div>
              <span>芒果</span>
            </a>
            <a href="javascript:" class="link_to_food">
              <div class="food_container">
                <img src="./images/nav/if_pear_2003196.png">
              </div>
              <span>梨子</span>
            </a>
            <a href="javascript:" class="link_to_food">
              <div class="food_container">
                <img src="./images/nav/if_strawberry_2003199.png">
              </div>
              <span>草莓</span>
            </a>
          </div>
        </div>
        <!-- Add Pagination -->
        <div class="swiper-pagination"></div>
      </div>
    </nav>
    <!--首页附近商家-->
    <div class="msite_shop_list">
      <div class="shop_header">
        <i class="iconfont icon-dangan"></i>
        <span class="shop_header_title">附近商家</span>
      </div>
      <shop-list/>
    </div>

  </section>

</template>

<script>
  import Swiper from 'swiper'
  import 'swiper/dist/css/swiper.min.css'
  import ShopList from '../../components/ShopList/ShopList'
export default {
    mounted() {
      new Swiper('.swiper-container',{
        loop:true,
        pagination:{
          el:'.swiper-pagination',
      },
      })
    },
  components:{
    ShopList
  }
}
</script>

<style lang="stylus" rel="stylesheet/stylus">
  @import "../../common/stylus/mixin.styl"
  .msite  //首页
    width 100%
    .header
      background-color #02a774
      position fixed
      z-index 100
      left 0
      top 0
      width 100%
      height 45px
      .header_search
        position absolute
        left 15px
        top 50%
        transform translateY(-50%)
        width 10%
        height 50%
        .icon-sousuo
          font-size 25px
          color #fff
      .header_title
        position absolute
        top 50%
        left 50%
        transform translate(-50%, -50%)
        width 50%
        color #fff
        text-align center
        .header_title_text
          font-size 20px
          color #fff
          display block
      .header_login
        font-size 14px
        color #fff
        position absolute
        right 15px
        top 50%
        transform translateY(-50%)
        .header_login_text
          color #fff
    .msite_nav
      bottom-border-1px(#e4e4e4)
      margin-top 45px
      height 200px
      background #fff
      .swiper-container
        width 100%
        height 100%
        .swiper-wrapper
          width 100%
          height 100%
          .swiper-slide
            display flex
            justify-content center
            align-items flex-start
            flex-wrap wrap
            .link_to_food
              width 25%
              .food_container
                display block
                width 100%
                text-align center
                padding-bottom 10px
                font-size 0
                img
                  display inline-block
                  width 50px
                  height 50px
              span
                display block
                width 100%
                text-align center
                font-size 13px
                color #666
        .swiper-pagination
          >span.swiper-pagination-bullet-active
            background #02a774
    .msite_shop_list
      top-border-1px(#e4e4e4)
      margin-top 10px
      background #fff
      .shop_header
        padding 10px 10px 0
        .shop_icon
          margin-left 5px
          color #999
        .shop_header_title
          color #999
          font-size 14px
          line-height 20px

</style>
