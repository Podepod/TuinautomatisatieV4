<template>
  <b-list-group-item>
    <b-row>
      <b-col>
        <h3>
          {{ naam[0].toUpperCase() + naam.substring(1) }}
        </h3>
      </b-col>
      <b-col>
        <b-button-group>
          <b-button :variant="(isActief) ? 'outline-success' : 'success'" :disabled="(isActief) ? true : false">Actief Maken</b-button>
          <b-button variant="warning">Aanpassen</b-button>
          <b-button :variant="(isDefault | isActief) ? 'outline-danger' : 'danger'" :disabled="(isDefault | isActief) ? true : false">Verwijderen</b-button>
        </b-button-group>
      </b-col>
    </b-row>
  </b-list-group-item>
</template>

<script>
  export default {
    props: [
      'nummer',
      'naam',
      'isDefault',
      'isActief'
    ]
  }
</script>
