<template>
  <div class="treeItem">
    <folder v-if="value.contents" :value="value"></folder>
    <file v-else :value="value"></file>
  </div>
</template>

<script>
import Folder from './Folder'
import File from './File'

export default {
  name: 'tree',

  props: {
    value: {
      type: Object,
      required: true
    }
  },

  data () {
    return {};
  },

  components: {Folder, File}
}
</script>

<style scoped>

</style>
