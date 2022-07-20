<template>
  <div>
    <NavbarLG />
    <b-container>
      <PoortAlert />
      <LaatsteSensorWaarde :opSensorPagina="true" />

      <h1>Sensoren</h1>
    </b-container>
  </div>
</template>

<script>
export default {
    name: "SensorenPage"
}
</script>
