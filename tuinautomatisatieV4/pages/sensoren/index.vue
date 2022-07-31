<template>
  <div>
    <NavbarLG />
    <b-container>
      <PoortAlert />

      <h1>Sensoren</h1>
      <LaatsteSensorWaarde :opSensorPagina="true" />

      <h2>Temperatuur</h2>
      <SensorLijst sensor="temperatuur" />

      <h2>Licht</h2>
      <SensorLijst sensor="licht" />

      <h2>Poort</h2>
      <SensorLijst sensor="poort" />

</b-container>
  </div>
</template>

<script>
export default {
    name: "SensorenPage"
}
</script>
