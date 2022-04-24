<template>
  <main>
    <order-component />
  </main>
</template>

<script lang="ts">
import { defineComponent } from "@vue/runtime-core";
import OrderComponent from "./components/Order/Order.vue";

export default defineComponent({
  name: "App",
  components: { OrderComponent },
});
</script>
<style lang="scss">
@import url("https://fonts.googleapis.com/css2?family=Red+Hat+Display:wght@500;700;900&display=swap");
@import "./assets/main.scss";
body {
  margin: 0px;
  font-family: "Red Hat Display", sans-serif;
}
main {
  background: url("./assets/images/pattern-background-desktop.svg") no-repeat
    center top;
  background-size: contain;
  width: 100%;
  height: 100vh;
  background-color: $pale-blue;
  display: flex;
  justify-content: center;
  align-items: center;
}
</style>
