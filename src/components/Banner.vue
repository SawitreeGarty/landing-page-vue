<template>
  <div id="banner">
    <div class="box-text-banner">
      <div class="title">DEVERLOPMENT</div>
      <div class="desc">We are web deverloper</div>
      <div class="box-btn">
        <div class="btn-banner btn-read">READ ME</div>
        <div class="btn-banner">LEARN MORE</div>
      </div>
    </div>
    <b-carousel
      id="carousel-no-animation"
      style="text-shadow: 0px 0px 2px #000"
      no-animation
      indicators
      img-width="1024"
      img-height="768"
      v-model="slide"
      :interval="50000"
    >
      <b-carousel-slide :img-src="imgBanner"></b-carousel-slide>
      <b-carousel-slide :img-src="imgBanner2"></b-carousel-slide>
      <b-carousel-slide :img-src="imgBanner3"></b-carousel-slide>
    </b-carousel>
  </div>
</template>

<script>
import imgBanner from "../images/img-code.jpeg";
import imgBanner2 from "../images/img-code4.webp";
import imgBanner3 from "../images/img-code3.jpeg";
export default {
  name: "BannerComponent",
  data() {
    return {
      slide: 0,
      imgBanner: imgBanner,
      imgBanner2: imgBanner2,
      imgBanner3: imgBanner3,
    };
  },
  methods: {},
};
</script>

<style lang="scss" scope>
#banner {
  position: relative;
  .box-text-banner {
    text-align: center;
    color: #fff;
    position: absolute;
    top: 50%;
    left: 50%;
    z-index: 99;
    transform: translate(-50%, -50%);
    .title {
      font-size: 30px;
      letter-spacing: 10px;
      font-weight: 700;
    }
    .desc {
      font-size: 18px;
      margin-top: 15px;
      margin-bottom: 30px;
      color: #fff;
      font-weight: 500;
    }
    .box-btn {
      .btn-banner {
        width: 120px;
        height: 35px;
        border: 2.5px solid #fff;
        border-radius: 2px;
        display: inline-block;
        font-size: 13px;
        line-height: 33px;
        font-weight: 900;
        letter-spacing: 0.3px;
        margin: 0 5px;
        cursor: pointer;
        &:hover {
          background: #fff;
          color: #000;
        }
      }
    }
  }
  .carousel-item {
    &:after {
      content: "";
      position: absolute;
      left: 0;
      top: 0;
      width: 100%;
      height: 100%;
      background: rgba(0, 0, 0, 0.3);
    }
  }
  .carousel-indicators {
    li {
      box-sizing: content-box;
      -ms-flex: 0 1 auto;
      flex: 0 1 auto;
      width: 30px;
      height: 3px;
      margin-right: 3px;
      margin-left: 3px;
      text-indent: -999px;
      cursor: pointer;
      background-color: #fff;
      background-clip: padding-box;
      border-top: 10px solid #0000;
      border-bottom: 10px solid #0000;
      opacity: 0.5;
      transition: opacity 0.6s ease;
      &.active {
        opacity: 1;
      }
    }
  }
}
@media screen and (max-width: 767px) {
  #banner {
    .box-text-banner {
      .title {
        font-size: 23px;
        letter-spacing: 0;
      }
      .desc {
        font-size: 18px;
        margin-top: 5px;
        margin-bottom: 15px;
      }
      .box-btn {
        .btn-banner {
          background: #fff;
          color: #000;
          &.btn-read {
            display: none;
          }
        }
      }
    }
  }
}
</style>
