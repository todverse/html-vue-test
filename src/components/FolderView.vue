<template>

  <p class="folderBox_folder">{{name}}</p>

  <template v-for="folder in folders">
    <FolderView :name="folder.name" :folders="folder.folders" :files="folder.files"/>
  </template>
  <template v-for="file in files">
    <FileView :name="file.name"/>
  </template>
</template>

<script>
import FileView from "./FileView";
export default {
  name: 'FolderView',
  components: {FileView},
  props: {
    name: String,
    folders:Array,
    files:Array
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
.folderBox_folder{
  border: 1px solid black;
  width: 200px;
  margin-left: 300px;
  text-align: center;
  color: orangered;
}
</style>
