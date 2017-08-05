<template>
  <div class="file">
    <p>{{value.name}}</p>
  </div>
</template>

<script>
export default {
  name: 'file',

  props: {
    value: {
      type: Object,
      required: true
    }
  },

  data () {
    return {}
  }
}
</script>

<style scoped>
  p {
    padding: 0;
    margin: 0;
    color: darkgray;
  }
</style>
