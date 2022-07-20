<template>
  <div class="accordion" role="tablist">
    <b-card no-body class="mb-1">
      <b-card-header header-tag="header" class="p-1" role="tab">
        <b-button block v-b-toggle.accordion-1>
          Sensor Waarden
        </b-button>
      </b-card-header>
      <b-collapse id="accordion-1" accordion="my-accordion" role="tabpanel">
        <b-card-body>
          <b-list-group>
            <b-list-group-item>
              Cras justo odio
              <b-badge variant="primary" pill>14</b-badge>
            </b-list-group-item>
            <b-list-group-item>
              Dapibus ac facilisis in
            </b-list-group-item>
            <b-list-group-item>
              Morbi leo risus
            </b-list-group-item>
          </b-list-group>
        </b-card-body>
      </b-collapse>
    </b-card>
  </div>
</template>
