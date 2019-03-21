<template>
  <swiper :options="swiperOption">
    <!-- slides -->

    <swiper-slide>
      <img class="swiper-img" src="http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20193
/2f5f3ea4698c9b7898db7562d89b91ed.jpg_750x200_bd3b4ce9.jpg"/>
    </swiper-slide>
    <swiper-slide>
      <img class="swiper-img" src="http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20192/
892f011c3b7bd6815b460c659acc5651.jpg_750x200_e2242cfb.jpg">
    </swiper-slide>


    <!-- Optional controls -->
    <div class="swiper-pagination"  slot="pagination"></div>
    <!--
    <div class="swiper-button-prev" slot="button-prev"></div>
    <div class="swiper-button-next" slot="button-next"></div>
    <div class="swiper-scrollbar"   slot="scrollbar"></div>
    -->
  </swiper>

</template>

<script>

    import SwiperSlide from "../../../../node_modules/vue-awesome-swiper/src/slide.vue";

    export default {
      components: {SwiperSlide},
      name: "HomeSwiper",
        data(){
          return{
            swiperOption:{}
          }
        }

    }
</script>

<style lang="stylus" scoped>
  .swiper-img
    width :100%

</style>
