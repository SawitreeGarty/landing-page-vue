<template>
  <div id="service-section">
    <b-container class="bv-example-row">
      <b-row>
        <div class="title">SERVICE</div>
      </b-row>

      <b-row>
        <b-col class="box-service" sm>
          <b-icon icon="pencil-square"></b-icon>
          <div class="title-service">WEB DESIGN</div>
          <div class="desc">
            Maecenas tempus, tellus eget condimentum rhoncus, sem quam semper
            libero, sit amet adipiscing sem.
          </div>
        </b-col>
        <b-col class="box-service" sm>
          <b-icon icon="gear"></b-icon>
          <div class="title-service">DEVELOPMENT</div>
          <div class="desc">
            Donec sodales sagittis magna. hendrerit id, lorem. Maecenas nec odio
            et ante tincidunt tempus, augue velit cursus nunc.
          </div>
        </b-col>
        <b-col class="box-service" sm>
          <svg
            width="30"
            xmlns="http://www.w3.org/2000/svg"
            viewBox="0 0 384 512"
          >
            <path
              d="M318.7 268.7c-.2-36.7 16.4-64.4 50-84.8-18.8-26.9-47.2-41.7-84.7-44.6-35.5-2.8-74.3 20.7-88.5 20.7-15 0-49.4-19.7-76.4-19.7C63.3 141.2 4 184.8 4 273.5q0 39.3 14.4 81.2c12.8 36.7 59 126.7 107.2 125.2 25.2-.6 43-17.9 75.8-17.9 31.8 0 48.3 17.9 76.4 17.9 48.6-.7 90.4-82.5 102.6-119.3-65.2-30.7-61.7-90-61.7-91.9zm-56.6-164.2c27.3-32.4 24.8-61.9 24-72.5-24.1 1.4-52 16.4-67.9 34.9-17.5 19.8-27.8 44.3-25.6 71.9 26.1 2 49.9-11.4 69.5-34.3z"
            />
          </svg>
          <div class="title-service">BRANDING</div>
          <div class="desc">
            At vero eos et accusamus et iusto odio dignissimos ducimus qui
            blanditiis praesentium voluptatum deleniti atque.
          </div>
        </b-col>
      </b-row>

      <b-row>
        <b-col class="box-service" sm>
          <b-icon icon="pencil-square"></b-icon>
          <div class="title-service">PHOTOGRAPHY</div>
          <div class="desc">
            Excepturi sint occaecati cupiditate non provident. similique sunt in
            culpa qui officia deserunt mollitia animi. id est laborum et dolorum
            fuga.
          </div>
        </b-col>
        <b-col class="box-service" sm>
          <b-icon icon="gear"></b-icon>
          <div class="title-service">TYPOGRAPHY</div>
          <div class="desc">
            Et harum quidem rerum facilis est et expedita distinctio. Nam libero
            tempore, cum soluta nobis est eligendi optio cumque nihil.
          </div>
        </b-col>
        <b-col class="box-service" sm>
          <svg
            width="30"
            xmlns="http://www.w3.org/2000/svg"
            viewBox="0 0 384 512"
          >
            <path
              d="M318.7 268.7c-.2-36.7 16.4-64.4 50-84.8-18.8-26.9-47.2-41.7-84.7-44.6-35.5-2.8-74.3 20.7-88.5 20.7-15 0-49.4-19.7-76.4-19.7C63.3 141.2 4 184.8 4 273.5q0 39.3 14.4 81.2c12.8 36.7 59 126.7 107.2 125.2 25.2-.6 43-17.9 75.8-17.9 31.8 0 48.3 17.9 76.4 17.9 48.6-.7 90.4-82.5 102.6-119.3-65.2-30.7-61.7-90-61.7-91.9zm-56.6-164.2c27.3-32.4 24.8-61.9 24-72.5-24.1 1.4-52 16.4-67.9 34.9-17.5 19.8-27.8 44.3-25.6 71.9 26.1 2 49.9-11.4 69.5-34.3z"
            />
          </svg>
          <div class="title-service">UI DESIGN</div>
          <div class="desc">
            Sed fringilla mauris sit amet nibh. Donec sodales sagittis magna.
            Sed consequat, leo eget bibendum sodales.
          </div>
        </b-col>
      </b-row>
    </b-container>
  </div>
</template>

<script>
export default {
  name: "ServiceComponent",
};
</script>

<style lang="scss" scope>
#service-section {
  padding: 120px 0;
  .title {
    text-align: center;
    font-size: 20px;
    letter-spacing: 5px;
    font-weight: 500;
    padding-bottom: 50px;
  }
  .box-service {
    padding: 0 25px 40px;
    .title-service {
      padding: 30px 0 10px;
      font-weight: 500;
      letter-spacing: 1px;
    }
    .desc {
      font-size: 15px;
      line-height: 20px;
      color: #999;
      font-weight: 500;
    }
  }
  .b-icon.bi {
    font-size: 40px;
  }
}
@media screen and (max-width: 767px) {
  #service-section {
    padding: 80px 0;
    .box-service{
      padding: 0 20px 40px;
    }
  }
}
</style>
