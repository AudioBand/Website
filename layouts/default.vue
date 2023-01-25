<template>
  <v-app dark>
    <v-app-bar :clipped-left="clipped" class="transparent" fixed app>
      <v-img
        class="mx-2"
        max-height="40"
        max-width="40"
        contain
        alt="AudioBand Logo"
        src="/audioband_logo.svg"
      />
      <TooltipButton icon="mdi-home" tooltip="Home" to="/" />
      <TooltipButton icon="mdi-download" tooltip="Download" to="/download" />

      <v-spacer />

      <TooltipButton
        icon="mdi-github"
        tooltip="Github"
        :href="GITHUB_URL"
        target="_blank"
      />
      <TooltipButton
        icon="mdi-discord"
        tooltip="Discord"
        :href="DISCORD_URL"
        target="_blank"
      />
      <TooltipButton
        icon="mdi-note-search"
        tooltip="Documentation"
        :href="DOCUMENTATION_URL"
        target="_blank"
      />
    </v-app-bar>
    <v-main>
      <Nuxt />
    </v-main>
    <v-footer class="accent" absolute app>
      <v-spacer />
      <span>&copy; {{ new Date().getFullYear() }}</span>
      <v-spacer />
    </v-footer>
  </v-app>
</template>

<script>
import TooltipButton from '~/components/TooltipButton.vue'
import { DOCUMENTATION_URL, GITHUB_URL, DISCORD_URL } from '@/constants/'

export default {
  name: 'DefaultLayout',
  components: { TooltipButton },
  data() {
    return {
      title: 'AudioBand',
      DOCUMENTATION_URL,
      GITHUB_URL,
      DISCORD_URL,
    }
  },
}
</script>
