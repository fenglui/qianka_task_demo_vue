<template>
  <section class="aui-content">
    <div class="aui-card-list">
      <div class="aui-card-list-header">
        <div>
          <i class="aui-iconfont aui-icon-my aui-text-danger"></i>
          <span class="aui-text-danger">当前任务列表</span>
        </div>
        <i class="aui-iconfont aui-icon-more"></i>
      </div>
      <div class="aui-card-list-content">
        <ul class="aui-list aui-media-list">
          <li class="aui-list-item aui-list-item-middle" v-for="task in tasks">
            <div class="aui-media-list-item-inner" v-on:click="_gotoTask(task.id,task.app_name)">
              <div class="aui-list-item-media" style="width: 3rem;">
                <img v-bind:src="task.thumb" class="aui-img-round">
              </div>
              <div class="aui-list-item-inner">
                {{ task.app_name }}
                <span class="aui-label aui-label-success" v-for="tag in task.tags" style="margin-left:12px">{{tag}}</span>
              </div>
              <div class="aui-list-item-inner aui-list-item-arrow" style="width:100px;">
                {{ task.money }}
              </div>
            </div>
          </li>
        </ul>
      </div>
      <div class="aui-card-list-footer aui-text-center">
        查看更多
      </div>
    </div>
  </section>
</template>
<script>
export default {
  data () {
    return {
      tasks:[
        {
          id:1,
        thumb:'http://upload.guo7.com/a43c89af5c4c323a8b11cb305bbc67ae.jpg',
        app_name:'手***',
        tags:['免费','有专属','剩3726份'],
        money:'3.20'}
      
      ,{ id:2,
        thumb:'http://upload.guo7.com/684865ff48af8a1865c415e454e92f27.jpeg',
        app_name:'J***',
        tags:['免费','有专属','剩16496份'],
        money:'3.20'}]    
    }
  },
  methods: {
    _gotoTask: function (id,app_name,event) {
        // 方法内 `this` 指向 vm
      alert('领到任务： ' + id + app_name + '!')
        // `event` 是原生 DOM 事件
        //alert(event.target.tagName)
      }
  }
  }
</script>
<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  h1 {
    color: #42b983;
  }
  .aui-label{
    font-size:0.8rem;
  }
</style>

