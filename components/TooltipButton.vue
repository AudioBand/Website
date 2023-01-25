<template>
  <v-tooltip bottom>
    <template #activator="{ on, attrs }">
      <v-btn icon v-bind="[attrs, ...$attrs]" v-on="on">
        <v-icon>
          {{ icon }}
        </v-icon>
      </v-btn>
    </template>
    <span>{{ tooltip }}</span>
  </v-tooltip>
</template>

<script>
export default {
  name: 'TooltipButton',
  props: {
    icon: {
      type: String,
      required: true,
    },
    tooltip: {
      type: String,
      required: true,
    },
  },
}
</script>
