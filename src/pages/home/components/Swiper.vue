<template>
  <div class="wrapper">
    <swiper :options="swiperOption" v-if="showSwiper">
      <swiper-slide v-for="item of list" :key="item.id">
        <img class="swiper-img" :src="item.imgUrl"/>
      </swiper-slide>
      <div class="swiper-pagination" slot="pagination"></div>
    </swiper>
  </div>
</template>

<script>

    import SwiperSlide from "../../../../node_modules/vue-awesome-swiper/src/slide.vue";

    export default {
      components: {SwiperSlide},
      name: "HomeSwiper",
      props:{
        list:Array
      },
        data (){
          return{
            swiperOption:{
              pagination:'.swiper-pagination',
              loop:true //让轮播插件支持循环轮播

            }/*,
            swiperList:[{
              id:'0001',
              imgUrl:'http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20193\n' +
              '/2f5f3ea4698c9b7898db7562d89b91ed.jpg_750x200_bd3b4ce9.jpg'
            },{
              id:'0002',
              imgUrl:'http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20192/\n' +
              '892f011c3b7bd6815b460c659acc5651.jpg_750x200_e2242cfb.jpg'
            }]*/
          }
        },
      computed:{
          showSwiper (){
            return this.list.length
          }
      }

    }
</script>

<style lang="stylus" scoped>
  .wrapper >>> .swiper-pagination-bullet-active
    background :#ffffff
  .wrapper
    overflow :hidden
    width :100%
    height :0;
    padding-bottom :26.66%
    background :#eee
    .swiper-img
      width :100%

</style>
