<template>
  <div id="second-screen">
    <h1>App boladão</h1>

    <div>Menu boladão do app boladão</div>

    <pre>
      <code>
        isAudioAndVideoAllowed: {{ isAudioAndVideoAllowed }}
        isAudioAllowed: {{ isAudioAllowed }}
        isVideoAllowed: {{ isVideoAllowed }}
      </code>
    </pre>

    <Call v-if="isAudioAndVideoAllowed"/>
    <router-link to="/">First Screen</router-link>
  </div>
</template>

<script>
import { mapGetters } from 'vuex'
import Call from "./Call";

export default {
  name: "SecondScreen",
    components: {
    Call,
  },
  computed: {
    ...mapGetters([
        'isAudioAndVideoAllowed',
        'isAudioAllowed',
        'isVideoAllowed',
    ])
  },
};
</script>


