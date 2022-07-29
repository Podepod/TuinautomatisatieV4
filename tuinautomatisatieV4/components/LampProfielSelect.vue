<template>
  <b-form-select class="mb-1" v-if="stand != 'manueel'" v-model="huidigGekozenProfiel" :options="profielen "></b-form-select>
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