<template>
  <div class="home">
    <h1>Heal Minded</h1>
    <h2>A therapeutical digital experience<br />to help you feel better</h2>
    <BreathingCircle />
    <Button />
  </div>
</template>

<script>
// @ is an alias to /src
import Button from "@/components/Button.vue";
import BreathingCircle from "../components/BreathingCircle.vue";

export default {
  name: "Home",
  components: {
    Button,
    BreathingCircle,
  },
};
</script>
