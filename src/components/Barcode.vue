<template>
  <qrcode-stream @decode="$emit('decode', $event)" />
</template>
<script>
import { QrcodeStream } from "vue-qrcode-reader";
export default {
  name: "Barcode",
  components: {
    QrcodeStream,
  },
};
</script>