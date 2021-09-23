<template>
    <p class="fileBox_file">{{name}}</p>
</template>


<script>
export default {
  name: 'FileView',
  props: {
    name: String,
  }
}
</script>

<style scoped lang="scss">

.fileBox_file {
  border: 1px solid black;
  text-align: center;
  width: 150px;
  color: green;
}
</style>
