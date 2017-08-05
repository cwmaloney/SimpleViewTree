<template>
  <div class="folder">
    <p>{{value.name}}/</p>
    <ul>
      <li v-for="item in value.contents">
        <tree-item :value="item"></tree-item>
      </li>
    </ul>
  </div>
</template>

<script>
import TreeItem from './TreeItem';

export default {
  name: 'folder',

  beforeCreate: function () {
    console.log('components=', this.$options.components);
    this.$options.components.TreeItem = require('./TreeItem');
  },

  props: {
    value: {
      type: Object,
      required: true
    }
  },

  data () {
    return {
    }
  },

  components: { TreeItem }
}
</script>

<style scoped>
  ul {
    list-style-type: none;
    padding: 0;
    margin: 0 10px;
  }

  li {
    padding: 0;
    margin: 0 3px;
  }
  p {
    padding: 0;
    margin: 0;
    color: black;
  }
</style>
