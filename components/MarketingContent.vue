<template>
  <div>
    <v-tabs v-model="tab">
      <v-tab>GENERAL</v-tab>
      <v-tab>TECHNICAL</v-tab>
    </v-tabs>

    <v-tabs-items v-model="tab">
      <v-tab-item> <GeneralContent /> </v-tab-item>
      <v-tab-item> <TechnicalContent /> </v-tab-item>
    </v-tabs-items>
  </div>
</template>

<script>
import GeneralContent from './GeneralContent.vue'
import TechnicalContent from './TechnicalContent.vue'

export default {
  name: 'MarketingContent',
  components: {
    GeneralContent,
    TechnicalContent,
  },
  data: () => ({
    tab: null,
  }),
}
</script>