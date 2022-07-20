<template>
  <b-list-group-item>
    <b-row>
      <b-col>
        <h3>
          Lamp {{ nummer }}
        </h3>
      </b-col>
      <b-col>
        <b-button-group>
          <b-button :variant="(status == 1) ? 'success' : 'outline-success'">Aan</b-button>
          <b-button :variant="(status == 0) ? 'danger' : 'outline-danger'">Uit</b-button>
          <b-button v-if="stand == 'manueel'" :variant="(status == 3) ? 'warning' : 'outline-warning'">Sensor</b-button>
        </b-button-group>
      </b-col>
    </b-row>
  </b-list-group-item>
</template>

<script>
  export default {
    props: [
      'nummer',
      'stand',
      'dag'
    ],
    data() {
      return {
        status: 1
      }
    }
  }
</script>
