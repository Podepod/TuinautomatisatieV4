<template>
  <b-list-group class="mb-1">
    <b-list-group-item variant="primary">
      <b-row>
        <b-col><b>Datum</b></b-col>
        <b-col><b>Tijd</b></b-col>
        <b-col><b>Waarde {{sensor}}</b></b-col>
      </b-row>
    </b-list-group-item>
    <b-list-group-item v-for="i in aantalWaarden" :variant="(i % 2 == 0) ? 'light' : 'default'" >
      {{ waarden[i] }}
    </b-list-group-item>
  </b-list-group>
</template>

<script>
  export default {
    props: [
      'sensor',
    ],
    data() {
      return {
        'aantalWaarden': 4,
        'prefix': '',
        'suffix': '°',
        'waarden': [
          0,
          0,
          0,
          0,

          0,
          0,
          0,
          0,

          0,
          0,
          0,
          0,

          0,
          0,
          0,
          0
        ]
      }
    }
  }
</script>