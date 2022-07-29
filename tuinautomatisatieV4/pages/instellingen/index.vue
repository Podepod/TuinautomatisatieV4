<template>
  <div>
    <NavbarLG />
    <b-container>
      <PoortAlert />

      <h1>Instellingen</h1>
      <hr />

      <h2>Meldingen</h2>
      <b-list-group class="mb-1">
        <b-list-group-item>
          <b-row>
            <b-col>Meldingen via E-mail</b-col>
            <b-col>
              <b-button-group>
                <b-button variant="outline-success">Aan</b-button>
                <b-button variant="danger">Uit</b-button>
              </b-button-group>
            </b-col>
          </b-row>
        </b-list-group-item>
        <b-list-group-item>
          <b-row>
            <b-col>Meldingen via Pushbullet</b-col>
            <b-col>
              <b-button-group>
                <b-button variant="success">Aan</b-button>
                <b-button variant="outline-danger">Uit</b-button>
              </b-button-group>
            </b-col>
          </b-row>
        </b-list-group-item>
        <b-list-group-item>
          <b-row>
            <b-col>Meldingen voor poortje</b-col>
            <b-col>
              <b-button-group>
                <b-button variant="outline-success">Aan</b-button>
                <b-button variant="danger">Uit</b-button>
              </b-button-group>
            </b-col>
          </b-row>
        </b-list-group-item>
        <b-list-group-item>
          <b-row>
            <b-col>Lampen voor poortje</b-col>
            <b-col>
              <b-button-group>
                <b-button variant="success">Aan</b-button>
                <b-button variant="outline-danger">Uit</b-button>
              </b-button-group>
            </b-col>
          </b-row>
        </b-list-group-item>
        <b-list-group-item>
          <b-row>
            <b-col>E-mailadres</b-col>
            <b-col>
              <b-input type="email" placeholder="voorbeeld@voorbeeld.be"></b-input>
            </b-col>
          </b-row>
        </b-list-group-item>
        <b-list-group-item>
          <b-row>
            <b-col>Extra e-mailadres</b-col>
            <b-col>
              <b-input type="email" placeholder="voorbeeld@voorbeeld.be"></b-input>
            </b-col>
          </b-row>
        </b-list-group-item>
      </b-list-group>

      <h2>Lampen</h2>
      <b-list-group class="mb-1">
        <b-list-group-item>
          <b-row>
            <b-col>Besturing</b-col>
            <b-col>
              <b-button-group>
                <b-button variant="info">Manueel</b-button>
                <b-button variant="outline-info">Automatisch</b-button>
              </b-button-group>
            </b-col>
          </b-row>
        </b-list-group-item>
        <b-list-group-item>
          <b-row>
            <b-col>Actief profiel</b-col>
            <b-col>
              <LampProfielSelect />
            </b-col>
          </b-row>
        </b-list-group-item>
        <b-list-group-item>
          <b-row>
            <b-col>Lichtdrempel</b-col>
            <b-col>
              <b-input type="number" min="0" value="12000"></b-input>
            </b-col>
          </b-row>
        </b-list-group-item>
        <b-list-group-item>
          <b-row>
            <b-col>Auto uit tijd</b-col>
            <b-col>
              <b-input type="time" value="23:00"></b-input>
            </b-col>
          </b-row>
        </b-list-group-item>
      </b-list-group>

      <h2>Poortdetectie</h2>
      <b-list-group class="mb-1">
        <b-list-group-item>
          <b-row>
            <b-col>Inschakelen</b-col>
            <b-col>
              <b-button-group>
                <b-button variant="outline-success">Aan</b-button>
                <b-button variant="danger">Uit</b-button>
              </b-button-group>
            </b-col>
          </b-row>
        </b-list-group-item>
        <b-list-group-item>
          <b-row>
            <b-col>Inschakel tijd</b-col>
            <b-col>
              <b-input type="time" value="23:00"></b-input>
            </b-col>
          </b-row>
        </b-list-group-item>
        <b-list-group-item>
          <b-row>
            <b-col>Uitschakel tijd</b-col>
            <b-col>
              <b-input type="time" value="23:00"></b-input>
            </b-col>
          </b-row>
        </b-list-group-item>
        <b-list-group-item>
          <b-row>
            <b-col>Tijd dat lampen aan blijven</b-col>
            <b-col>
              <b-input type="number" min="0" value="2"></b-input>
            </b-col>
          </b-row>
        </b-list-group-item>
      </b-list-group>

      <h2>Sensoren</h2>
      <b-list-group class="mb-1">
        <b-list-group-item>
          <b-row>
            <b-col>Toon laatste waarden op andere pagina's</b-col>
            <b-col>
              <b-button-group>
                <b-button variant="success">Aan</b-button>
                <b-button variant="outline-danger">Uit</b-button>
              </b-button-group>
            </b-col>
          </b-row>
        </b-list-group-item>
        <b-list-group-item>
          <b-row>
            <b-col>Hoeveelheid sensor waarden op overzichtpagina</b-col>
            <b-col>
              <b-input type="number" min="0" max="128" value="2"></b-input>
            </b-col>
          </b-row>
        </b-list-group-item>
        <b-list-group-item>
          <b-row>
            <b-col>Hoeveelheid sensor waarden op sensorpagina</b-col>
            <b-col>
              <b-input type="number" min="0" max="128" value="2"></b-input>
            </b-col>
          </b-row>
        </b-list-group-item>
      </b-list-group>

      <LaatsteSensorWaarde />
    </b-container>
  </div>
</template>

<script>
export default {
    name: "InstellingenPage"
}
</script>
