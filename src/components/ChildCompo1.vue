<template>
    <ul>
      <button @click="emitEvent">イベントを発火</button>
      <button @click="emitEvent">文言を変える</button>
    </ul>
</template>

<script>
export default {
  name: 'ChileCompo1',
  data() {
    return {
      eventData: 'ChildCompo1で定義した文言'
    };
  },
  methods: {
    emitEvent() {
      this.$emit('custom-event', this.eventData); // 'custom-event'というカスタムイベントを発火
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
button {
  font-size: 10px;
}
</style>
