<template>
  <a href="#" class="btn btn-rating">
    <ph-fingerprint :size="48" color="#ccc" weight="fill" />
  </a>
</template>

<script>
import { PhFingerprint } from "phosphor-vue";
export default {
  name: "App",
  components: {
    PhFingerprint,
  },
};
</script>

<style lang="scss" scoped>
// Vars
$white: #fff;
$btnMainBg: #ccc;
$btnMainBorder: $white;
$btnMainHoverBg: #ccc;
$btnMainHoverBorder: #ccc;

$size: 64px;

// GENERAL BUTTON
.btn {
  width: $size;
  height: $size;

  transition: all 0.2s ease;
  display: inline-block;
  font-size: 16px;
  line-height: 1.2;
  text-decoration: none;
  text-transform: uppercase;
  text-align: center;
  margin: 12px;
  border-radius: 50%;
  border: 3px solid #ccc;
  box-shadow: 0 1px 0 0 rgba(255, 255, 255, 0.298039) inset,
    0 -1px 1px 0 rgba(255, 255, 255, 0.14902) inset,
    0 7px 0 0 rgb(187, 187, 187), 0 8px 3px 0 rgba(0, 0, 0, 0.2);

  // Icon
  > svg {
    position: relative;
    top: 6px;
  }

  &.active {
    box-shadow: none;
    transform: translateY(5px);
  }
}
</style>
