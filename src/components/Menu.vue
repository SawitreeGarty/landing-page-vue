<template>
  <div id="menu-section" :class="{ active: activeBg }">
    <div class="column column-left">
      <div class="logo">
        <b-icon icon="code-slash"></b-icon>
        <span class="text-logo">Deverlop</span>
      </div>
    </div>
    <div class="column column-right">
      <div class="menu-container">
        <div class="menu">
          <span class="menu-name">HOME</span>
          <b-icon icon="chevron-down"></b-icon>
        </div>
        <div class="menu">
          <span class="menu-name">ABOUT US</span>
          <b-icon icon="chevron-down"></b-icon>
        </div>
        <div class="menu" v-scroll-to="'#service-section'">
          <span class="menu-name">SERVICE</span>
          <b-icon icon="chevron-down"></b-icon>
        </div>
        <div class="menu" v-scroll-to="'#greatwork-section'">
          <span class="menu-name">GREAT WORK</span>
          <b-icon icon="chevron-down"></b-icon>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "MenuComponent",
  data() {
    return {
      activeBg: false,
    };
  },
  mounted() {
    window.addEventListener("scroll", this.onScroll);
  },
  beforeDestroy() {
    window.removeEventListener("scroll", this.onScroll);
  },
  methods: {
    onScroll(e) {
      this.windowTop = e.target.documentElement.scrollTop;
      this.activeBg = false;
      if (this.windowTop > 0) {
        this.activeBg = true;
      }
    },
  },
};
</script>

<style lang="scss" scope>
#menu-section {
  position: fixed;
  left: 0;
  top: 0;
  z-index: 9;
  width: 100%;
  padding: 20px;
  &.active {
    background-color: rgba(0, 0, 0, 0.5);
  }
  .column {
    display: inline-block;
    width: 50%;
    vertical-align: middle;
    .logo {
      font-size: 30px;
      color: #fff;
      font-weight: 500;
      .text-logo {
        vertical-align: middle;
        padding-left: 10px;
      }
    }
    .menu-container {
      display: flex;
      justify-content: space-between;
      max-width: 400px;
      .menu {
        display: inline-block;
        cursor: pointer;
        .menu-name {
          color: #fff;
          font-size: 12px;
          font-weight: 900;
          letter-spacing: 0.3px;
          padding-right: 5px;
        }
        .b-icon.bi {
          font-size: 10px;
          color: #c7c7c7;
          vertical-align: 0;
        }
      }
    }
  }
}
@media screen and (max-width: 767px) {
  #menu-section {
    .column {
      &.column-left {
        text-align: left;
        width: 100%;
      }
      &.column-right {
        display: none;
      }
      .logo {
        font-size: 22px;
        color: #fff;
        font-weight: 500;
      }
    }
  }
}
</style>
