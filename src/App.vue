<template>
  <div id="app">
<!--
    <img src="./assets/logo.png">
    <div>
      <el-button @click="startHacking">Start</el-button>
      <el-button @click="test">Start</el-button> 
    </div>
 -->

    <transition name="fade"
		            mode="out-in">
			<router-view></router-view>
	</transition>
  </div>
</template>

<script>
export default {
  methods: {
    startHacking () {
      this.$notify({
        title: 'It works!',
        type: 'success',
        message: 'We\'ve laid the ground work for you. It\'s time for you to build something epic!',
        duration: 5000
      })
    },

    test (){
      alert(123);
    }
  }
}
</script>

<style>
#app {
  font-family: Helvetica, sans-serif;
  text-align: center;
}
</style>
