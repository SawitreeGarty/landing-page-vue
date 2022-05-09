<template>
  <div id="foooter">
    © 2020 <span class="bold-text"><b-icon icon="code-slash"></b-icon> Developer.</span> All Rights Reserved.
  </div>
</template>

<script>
export default {
  name: "FooterComponent",
};
</script>

<style lang="scss" scope>
#foooter {
  padding: 60px;
  color: #999;
  font-weight: 500;
  font-size: 15px;
  letter-spacing: 1px;
  .bold-text{
    color: #000;
  }
}
</style>
