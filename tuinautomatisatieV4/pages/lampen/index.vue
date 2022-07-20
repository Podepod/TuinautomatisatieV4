<template>
  <div>
    <NavbarLG class="mb-1" />
    <b-container>
      <PoortAlert />

      <h1>Lampen</h1>
      <ManueleLampen v-if="stand == 'manueel'" class="mb-1" />
      <AutomatischeLampen v-else class="mb-1" />

      <LampenButtonBar :manueel="stand == 'manueel'" />

      <LaatsteSensorWaarde />
    </b-container>
  </div>
</template>

<script>
export default {
    name: "LampenPage",
    data() {
      return {
        stand: "automatisch"
      }
    }
}
</script>
