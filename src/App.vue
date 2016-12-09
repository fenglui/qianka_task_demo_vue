<template>
  <div id="app" class="wrap-container">
    <div class="padding-horizontal">
      <tasks></tasks>
    </div>
  </div>
</template>
<script>
import tasks from './components/tasks'

export default {
  components: {
    tasks
  }
  }
</script>
<style>
  @import 'css/aui.2.0.css';
</style>