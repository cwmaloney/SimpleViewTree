<template>
  <div id="app">
    <tree-item :value="root"></tree-item>
  </div>
</template>

<script>

  import TreeItem from './components/TreeItem'

  export default {
    name: 'app',

    data() {
      return {
        root: {
          name: 'root', contents: [
            { name: 'folder1', contents: [
              { name: 'folder2', contents: [
                { name: 'file1'},
                { name: 'file2'},
                { name: 'folder3', contents: [
                  { name: 'file4'}
                ]}
              ]},
              {name: 'file5'}
            ]},
            { name: 'folder4', contents: [
              { name: 'folder5', contents: [
                { name: 'file5'},
                { name: 'file6'},
                { name: 'folder6', contents: [
                  { name: 'file7'}
                ]}
              ]}
            ]},
            {name: 'file8'}
          ]
        }
      }
    },

    components: {
      TreeItem
    }
  }
</script>

<style>
#app {

}
</style>
