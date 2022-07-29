<template>
  <div>
    <NavbarLG />
    <b-container>
      <PoortAlert />
      
      <h1>Profielen</h1>

      <b-list-group class="mb-1">
        <LampProfielListItem v-for="p in profielen.length" :nummer="p" :naam="profielen[p-1]" :isDefault="(p-1 == 0) ? true : false" :isActief="(profielen[p-1] == huidigGekozenProfiel) ? true : false" />    
      </b-list-group>

      <LaatsteSensorWaarde />
    </b-container>
  </div>
</template>

<script>
export default {
  name: 'ProfielenPage',
  data() {
    return {
      huidigGekozenProfiel: "winter",
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
