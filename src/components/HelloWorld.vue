<template>
  <div class="hello">
    <!-- <h1>{{ msg }}</h1> -->
    <p>
    <!-- 使用 router-link 组件来导航. -->
    <!-- 通过传入 `to` 属性指定链接. -->
    <!-- <router-link> 默认会被渲染成一个 `<a>` 标签 -->
    <router-link to="/foo">Go to Foo</router-link>
    <router-link to="/bar">Go to Bar</router-link>
    </p>
    <router-view></router-view>
    <p style = "font-size:25px;">计数器: {{ counter }}</p>
    <button @click = "counter++" style = "font-size:25px;">点我</button>
    <br></br>
    <label for="r1">修改颜色</label><input type="checkbox" v-model="use" id="r1">
    <div v-bind:class="{'class1': use}">
    v-bind:class 指令
     </div>
    <div v-html="details"></div>
    <h1>{{ detail() }}</h1>
   <p><a href="http://10.239.81.222:8000/cafeparser/">hhhh</a></p>
    <h2>Essential Links</h2>
  </div>
</template>

<script>
const foo = { template: '<div>foo</div>' };
const bar = { template: '<div>bar</div>' };
const routes = [
  { path: '/foo', component: foo },
  { path: '/bar', component: bar }
];
export default {
  name: 'HelloWorld',
  data () {
    return {
      msg: 'Welcome to Your Vue.js App',
      site: 'vue',
      counter: 1,
      use: false,
      details: '<h1> 学的不仅是技术，更是梦想！</h1>'
    }
  },
  methods: {
    detail: function() {
      return  this.site + " - 学的不仅是技术，更是梦想！";
    }
  }
}
</script>

<style>
.class1{
  background: #444;
  color: #eee;
}
</style>
