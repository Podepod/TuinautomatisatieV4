<template>
  <b-form-select class="mb-1" v-model="huidigGekozenProfiel" :options="profielen "></b-form-select>
</template>

<script>
export default {
  data () {
    return {
      huidigGekozenProfiel: "default",
      profielen: [
        "default",
        "winter",
        "zomer",
        "feest"
      ]
    }
  }
}
</script>