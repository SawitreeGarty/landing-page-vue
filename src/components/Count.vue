<template>
  <div id="count-section">
    <b-container class="bv-example-row">
      <b-row>
        <b-col class="col-num" sm>
          <div class="number counter-no-loop"></div>
          <div class="desc-num">CLIENTS</div>
        </b-col>
        <b-col class="col-num" sm>
          <div class="number counter-loop"></div>
          <div class="desc-num">PROJECT</div>
        </b-col>
        <b-col class="col-num" sm>
          <div class="number counter-loop-countdown"></div>
          <div class="desc-num">AWARDS</div>
        </b-col>
        <b-col class="col-num" sm>
          <div class="number">34</div>
          <div class="desc-num">TEAM</div>
        </b-col>
      </b-row>
    </b-container>
  </div>
</template>

<script>
export default {
  name: "CountComponent",
};
</script>

<style lang="scss" scope>
#count-section {
  background-image: url("../images/working.webp");
  padding: 80px 0;
  background-position: center center;
  position: relative;
  text-align: center;
  &:after {
    content: "";
    position: absolute;
    left: 0;
    top: 0;
    background: rgba(0, 0, 0, 0.7);
    width: 100%;
    height: 100%;
  }
  .col-num {
    position: relative;
    z-index: 9;
    color: #fff;
    .number {
      font-weight: 900;
      font-size: 40px;
      letter-spacing: 0.3px;
    }
    .desc-num {
      font-size: 13px;
      font-weight: 900;
      letter-spacing: 1px;
    }
  }
}

@property --num {
  syntax: "<integer>";
  initial-value: 0;
  inherits: false;
}

.counter-loop {
  animation: counter 5s infinite ease-in-out;
  counter-reset: num var(--num);
  &:after {
    content: counter(num);
  }
}

.counter-no-loop {
  animation: counter-no-loop 20s ease-in-out;
  counter-reset: num var(--num);
  &:after {
    content: counter(num);
  }
}

.counter-loop-countdown {
  animation: countdown 5s infinite alternate ease-in-out;
  counter-reset: num var(--num);
  &:after {
    content: counter(num);
  }
}

@keyframes counter {
  from {
    --num: 0;
  }
  to {
    --num: 154;
  }
}
@keyframes countdown {
  from {
    --num: 0;
  }
  to {
    --num: 59;
  }
}

@keyframes counter-no-loop {
  from {
    --num: 0;
  }
  to {
    --num: 1054;
  }
}

@media screen and (max-width: 767px) {
  #count-section{
    padding: 80px 0 40px;
    .col-num{
      padding-bottom: 40px;
    }
  }
}
</style>
