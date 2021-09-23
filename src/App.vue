<template>
  <div id="app" class="container">
    <h1>QRCode Reader</h1>

    <p>{{ barcode }}</p>

    <Barcode @decode="decode" />
  </div>
</template>

<script>
import Barcode from "./components/Barcode.vue";

export default {
  name: "App",
  components: {
    Barcode,
  },
  data() {
    return {
      barcode: "",
    };
  },
  methods: {
    decode(value) {
      this.barcode = value;
    },
  },
};
</script>

<style>
.container {
  width: 80vw;
  margin: 0 auto;
}
</style>
