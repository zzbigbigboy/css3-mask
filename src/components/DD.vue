<style lang="scss">
.content_bodyD {
  width: 100vw;
  .box {
    position: relative;
    width: 600px;
    height: 360px;
    margin: 10px auto;
  }

  .notching {
    margin: auto;
    position: absolute;
    top: 0;
    width: 100%;
    height: 100%;
    background: url("~@/assets/icons/img2.jpg");
    background-size: cover;

    mask-size: 50% 50%;
    mask-repeat: no-repeat;

    &::before {
      position: absolute;
      content: "";
      top: 0;
      left: 0;
      right: 0;
      bottom: 0;
      background: url("~@/assets/icons/img1.jpg");
      background-size: cover;
      // mask: conic-gradient(#000 15%, transparent 30%, transparent);
      // mask: linear-gradient( 90deg, #000 50%, transparent 60%, transparent 100%);
      animation: maskRotateD 5s infinite linear;
      // mask: conic-gradient(#000 50}, transparent #{$i + '%'}, transparent);
    }
  }

  @keyframes maskRotateD {
    @for $i from 0 through 100 {
      #{$i}% {
        // mask: conic-gradient(#000 #{$i - 10 + '%'}, transparent #{$i + '%'}, transparent);
        mask: linear-gradient(45deg, #000 #{$i + '%'}, transparent #{$i + 5 + '%'}, transparent 1%);
      }
    }
  }
}
</style>

<template>
  <div class="content_bodyD">
    <div class="box">
      <div class="notching"></div>
    </div>
  </div>
</template>

<script>
export default {
  name: "DD",
  props: {
    msg: String,
  },
};
</script>