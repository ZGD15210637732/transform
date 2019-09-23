<template>
  <div class="hello">
    <van-swipe style="height: 100%" vertical  :loop='false' @change="onChange">
      <van-swipe-item>
        <div class="first">
          <p :class="{'title':this.class[0].show}">流量至上的传统电商平台</p>
          <p :class="{'title1':this.class[0].show}">店铺运营成本递增</p>
          <p :class="{'title2':this.class[0].show}">流量获取愈发困难</p>
          <p :class="{'title3':this.class[0].show}">资源位越来越贵</p>
          <p :class="{'title4':this.class[0].show}">竞争对手却与日俱增</p>
          <p :class="{'title5':this.class[0].show}">与其举步艰难</p>
          <p :class="{'title6':this.class[0].show}">这时我们需要<span style="font-size: 30px;color:yellow">另辟蹊跷</span></p>
        </div>
      </van-swipe-item>
      <van-swipe-item>
        <div class="two">
          <!-- <img src="../assets/logo.png" alt="" :class="{'img':this.class[1].show}"> -->
          twpapp
        </div>
      </van-swipe-item>
      <van-swipe-item>
        <div class="three">
          <!-- <img src="../assets/logo.png" alt="" :class="{'img':this.class[2].show}"> -->
          threeapp
        </div>
      </van-swipe-item>
      <van-swipe-item>
        <div class="four">
          <!-- <img src="../assets/logo.png" alt="" :class="{'img':this.class[3].show}"> -->
          fourapp
        </div>
      </van-swipe-item>
      <van-swipe-item>
        <div class="five">
          <!-- <img src="../assets/logo.png" alt="" :class="{'img':this.class[4].show}"> -->
          fiveapp
        </div>
      </van-swipe-item>
      <van-swipe-item>
        <div class="six">
          <!-- <img src="../assets/logo.png" alt="" :class="{'img':this.class[5].show}"> -->
          sixapp
        </div>
      </van-swipe-item>
      <van-swipe-item>
          <div class="seven">
            <!-- <img src="../assets/logo.png" alt="" :class="{'img':this.class[5].show}"> -->
            sixapp
          </div>
        </van-swipe-item>
    </van-swipe>
  </div>
</template>

<script>
  import { Swipe, SwipeItem } from 'vant';
  export default {
    name: 'HelloWorld',
    data() {
      return {
        class: [
          {
            show: true
          },
          {
            show: false
          },
          {
            show: false
          },
          {
            show: false
          },
          {
            show: false
          },
          {
            show: false
          },
          {
            show: false
          }
        ],
      }
    },
    components: {
      [Swipe.name]: Swipe,
      [SwipeItem.name]: SwipeItem
    },
    methods: {
      onChange(i) {
        for (var item in this.class) {
          this.class[item].show = false
        }
        this.class[i].show = true
      }
    },

  }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  html,
  body {
    height: 100%;
  }

  .hello {
    height: 100%;
  }

  .first {
    width: 100%;
    height: 100%;
    background-image: url('../assets/1.jpg');
    background-size: 100% 
  }
  .two {
    width: 100%;
    height: 100%;
    background-image: url('../assets/2.jpg');
    background-size: 100%  100%
  }
  .three {
    width: 100%;
    height: 100%;
    background-image: url('../assets/3.jpg');
    background-size: 100%  100%
  }
  .four {
    width: 100%;
    height: 100%;
    background-image: url('../assets/4.jpg');
    background-size: 100%  100%
  }
  .five {
    width: 100%;
    height: 100%;
    background-image: url('../assets/5.jpg');
    background-size: 100%  100%
  }
  .six {
    width: 100%;
    height: 100%;
    background-image: url('../assets/6.jpg');
    background-size: 100%  100%
  }
  .seven {
    width: 100%;
    height: 100%;
    background-image: url('../assets/7.jpg');
    background-size: 100%  100%
  }
  .img {
    width: 100%
  }
  @keyframes spin{
    from { transform: translateX(0) translateY(0); }
    to { transform: translateX(550px) translateY(0px);}
}
  .title{
    color: white;
    font-size: 32px;
    position: absolute;
    top:400px;
    left: -500px;
    animation: spin 2s infinite linear ;
    animation-iteration-count:1;
    animation-fill-mode: forwards
  }
  .title1{
    color: white;
    font-size: 32px;
    position: absolute;
    top:500px;
    left: -500px;
    animation: spin 2s infinite linear ;
    animation-delay: 1s;
    animation-iteration-count:1;
    animation-fill-mode: forwards;
  }
  .title2{
    color: white;
    font-size: 32px;
    position: absolute;
    top:600px;
    left: -500px;
    animation: spin 2s infinite linear ;
    animation-delay: 2s;
    animation-iteration-count:1;
    animation-fill-mode: forwards
  }
  .title3{
    color: white;
    font-size: 32px;
    position: absolute;
    top:700px;
    left: -500px;
    animation: spin 2s infinite linear ;
    animation-delay: 3s;
    animation-iteration-count:1;
    animation-fill-mode: forwards
  }
  .title4{
    color: white;
    font-size: 32px;
    position: absolute;
    top:800px;
    left: -500px;
    animation: spin 2s infinite linear ;
    animation-delay: 4s;
    animation-iteration-count:1;
    animation-fill-mode: forwards
  }
  .title5{
    color: white;
    font-size: 32px;
    position: absolute;
    top:900px;
    left: -500px;
    animation: spin 2s infinite linear ;
    animation-delay: 5s;
    animation-iteration-count:1;
    animation-fill-mode: forwards
  }
  @keyframes spin1{
    from { transform: translateX(0) translateY(0); }
    to { transform: translateX(0px) translateY(-380px);}
}
  .title6{
    color: white;
    font-size: 40px;
    position: absolute;
    bottom: -200px;
    left: 50px;
    animation: spin1 2s infinite linear ;
    animation-delay: 6.5s;
    animation-iteration-count:1;
    animation-fill-mode: forwards
  }
</style>
<style>
  .van-swipe__track {
    height: 100%;
  }

  .van-swipe__indicators {
    display: none
  }
</style>