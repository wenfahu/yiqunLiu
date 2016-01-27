<template>
	<div class="ui container">
		<h2 class="ui centered header">
			<div class="content">
				PUBLICATIONS
				<div class="sub header">
					Selected Publicatinos
				</div>
			</div>
		</h2>

		<div class="ui five column grid">
			<div v-for="item in items"  class="three column row">
				<div class="column">
					<div class="ui header">
						{{item.year}}
					</div>
					<article>
						{{item.text}}
					</article>
					<p v-on:click='show-more'>
						show more
					</p>
				</div>
				<div class="column">
					<img class="ui circular medium centered image" :src=
						"item.img" />
				</div>
			</div>
		</div>

	</div>
</template>

<style scoped>
.ui.circular.medium.image{
	width: 150px;
	height: 150px;
}

article{
	height: 3em;
	overflow: hidden;
}
</style>

<script>
export default{
	methods: {
		show-more(event){
			console.log('oo');
		}
	},
	data () {
		return {
			items: [
				{
					year: 2015,
					img: require('../assets/computer.jpg'),
					text: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Etiam a interdum augue. Etiam ac justo eu sapien porta commodo ac vestibulum turpis. Vivamus ac diam suscipit nunc fringilla posuere. Sed vel libero nunc. Sed ipsum magna, posuere eget lorem quis, pretium viverra quam. Interdum et malesuada fames ac ante ipsum primis in faucibus. Pellentesque porta lobortis lorem ut ullamcorper. Integer volutpat tellus eget vulputate consectetur. Suspendisse potenti. Praesent in mollis dui, eget sollicitudin felis.'
				},
				{
					year: 2015,
					img: require('../assets/computer.jpg'),
					text: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Etiam a interdum augue. Etiam ac justo eu sapien porta commodo ac vestibulum turpis. Vivamus ac diam suscipit nunc fringilla posuere. Sed vel libero nunc. Sed ipsum magna, posuere eget lorem quis, pretium viverra quam. Interdum et malesuada fames ac ante ipsum primis in faucibus. Pellentesque porta lobortis lorem ut ullamcorper. Integer volutpat tellus eget vulputate consectetur. Suspendisse potenti. Praesent in mollis dui, eget sollicitudin felis.'
				},
				{
					year: 2015,
					img: require('../assets/computer.jpg'),
					text: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Etiam a interdum augue. Etiam ac justo eu sapien porta commodo ac vestibulum turpis. Vivamus ac diam suscipit nunc fringilla posuere. Sed vel libero nunc. Sed ipsum magna, posuere eget lorem quis, pretium viverra quam. Interdum et malesuada fames ac ante ipsum primis in faucibus. Pellentesque porta lobortis lorem ut ullamcorper. Integer volutpat tellus eget vulputate consectetur. Suspendisse potenti. Praesent in mollis dui, eget sollicitudin felis.'
				},
			]
		}
	}
}
</script>
