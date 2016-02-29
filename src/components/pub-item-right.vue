<template>
	<div class="column"></div>
	<div class="column">
		<img class="ui circular medium centered image" :src=img />
		<div class="vr">&nbsp;</div>
	</div>
	<div class="column">
		<div class="ui header">
			{{year}}
		</div>
		<h3 class="ui teal header" v-on:click="toggle">
			{{title}}
		</h3>
		<article v-if="show" transition="expand">
			{{content}}
		</article>
	</div>
</template>

<style scoped>
.expand-transition{
	transition: all .7s ease;
	height: 100%;
	padding: 10px;
	background-color: #eee;
	overflow: hidden;
}

.expand-enter, .expand-leave {
	height: 0;
	padding: 0 10px;
	opacity: 0;
}

.ui.circular.medium.image{
	width: 150px;
	height: 150px;
}

article{
	overflow: hidden;
}

.vr {
	width:2px;
	background-color:teal;
	position:absolute;
	top:160px;
	bottom:-20px;
	left:50%;
}

</style>

<script>
export default{
	methods: {
		toggle(e){
			console.log('toggle')
			this.show = !this.show
		}
	},
	props: ['year', 'content', 'img', 'title' ],
	data() {
		return {
			show: false
		}
	}
}
</script>
