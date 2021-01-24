<template>
  <div class="breathing-circle"></div>
</template>

<style lang="scss" scoped>
$size: 90px;
$scale: 2;

// GENERAL BUTTON
.breathing-circle {
  width: $size;
  height: $size;
  background: #ccc;
  position: relative;
  border-radius: 50%;
  margin: 80px auto;

  &::after {
    content: "";
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%) scale($scale);
    transform-origin: center;
    background: #eee;
    border-radius: 50%;
    width: 100%;
    height: 100%;
    z-index: -2;
  }

  &::before {
    content: "";
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%) scale($scale);
    transform-origin: center;
    background: #ddd;
    border-radius: 50%;
    width: 100%;
    height: 100%;
    z-index: -1;
    animation-name: breathe;
    animation-duration: 8s;
    animation-iteration-count: infinite;
  }
}

@keyframes breathe {
  0% {
    transform: translate(-50%, -50%) scale(1);
  }

  50% {
    transform: translate(-50%, -50%) scale($scale);
  }

  100% {
    transform: translate(-50%, -50%) scale(1);
  }
}
</style>
