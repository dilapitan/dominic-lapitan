<template>
  <v-container>
    <br /><br />
    <v-row justify="center" align="center">
      <v-col cols="10" sm="8" md="6">
        <div class="text-h4">DOMINIC LAPITAN</div>
        <div class="text-h6 grey--text">Remove Software Developer</div>

        <br />

        <p>
          Hello! My name is Dominic. Currently, I'm a remote software developer
          working for
          <span>
            <a href="https://excellenceinbreeding.org/" target="_blank"
              >Enterprise Breeding System</a
            > </span
          >. Aside from that, I love working on side projects and studying
          topics related to modern Web development. On the side, I enjoy reading
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
          >
            {{ link.label }}
          </v-btn>
        </div>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  name: 'IndexPage',
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
