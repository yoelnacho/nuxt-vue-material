<template>
  <div class="md-layout-item">
    <md-speed-dial :class="topPosition" md-direction="bottom">
      <md-speed-dial-target class="md-primary">
        <md-icon>my_location</md-icon>
      </md-speed-dial-target>

      <md-speed-dial-content>
        <md-button class="md-icon-button">
          <md-icon>directions</md-icon>
        </md-button>

        <md-button class="md-icon-button">
          <md-icon>streetview</md-icon>
        </md-button>
      </md-speed-dial-content>
    </md-speed-dial>

    <div>
      <small>Raised</small>
      <md-button class="md-raised" md-ripple>Default</md-button>
      <md-button class="md-raised" :md-ripple="false">Ripple Off</md-button>
      <md-button class="md-raised md-primary">Primary</md-button>
      <md-button class="md-raised md-accent">Accent</md-button>
      <md-button class="md-raised" disabled>Disabled</md-button>
    </div>

    <md-switch v-model="array" value="1">Array</md-switch>

    <md-field>
      <label for="movie">Movie</label>
      <md-select v-model="movie" name="movie" id="movie">
        <md-option value="fight-club">Fight Club</md-option>
        <md-option value="godfather">Godfather</md-option>
        <md-option value="godfather-ii">Godfather II</md-option>
        <md-option value="godfather-iii">Godfather III</md-option>
        <md-option value="godfellas">Godfellas</md-option>
        <md-option value="pulp-fiction">Pulp Fiction</md-option>
        <md-option value="scarface">Scarface</md-option>
      </md-select>
    </md-field>

    <md-field>
      <label>Initial Value</label>
      <md-input v-model="initial"></md-input>
    </md-field>

    <md-field>
      <label>Initial Value (Read Only)</label>
      <md-input v-model="initial" readonly></md-input>
    </md-field>

    <md-field>
      <label>Type here!</label>
      <md-input v-model="type"></md-input>
      <span class="md-helper-text">Helper text</span>
    </md-field>

    <md-field>
      <label>With label</label>
      <md-input v-model="withLabel" placeholder="A nice placeholder"></md-input>
    </md-field>

    <md-field md-inline>
      <label>Inline</label>
      <md-input v-model="inline"></md-input>
    </md-field>

    <md-field>
      <label>Number</label>
      <md-input v-model="number" type="number"></md-input>
    </md-field>

    <md-field>
      <label>Textarea</label>
      <md-textarea v-model="textarea"></md-textarea>
    </md-field>

    <md-field>
      <label>Textarea with Autogrow</label>
      <md-textarea v-model="autogrow" md-autogrow></md-textarea>
    </md-field>

    <md-field>
      <label>Disabled</label>
      <md-input v-model="disabled" disabled></md-input>
    </md-field>
  </div>
</template>

<script>
export default {
  name: "TextFields",
  data: () => ({
    topPosition: 'md-top-right',
    array: [],
    movie: "godfather",
    initial: "Initial Value",
    type: null,
    withLabel: null,
    inline: null,
    number: null,
    textarea: null,
    autogrow: null,
    disabled: null
  })
};
</script>