<template lang="">
  <div>
    <div id="pan">
      <div id="pin"></div>
      <!-- <canvas id="canvas" width="1000px" height=""></canvas> -->
    </div>
  </div>
</template>
<script>
export default {
  mounted() {
    var canvas = document.getElementById("canvas");
    var ctx = canvas.getContext("2d");
    ctx.fillStyle = "red";
    ctx.fillRect(0, 0, 100, 100);
  },
};
</script>
<style lang="css">
#pan {
  width: 1000px;
  height: 0;
  overflow: hidden;
  position: relative;
}
#pin {
  width: 0;
  height: 0;
  top: 170px;
  left: calc(50% - 16px);
  position: absolute;
  border-radius: 32px 32px 0 0;
  border-top: 70px solid crimson;
  border-left: 16px solid transparent;
  border-right: 16px solid transparent;
  border-bottom: 0;
  z-index: 1;
}
</style>
