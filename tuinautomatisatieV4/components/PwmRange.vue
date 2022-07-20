<template>
  <b-list-group-item>
    <b-row>
      <b-col>
        <h3>{{ pwm.toFixed(0) }}</h3>
      </b-col>
      <b-col>
        <b-form-input
          id="pwm"
          v-model="pwm"
          type="range"
          number
          min="0"
          max="100"
          step="1"
        ></b-form-input>
      </b-col>
    </b-row>
  </b-list-group-item>
</template>

<script>
export default {
  data() {
    return {
      pwm: 10
    }
  }
}
</script>