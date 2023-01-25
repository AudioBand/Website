<template>
  <v-container class="primary" fill-height fluid>
    <v-row align="center" justify="center">
      <v-card class="transparent" elevation="0">
        <v-card-title class="text-h1 font-weight-bold justify-center">
          <!-- <v-img class="ma-n12" max-height="100%" contain alt="AudioBand Logo" src="/audioband_logotype_cover.svg" /> -->
          AudioBand
        </v-card-title>
        <v-divider />
        <v-card-subtitle class="text-h3 font-weight-medium justify-center"
          >this is a music player bla bla</v-card-subtitle
        >
        <v-card-actions class="justify-space-around">
          <v-btn x-large color="accent" to="/download">
            <v-icon>mdi-download</v-icon>
            Download Now!
          </v-btn>
          <v-btn x-large color="#333" target="_blank" :href="GITHUB_URL">
            <v-icon>mdi-github</v-icon>
            Github
          </v-btn>
          <v-btn x-large color="#5865F2" target="_blank" :href="DISCORD_URL">
            <v-icon>mdi-discord</v-icon>
            Discord
          </v-btn>
        </v-card-actions>
      </v-card>
    </v-row>
  </v-container>
</template>

<script>
import { DOCUMENTATION_URL, GITHUB_URL, DISCORD_URL } from '@/constants/'

export default {
  name: 'IndexPage',
  data() {
    return {
      DOCUMENTATION_URL,
      GITHUB_URL,
      DISCORD_URL,
    }
  },
}
</script>
