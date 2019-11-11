<template>
  <v-app>
    <v-navigation-drawer v-model="drawer" app right>
      <v-list dense>
        <v-list-item link href="https://discordapp.com/invite/FACZyp9" target="_blank">
          <v-list-item-action>
            <v-icon>mdi-discord</v-icon>
          </v-list-item-action>

          <v-list-item-content>
            <v-list-item-title>Discord</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>

    <v-app-bar app color dark>
      <div class="d-flex align-center">
        <v-img :src="require('./assets/logo-light.svg')" class="shrink mr-2" contain width="40" />
        <v-img class="shrink mt-1 hidden-sm-and-down" contain min-width="100" />
      </div>
      <v-spacer />
      <v-toolbar-title>Navigation</v-toolbar-title>
      <v-app-bar-nav-icon @click.stop="drawerRight = !drawerRight" />
    </v-app-bar>
  </v-app>
</template>

<script>
export default {
  name: "App",

  components: {},

  data: () => ({
    drawer: null
  })
};
</script>
<style>
</style>