<template>
  <div>
      <h2>News-Content [{{$route.params.id}}]</h2>
      <ul>
        <li><a href="/">Home</a></li>
      </ul>
  </div>
</template>

<script>
  export default {
    validate({params}) {
      return /^\d+$/.test(params.id);
    },
    data() {
      return{
        title: this.$route.params.title
      }
    },
    //独立设置head信息
    // 为了避免子组件中的meta标签不能正确覆盖父组件中相同的标签而产生重复的现象，
    // 建议利用 hid 键为meta标签配一个唯一的标识编号。
    head(){
      return{
        title:this.title,
        meta:[
          {hid:'description',name:'news',content:'This is news page'}
        ]
      }
    }
  }
</script>
