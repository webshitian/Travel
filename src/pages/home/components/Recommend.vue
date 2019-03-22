<template>
  <div>
    <div class="title">热销推荐</div>
    <ul>
      <li class="item border-bottom" v-for="item of recommendList">
        <img class="item-img" :src="item.imgUrlL"/>
        <div class="item-info">
          <p class="item-title">{{item.title}}</p>
          <p class="item-desc">{{item.desc}}</p>
          <p class="item-price"></p>
          <button class="item-button">查看详情</button>
        </div>
      </li>
    </ul>
  </div>

</template>

<script>

  export default {
    name: "HomeRecommend",
    data (){
      return{
        recommendList:[{
          id:'0001',
          imgUrlL:"https://imgs.qunarzz.com/sight/p0/201403/07/30b534b0de51ccac2906bcb6ba159988.jpg_200x200_2f08733b.jpg",
          title:'长隆野生动物世界',
          desc:'长隆野生动物世界天下第一，这里是你梦开始的地方'
        },{
          id:'0002',
          imgUrlL:'https://imgs.qunarzz.com/sight/p0/1410/20/41d723daadc98045fe6b7283ba0af40c.jpg_200x200_5a05d5bc.jpg',
          title:'碧水湾温泉度假村',
          desc:'碧水湾温泉度假村天下第一，这里是你梦开始的地方'
        },{
          id:'0003',
          imgUrlL:'https://imgs.qunarzz.com/sight/p0/1603/3c/3c514c20a740128b90.water.jpg_200x200_c7102a23.jpg',
          title:'南沙百万葵园',
          desc:'南沙百万葵园天下第一，这里是你梦开始的地方'
        },{
          id:'0004',
          imgUrlL:'https://imgs.qunarzz.com/sight/p0/1603/3b/3bd311262ee06d8c90.img.jpg_200x200_c118d7da.jpg',
          title:'广州长隆旅游度假区',
          desc:'广州长隆旅游度假区天下第一，这里是你梦开始的地方'
        },{
          id:'0005',
          imgUrlL:'https://imgs.qunarzz.com/sight/p0/1603/50/50309ba1d90e4e3290.water.jpg_200x200_41a17778.jpg',
          title:'流溪河国家森林公园',
          desc:'流溪河国家森林公园天下第一，这里是你梦开始的地方'
        }]
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
  .item
    overflow:hidden
    display:flex
    height: 1.9rem
    .item-img
      width:1.7rem
      height:1.7rem
      padding: .1rem
    .item-info
      flex:1 //自动撑开屏幕的宽度
      padding: .1rem
      min-width:0
      .item-title
        line-height: .54rem
        font-size: .32rem
        ellipsis()
      .item-desc
        line-height: .4rem
        color: #ccc
        ellipsis()
      .item-button
        line-height: .44rem
        margin-top: .16rem
        background: #ff9300
        padding:0 .2rem
        border-radius: .06rem
        color: #fff
</style>
