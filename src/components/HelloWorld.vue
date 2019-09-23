<template>
  <div class="hello">
    <van-swipe style="height: 100%" vertical :loop='false' @change="onChange">
      <van-swipe-item>
        <div class="first">
          <!-- <img src="../assets/1.jpg.jpg" alt="" :class="{'img':this.class[0].show}"> -->
          firstapp
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

  .img {
    width: 100%
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