<template>
  <v-container>
    <v-row justify="center" align="center">
      <v-col cols="10" sm="8" md="6">
        <div class="text-h4">DOMINIC LAPITAN</div>
        <div class="text-h6 grey--text">Remote Software Developer</div>

        <br />

        <p>
          👋 Hello! My name is Dominic. Currently, I'm a remote software
          developer working for open source projects about Crop Breeding. Aside
          from that, I love working on side projects and studying technologies
          related to Modern Web Development.
        </p>

        <MarketingContent />

        <p>
          🤓 On the side, I enjoy reading
          <span>
            <a
              href="https://www.goodreads.com/user/show/121647616-dominic"
              target="_blank"
              >books</a
            > </span
          >,
          <span>
            <a href="https://en.wikipedia.org/wiki/Speedcubing" target="_blank"
              >speedcubing</a
            > </span
          >, and playing classical pieces on the piano.
        </p>

        <p>
          🚀 For inquiries, contact me at:
          <a id="email">dilapitan.dev@gmail.com</a>
        </p>
      </v-col>
    </v-row>

    <v-row justify="center" align="center">
      <v-col cols="10" sm="8" md="6">
        <div class="d-flex justify-space-between flex-wrap">
          <v-btn
            v-for="(link, i) in links"
            :key="i"
            class="overline primary--text font-weight-bold"
            text
            :href="link.link"
            target="_blank"
            :disabled="link.label === 'Portfolio'"
          >
            {{ link.label }}
          </v-btn>
        </div>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
import MarketingContent from '../components/MarketingContent.vue'

export default {
  name: 'IndexPage',
  components: {
    MarketingContent,
  },
  data: () => ({
    links: [
      {
        label: 'Portfolio',
        link: '',
      },
      {
        label: 'Github',
        link: 'https://github.com/dilapitan',
      },
      {
        label: 'Codepen',
        link: 'https://codepen.io/dilapitan',
      },
      {
        label: 'LinkedIn',
        link: 'https://www.linkedin.com/in/dilapitan/',
      },
      {
        label: 'Buy Me Coffee',
        link: 'https://ko-fi.com/dilapitan',
      },
    ],
  }),
}
</script>

<style scoped>
#email {
  text-decoration: underline;
}
</style>