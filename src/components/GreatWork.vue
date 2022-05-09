<template>
  <div id="greatwork-section">
    <div class="title">GREAT WORK</div>
    <div class="tab">
      <div class="all-tab">
        <span
          class="menu-tab"
          v-bind:class="{ active: active_tab === 'all' }"
          v-on:click="selectTab('all')"
          >ALL</span
        >
        <span
          class="menu-tab"
          v-bind:class="{ active: active_tab === 'branding' }"
          v-on:click="selectTab('branding')"
          >BRANDING</span
        >
        <span
          class="menu-tab"
          v-bind:class="{ active: active_tab === 'design' }"
          v-on:click="selectTab('design')"
          >DESIGN</span
        >
        <span
          class="menu-tab"
          v-bind:class="{ active: active_tab === 'photo' }"
          v-on:click="selectTab('photo')"
          >PHOTO</span
        >
        <span
          class="menu-tab"
          v-bind:class="{ active: active_tab === 'coffee' }"
          v-on:click="selectTab('coffee')"
          >COFFEE</span
        >
      </div>
      <div class="content-tab">
        <b-row>
          <b-col
            class="imgGallery"
            v-for="(item, index) in showImg"
            :key="index"
            v-bind:style="{ 'background-image': 'url(' + item + ')' }"
          ></b-col>
        </b-row>
      </div>
    </div>
  </div>
</template>

<script>
import imgBranding from "../images/branding.jpeg";
import imgBranding2 from "../images/branding2.jpeg";
import imgDesign from "../images/design.jpeg";
import imgDesign2 from "../images/design2.jpeg";
import imgPhoto from "../images/photo.jpeg";
import imgPhoto2 from "../images/photo2.jpeg";
import imgCoffee from "../images/coffee.png";
import imgCoffee2 from "../images/coffee2.webp";

export default {
  name: "GreatWorkComponent",
  data() {
    return {
      active_tab: "all",
      listImg: [
        { nameImg: imgBranding, menu: "branding" },
        { nameImg: imgBranding2, menu: "branding" },
        { nameImg: imgDesign, menu: "design" },
        { nameImg: imgDesign2, menu: "design" },
        { nameImg: imgPhoto, menu: "photo" },
        { nameImg: imgPhoto2, menu: "photo" },
        { nameImg: imgCoffee, menu: "coffee" },
        { nameImg: imgCoffee2, menu: "coffee" },
      ],
      showImg: [
        imgBranding,
        imgBranding2,
        imgDesign,
        imgDesign2,
        imgPhoto,
        imgPhoto2,
        imgCoffee,
        imgCoffee2,
      ],
    };
  },
  methods: {
    selectTab(tab) {
      this.active_tab = tab;
      this.showImg = [];
      this.listImg.forEach((filter) => {
        if (tab === "all") {
          this.showImg.push(filter.nameImg);
        } else {
          if (tab === filter.menu) {
            this.showImg.push(filter.nameImg);
          }
        }
      });
    },
  },
};
</script>

<style lang="scss" scope>
#greatwork-section {
  .title {
    font-size: 20px;
    padding-top: 120px;
    padding-bottom: 50px;
    font-weight: 700;
    letter-spacing: 1px;
  }
  .tab {
    .all-tab {
      padding-bottom: 40px;
      .menu-tab {
        font-size: 12px;
        letter-spacing: 1px;
        padding: 0 20px;
        font-weight: 700;
        cursor: pointer;
        &.active {
          color: #ff9933;
        }
      }
    }
    .content-tab {
      overflow: hidden;
      .imgGallery {
        height: 300px;
        background-position: center center;
        min-width: 300px;
        background-size: cover;
      }
      .img-tab {
        max-width: 430px;
      }
    }
  }
}
@media screen and (max-width: 767px) {
  #greatwork-section{
    .title{
      padding-top: 80px;
    }
    .tab { 
      .all-tab {
        .menu-tab{
          padding: 0 12px;
        }
      }
    }
  }
}
</style>
