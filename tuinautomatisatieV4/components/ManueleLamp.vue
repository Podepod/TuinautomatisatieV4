<template>
  <b-list-group-item>
    <b-row>
      <b-col>
        <h3>Lamp {{ nummer }}</h3>
      </b-col>
      <b-col>
        <b-button-group>
          <b-button variant="outline-success">Aan</b-button>
          <b-button variant="outline-danger">Uit</b-button>
          <b-button variant="outline-warning">Sensor</b-button>
        </b-button-group>
      </b-col>
    </b-row>
  </b-list-group-item>
</template>

<script>
  export default {
    props: [
      'nummer'
    ],
    data() {
      return {
        stand: 0
      }
    }
  }
</script>
