<template>
  <b-card no-body class="mb-1" >
    <b-tabs card fill>
      <b-tab v-for="i in 7" :title="dagen[i-1]" :active="(i == 1) ? true : undefined">
        <b-card-text no-body>
          <b-list-group flush>
            <Lamp v-for="j in 7" :nummer="j" stand="automatisch" :dag="i" />    
          </b-list-group>
        </b-card-text>
      </b-tab>
    </b-tabs>
  </b-card>
</template>

<script>
export default {
  props: [
    'profiel'
  ],
  data() {
    return {
      dagen: ["Ma", "Di", "Wo", "Do", "Vr", "Za", "Zo"],
    }
  }
}
</script>