<template>
  <v-app dark>
    <template v-if="error.statusCode === 404">
      <br />
      <h2 class="red--text">
        {{ pageNotFound }}.
        <span class="black--text">Why you here, bro?</span>
      </h2>
    </template>

    <h1 v-else>
      {{ otherError }}
    </h1>

    <br />

    <NuxtLink to="/">
      <v-btn color="primary">Go Home</v-btn>
    </NuxtLink>
  </v-app>
</template>

<script>
export default {
  name: 'EmptyLayout',
  layout: 'empty',
  props: {
    error: {
      type: Object,
      default: null,
    },
  },
  data() {
    return {
      pageNotFound: 'Error 404. Not Found',
      otherError: 'An error occurred',
    }
  },
  head() {
    const title =
      this.error.statusCode === 404 ? this.pageNotFound : this.otherError
    return {
      title,
    }
  },
}
</script>
