<template>
  <div id="app">
    <img class="logo" src="./assets/logo.png">
    <hello></hello>
	<Research></Research>
	<Publications></Publications>
	<Course></Course>
	<Awards></Awards>
	<Slides></Slides>
	<Patents></Patents>
  </div>
</template>

<script>
import Hello from './components/Hello'
import Research from './components/Research'
import Slides from './components/Slides'
import Patents from './components/Patents'
import Awards from './components/Awards'
import Course from './components/Course'
import Publications from './components/Publications'

export default {
  components: {
    Hello,
	Research,
	Slides,
	Patents,
	Awards,
	Course,
	Publications,
  }
}
</script>

<style>
body {
  font-family: Helvetica, sans-serif;
}
</style>
