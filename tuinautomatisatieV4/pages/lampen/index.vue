<template>
  <div>
    <NavbarLG />
    <b-container>
      <PoortAlert />

      <h1>Lampen</h1>
      
      <LampProfielSelect v-if="stand !=  'manueel'" />
      
      <ManueleLampen v-if="stand == 'manueel'" />
      <AutomatischeLampen v-else />

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
