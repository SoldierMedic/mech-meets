<template>
  <v-app>
    <v-navigation-drawer v-model="drawer" app floating right>
      <v-list dense rounded>
        <v-list-item link href="https://discordapp.com/invite/FACZyp9" target="_blank">
          <v-list-item-action>
            <v-icon>mdi-discord</v-icon>
          </v-list-item-action>

          <v-list-item-content>
            <v-list-item-title>Discord</v-list-item-title>
          </v-list-item-content>
        </v-list-item>

        <v-list-item
          link
          href="https://drive.google.com/open?id=1g-0-HS29PFlORcFRmP7pnl22SVB8c3Pf"
          target="_blank"
        >
          <v-list-item-action>
            <v-icon>mdi-image-multiple</v-icon>
          </v-list-item-action>

          <v-list-item-content>
            <v-list-item-title>Gallery</v-list-item-title>
          </v-list-item-content>
        </v-list-item>

        <v-list-item link href="https://discordapp.com/invite/FACZyp9" target="_blank">
          <v-list-item-action>
            <v-icon>mdi-calendar-question</v-icon>
          </v-list-item-action>

          <v-list-item-content>
            <v-list-item-title>RSVP</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>

    <v-app-bar app color dark>
      <div class="d-flex align-center">
        <v-img :src="require('./assets/logo-light.svg')" class="shrink mr-2" contain width="40" />
        <v-img class="shrink mt-1 hidden-sm-and-down" contain min-width="100" />
      </div>
      <v-spacer></v-spacer>
      <v-toolbar-title>Navigation</v-toolbar-title>
      <v-app-bar-nav-icon @click.stop="drawer = !drawer" />
    </v-app-bar>
    <Chat />
  </v-app>
</template>

<script>
import Chat from "@/components/chat.vue";

export default {
  components: {
    Chat
  },

  data: () => ({
    drawer: null
  })
};
</script>
<style>
</style>