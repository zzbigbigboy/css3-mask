<style lang="scss">
.content_body {
  width: 100%;
  height: 100vh;
  background: url("~@/assets/icons/bg.jpg") no-repeat;
  background-position: center;
}

.notching {
  margin: auto;
  position: absolute;
  top: 0;
  width: 400px;
  height: 240px;
  background: url("~@/assets/icons/img2.jpg");
  background-size: cover;
  
  mask-size: 50% 50%;
  mask-repeat: no-repeat;

  &::before {
    position: absolute;
    content: '';
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    background: url("~@/assets/icons/img1.jpg");
    background-size: cover;
    // mask: conic-gradient(#000 15%, transparent 30%, transparent);
    // mask: linear-gradient( 90deg, #000 50%, transparent 60%, transparent 100%);
    animation: maskRotate 5s infinite linear;
    // mask: conic-gradient(#000 50}, transparent #{$i + '%'}, transparent);
  }
}

@keyframes maskRotate {
    @for $i from 0 through 100 {
        #{$i}% {
            // mask: conic-gradient(#000 #{$i - 10 + '%'}, transparent #{$i + '%'}, transparent);
            // mask: linear-gradient(0deg, #000 #{$i + '%'}, transparent #{$i + 5 + '%'}, transparent 1%);
            mask: linear-gradient( #{$i * 3.6 + 'deg'}, #000 45%, transparent 55%, transparent 1%);
        }
    }
}
</style>

<template>
  <div class="content_body">
    <!-- <div class="mask_bg"></div> -->
    <div class="notching"></div>
  </div>
</template>

<script>
export default {
  name: "HelloWorld",
  props: {
    msg: String,
  },
};
</script>