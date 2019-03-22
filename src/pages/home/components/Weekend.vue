<template>
  <div>
    <div class="title">周末去哪</div>
    <ul>
      <li class="item border-bottom" v-for="item of recommendList">
        <div class="item-img-wrapper">
        <img class="item-img" :src="item.imgUrlL"/>
        </div>
        <div class="item-info">
          <p class="item-title">{{item.title}}</p>
          <p class="item-desc">{{item.desc}}</p>
          <p class="item-price"></p>
        </div>
      </li>
    </ul>
  </div>

</template>

<script>

  export default {
    name: "HomeWeekend",
    data (){
      return{
        recommendList:[{
          id:'0001',
          imgUrlL:"https://imgs.qunarzz.com/sight/source/1811/15/66f14e0fd6fbb.jpg_r_640x214_5d69f21d.jpg",
          title:'清远周边逛',
          desc:'长隆野生动物世界天下第一，这里是你梦开始的地方'
        },{
          id:'0002',
          imgUrlL:'https://imgs.qunarzz.com/sight/source/1811/b8/5d599bbdcf8b57.jpg_r_640x214_2ee055e3.jpg',
          title:'浮在海上的绿洲',
          desc:'碧水湾温泉度假村天下第一，这里是你梦开始的地方'
        },{
          id:'0003',
          imgUrlL:'https://imgs.qunarzz.com/sight/source/1812/fe/208e0360d686b8.jpg_r_640x214_7b9e6607.jpg',
          title:'广州泡汤圣地',
          desc:'南沙百万葵园天下第一，这里是你梦开始的地方'
        },{
          id:'0004',
          imgUrlL:'https://imgs.qunarzz.com/sight/source/1505/92/580e9ea4f37a1b.jpg_r_640x214_72112761.jpg',
          title:'广州必打卡',
          desc:'广州长隆旅游度假区天下第一，这里是你梦开始的地方'
        },{
          id:'0005',
          imgUrlL:'https://imgs.qunarzz.com/sight/source/1811/f8/29dfa785277839.jpg_r_640x214_7d051523.jpg',
          title:'阳江温泉知多少',
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
  .item-img-wrapper
    overflow:hidden
    height:0
    padding-bottom:33.9%
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
