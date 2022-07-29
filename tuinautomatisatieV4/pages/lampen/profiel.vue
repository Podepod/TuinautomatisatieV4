<template>
  <div>
    <NavbarLG />
    <b-container>
      <PoortAlert />
      
      <h1>Profielen</h1>

      <AutomatischeLampen :profiel="huidigGekozenProfiel" />

      <LaatsteSensorWaarde />
    </b-container>
  </div>
</template>

<script>
export default {
  name: 'ProfielPage',
}
</script>
