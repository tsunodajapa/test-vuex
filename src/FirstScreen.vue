<template>
  <div id="first-screen">
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
    <router-link to="/second-screen">Second Screen</router-link>
  </div>
</template>

<script>
import { mapGetters } from 'vuex'
import Call from "./Call";

export default {
  name: "FirstScreen",
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

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
