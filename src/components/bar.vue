<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <h2>bar</h2>
    <p>
      <router-link to="/foo">Go to Foo</router-link>
      <router-link to="/bar">Go to Bar</router-link>
    </p>
  </div>
</template>

<script>
export default {
  name: 'bar',
  data () {
    return {
      msg: 'Welcome to bar',
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
