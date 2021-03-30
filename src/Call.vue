<template>
  <div id="call">
    <h2>call is happening!</h2>

    <p>Video: {{ audioAndVideoStreamId.videoId }}</p>
    <p>Audio: {{ audioAndVideoStreamId.audioId }}</p>
  </div>
</template>

<script>

import { mapGetters } from 'vuex'

export default {
  name: 'Call',
  computed: {
    ...mapGetters([
      'audioAndVideoStreamId'
    ])
  },
  mounted() {
    this.$store.dispatch('connect');
  }
}
</script>