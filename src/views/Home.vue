<template>
  <div class="home">
    <!-- 轮播图 -->
    <div class="swiper-container">
      <div class="description absolute-el">Lorem ipsum dolor sit amet consectetur adipisicing elit. Nam facilis minus fugiat ut, amet obcaecati vero</div>
      <div class="detail-btn absolute-el">我要求婚</div>
      <el-carousel :interval="5000" arrow="always" height='500px'>
        <el-carousel-item v-for="item in swiperList" :key="item">
          <img :src="item" class="swiper_image">
        </el-carousel-item>
      </el-carousel>
    </div>
    <div class="center">
      <!-- 精选案例 -->
      <HomeTitle cnTitle='精选案例' enTitle='Selected case' />
      <div class="selected-case">
        <div class="case-item" v-for="(item,index) in 4" :key="index" :style="index>1?'margin-top:30px':''"></div>
      </div>
      <!-- 热门套餐 -->
      <HomeTitle cnTitle='热门套餐' enTitle='Hot meals' />
    </div>
    <!-- 提交手机号码-->
    <div class="submit">
      <div class="form">
        <div class="name">
          <p class="cn-title">您的姓名</p>
          <p class="en-title">name</p>
          <el-input v-model="name" placeholder="姓名"></el-input>
        </div>
        <div class="tel">
          <p class="cn-title">输入手机号码立即提交</p>
          <p class="en-title">Contact Information</p>
          <el-input v-model="tel" placeholder="手机"></el-input>
        </div>
      </div>
      <div class="submit-btn text-center">提交预约</div>
    </div>

    <div class="center">
      <!-- 地点 -->
      <div class="place-container" style="margin-top:30px">
        <div class="place-item" v-for='item in 3' :key="item">
        </div>
      </div>
      <div class="place-container" style="margin-top:15px">
        <div class="place-item" v-for='item in 3' :key="item">
        </div>
      </div>
      <!-- 高端定制 -->
      <HomeTitle cnTitle='高端定制' enTitle='High-end custom' />
      <div class="high-end">
        <div class="high-end-item" v-for="item in 2" :key='item'>
        </div>
      </div>
      <div class="high-end" style="margin-top:20px">
        <div class="high-end-item" v-for="item in 2" :key='item'>
        </div>
      </div>
    </div>

    <div class="steps">

    </div>

    <div class="center">
      <HomeTitle cnTitle='客户评价' enTitle='Customer Evaluation' />
      
    </div>
  </div>
</template>

<script>
// @ is an alias to /src
import HomeTitle from '@/components/HomeTitle.vue'
export default {
  name: 'Home',
  data() {
    return {
      swiperList:['https://ss0.bdstatic.com/94oJfD_bAAcT8t7mm9GUKT-xh_/timg?image&quality=100&size=b4000_4000&sec=1585536106&di=56b60f028f0d078f95c4a91bf2127cc1&src=http://pic.vjshi.com/2016-12-02/3316441f8d25bd71d321965899d0221e/00003.jpg?x-oss-process=style/watermark','https://timgsa.baidu.com/timg?image&quality=80&size=b9999_10000&sec=1585546191773&di=df2154696ca491aca1fb9943fe2f860a&imgtype=0&src=http%3A%2F%2Fimg.jk51.com%2Fimg_jk51%2F62578618.jpeg'],
      caseList:[],
      name:''
    }
  },
  components: {
    HomeTitle
  },
  methods: {

  },
}
</script>
<style lang="scss">
  .text-center{
    text-align: center;
  }
  .swiper-container{
    position: relative;
    .swiper_image{
      width: 100%;
      height: 100%;
    }
    .description{
      width: 100%;
      text-align: center;
      top: 200px;
      color: #fff;
    }
    .detail-btn{
      width: 200px;
      height: 50px;
      top: 280px;
      border: 2px solid #666;
      line-height: 50px;
      text-align: center;
      border-radius: 5px;
      color: #666;
      font-size: 20px;
      transition: all 0.7s;
      &:hover{
        cursor: pointer;
        border: 2px solid #fff;
        color: #fff;
      }
    }
    .absolute-el{
      z-index: 10;
      position: absolute;
      left: 0;
      right: 0;
      margin: 0 auto;
    }
  }
  .center{
    width: 800px;
    margin: 0 auto;
    .selected-case{
      display: flex;
      justify-content: space-between;
      flex-wrap: wrap;
      .case-item{
        width: 45%;
        height: 200px;
        background-color: red;
      }
    }
    .place-container{
      display: flex;
      flex-wrap: wrap;
      justify-content: space-between;
      .place-item{
        width: 250px;
        height: 200px;
        border: 1px solid #000;
      }
    }
    .high-end{
      display: flex;
      justify-content: space-between;
      .high-end-item{
        width: 390px;
        height: 245px;
        border: 1px solid #000;
      }

    }
  }
  .submit{
    width: 100vw;
    height: 225px;
    border: 1px solid #000;
    display: flex;
    justify-content: center;
    align-items: center;
    .form{
      width: 500px;
      height: 110px;
      border: 1px solid #000;
      display: flex;
      >div{
        width: 50%;
        height: 100%;
      }
      input{
        margin-left: 10px;
        margin-top: 15px;
        width: 80%;
      }
      .cn-title{
        line-height: 18px;
        margin-left: 10px;
        font-size: 18px;
      }
      .en-title{
        margin-top: 16px;
        line-height: 12px;
        margin-left: 10px;
        font-size: 12px;
      }
    }
    .submit-btn{
      width: 325px;
      height: 90px;
      margin-left: 150px;
      line-height: 90px;
      font-size: 20px;
      color: #fff;
      cursor: pointer;
      background: linear-gradient(to right, #f4749b, #951586);
      opacity: 0.7;
      transition: all 0.5s;
      user-select: none;
      &:hover{
        opacity: 1;
      }
    }
  }
  .steps{
    width: 100vw;
    height: 240px;
    border: 1px solid #000;
    margin-top: 60px;
  }
</style>
