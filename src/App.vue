<template>
    <div>
        <!--ChildCompo1のtemplateを呼び出す？-->
        <c-comp1 @custom-event="handleCustomEvent"></c-comp1>
        <p>{{ eventData }}</p>
    </div>
</template>

<script>
import ChildCompo1 from './components/ChildCompo1.vue'

export default {
  name: 'App',
  components: {
    'c-comp1' : ChildCompo1
  },
  data() {
    return {
      eventData: null
    };
  },
  methods: {
    handleCustomEvent(data) {
      this.eventData = data;
    }
  }

}
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
