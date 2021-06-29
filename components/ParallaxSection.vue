<template>
  <div class="parallax-bg">
    <div class="parallax-haze" />
  </div>
</template>

<style>
.parallax-bg {
  background-image: url('/top-banner.jpg');
  background-attachment: fixed;
  background-repeat: no-repeat;
  background-size: cover;
  /*filter: blur(8px) saturate(30%);
  -webkit-filter: blur(8px) saturate(30%);*/

  position: relative;
  padding: 8rem 0;
}

.parallax-haze {
  background-color: #be3131;
  position: absolute;
  top: 0;
  left: 0;
  height: 100%;
  width: 100%;
  opacity: 0.7;
}
</style>
