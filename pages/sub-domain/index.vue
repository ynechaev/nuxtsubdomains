<template>
  <h1>subdomain index host: {{ this.host }}</h1>
</template>

<script>
export default {
  async asyncData({ req, redirect }) {
    if (process.server) {
      var host = req.headers.host
      return { host }
    }
  },
  data() {
    return {
      host: null
    }
  }
}
</script>