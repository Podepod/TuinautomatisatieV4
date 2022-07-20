<template>
  <div>
    <div v-if="!opSensorPagina" class="accordion" role="tablist">
      <b-card no-body class="mb-1">
        <b-collapse id="accordion-1" accordion="my-accordion" role="tabpanel">
          <b-card-body>
            <b-list-group flush>
              <b-list-group-item v-for="sensor in sensoren">
                <b-row>
                  <b-col>{{ sensor.naam }}</b-col>
                  <b-col>{{ sensor.prefix }}{{ sensor.waarde }}{{ sensor.suffix }}</b-col>
                </b-row>
              </b-list-group-item>
            </b-list-group>
          </b-card-body>
        </b-collapse>
        <b-card-footer class="p-1" role="tab">
          <b-button block v-b-toggle.accordion-1>
            Sensor Waarden
          </b-button>
        </b-card-footer>
      </b-card>
    </div>
    <div v-else>
      <h3>Laatste sensor waarden</h3>
      <b-list-group>
        <b-list-group-item v-for="sensor in sensoren">
          <b-row>
            <b-col>{{ sensor.naam }}</b-col>
            <b-col>{{ sensor.prefix }}{{ sensor.waarde }}{{ sensor.suffix }}</b-col>
          </b-row>
        </b-list-group-item>
      </b-list-group>
    </div>
  </div>
</template>

<script>
export default {
  props: [
    'opSensorPagina'
  ],
  data() {
    return {
      sensoren: [
        {
          naam: "Temperatuur",
          prefix: "",
          suffix: "°C",
          waarde: 37
        },
        {
          naam: "Poort",
          prefix: "",
          suffix: "",
          waarde: "Open"
        },
        {
          naam: "Licht",
          prefix: "",
          suffix: "",
          waarde: "12000"
        }
      ]
    }
  }
}
</script>