<template>
  <div id="app">
  	<v-header :title="msg"></v-header>
    <div>{{msg}}</div>

    <br>
    <div>
    	{{object.name}}
    </div>
    <br>
    <div>
    	<ul>
    		<li v-for="item in list">
    			{{item.name}}
    		</li>
    	</ul>
    </div>
    <div v-for="item in list">
    	{{item.name}}
    </div>
    <br>
    <div v-bind:title="msg">title</div>
    <br>
    <div v-html="h"></div>

    <br>

    <div v-bind:class="{red:flag}">color</div>

    <br>

    <div v-for="(item,key) in list">
    	<div v-bind:class="{red:key==0}">{{item.name}}</div>
    </div>
    <br>
    <input type="text" v-model="msg"/>
    <br>
    <input type="text" ref="a"/><button v-on:click="getMsg()">button</button>
  </div>
</template>

<script>
import Header from "./components/Header.vue";

export default {
  data() {
  	return {
  		msg: "hello",
  		object: {"name":1,"age":12},
  		list: [
  			{"name" : 1},
  			{"name" :2}
  		],
  		h: "<h2>hello</h2>",
  		flag: true
  	}
  },
  methods: {
  	getMsg() {
  		alert(this.$refs.a.value);
  	}
  },
  components: {
  	"v-header": Header
  },
  mounted() {
  	alert("hello");
  }
}
</script>

<style>
	.red {
		color: red;
	}
</style>
