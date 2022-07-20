<template>
  <div>
    <b-row class="mb-1">
      <b-col>
        <b-button v-if="manueel" variant="info">Zet de lampen op automatisch</b-button>
        <b-button v-else variant="info">Zet de lampen op manueel</b-button>
      </b-col>
    </b-row>

    <b-row class="mb-1">
      <b-col>
        <b-button-group>
          <b-button variant="success">Alles Aan</b-button>
          <b-button variant="danger">Alles Uit</b-button>
          <b-button v-if="manueel" variant="warning">Alles Sensor</b-button>
        </b-button-group>
      </b-col>
    </b-row>

    <b-row class="mb-1">
      <b-col v-if="!manueel">
        <b-button-group>
          <b-button variant="outline-success">Alles Aan (/dag)</b-button>
          <b-button variant="outline-danger">Alles Uit (/dag)</b-button>
        </b-button-group>
      </b-col>
    </b-row>
  </div>
</template>


<script>
export default {
    props: [
        'manueel'
    ]
}
</script>