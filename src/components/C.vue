<style lang="scss">
.content_bodyC {
  .box {
    position: relative;
    width: 600px;
    height: 360px;
  }

  .img1 {
    background: url("~@/assets/icons/img1.jpg") no-repeat left top;
    background-size: cover;
    height: 100%;
    position: absolute;
    left: 0;
    top: 0;
    width: 100%;
  }

  .img2 {
    position: absolute;
    height: 100%;
    width: 100%;
    left: 0;
    top: 0;
    mask: url("~@/assets/icons/n.png");
    mask-size: 3000% 100%;
    animation: maskMoveC 2s steps(29) infinite;
  }

  .img2::before {
    content: "";
    position: absolute;
    top: 0;
    left: 0;
    height: 100%;
    width: 100%;
    background: url("~@/assets/icons/img2.jpg") no-repeat left top;
    background-size: cover;
  }

  @keyframes maskMoveC {
    from {
      mask-position: 0 0;
    }
    to {
      mask-position: 100% 0;
    }
  }
}
// @keyframes maskRotate {
//     @for $i from 0 through 100 {
//         #{$i}% {
//             // mask: conic-gradient(#000 #{$i - 10 + '%'}, transparent #{$i + '%'}, transparent);
//             // mask: linear-gradient(0deg, #000 #{$i + '%'}, transparent #{$i + 5 + '%'}, transparent 1%);
//             mask: linear-gradient( #{$i * 3.6 + 'deg'}, #000 45%, transparent 55%, transparent 1%);
//         }
//     }
// }
</style>

<template>
  <div class="content_bodyC">
    <div class="box">
      <div class="img1"></div>
      <div class="img2"></div>
    </div>
  </div>
</template>

<script>
export default {
  name: "C",
  props: {
    msg: String,
  },
};
</script>