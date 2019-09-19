<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <h2>foo</h2>
    <p>
      <router-link to="/foo">Go to Foo</router-link>
      <router-link to="/bar">Go to Bar</router-link>
    </p>
    <div>
	<nav v-bind:class="active" v-on:click.prevent>
      	  <a href="#" class="home" v-on:click="makeActive('home')">Home</a>
	  <a href="#" class="projects" v-on:click="makeActive('projects')">Projects</a>
	</nav>
        <p>您选择了 <b>{{active}} 菜单</b></p>
    </div>
  </div>

</template>

<script>
export default {
  name: 'foo',
  data () {
    return {
      msg: 'Welcome to foo',
      site: 'vue',
      counter: 1,
      use: false,
      active: 'home',
      details: '<h1> 学的不仅是技术，更是梦想！</h1>'
    }
  },
  methods: {
    detail: function() {
      return  this.site + " - 学的不仅是技术，更是梦想！";
    },
    makeActive: function(item){
	// 模型改变，视图会自动更新
	this.active = item;
    }
  }
}
</script>
<style>
  nav{
    display:inline-block;
    margin:60px auto 45px;
    background-color:#5597b4;
    box-shadow:0 1px 1px #ccc;
    border-radius:2px;
  }

  nav.home .home,
  nav.projects .projects,
  nav.services .services,
  nav.contact .contact{
	background-color:#e35885;
  }
</style>
