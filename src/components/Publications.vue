<template>
<div class="ui stripe vertical segment">
	<div class="ui container">
		<h2 class="ui centered header">
			<div class="content">
				PUBLICATIONS
				<div class="sub header">
					Selected Publicatinos
				</div>
			</div>
		</h2>

		<div v-for="item in items" class="ui five column grid">
			<div v-if="$index % 2 == 0" class="three column right aligned row">
				<pub-item-left :title=item.title :year=item.year :content=item.text :img=item.img></pub-item-left>
			</div>
			<div v-else class="three column row">
				<pub-item-right :title=item.title :year=item.year :content=item.text :img=item.img></pub-item-right>
			</div>
		</div>
	</div>
</div>
</template>

<style scoped>

.full-width{
	width: 100%;
}

.ui.stripe.vertical.segment{
	padding: 6em 0em;
}
</style>

<script>
import PubItemLeft from './pub-item-left.vue'
import PubItemRight from './pub-item-right.vue'

export default{
	components: {PubItemLeft, PubItemRight},
	methods: {
		show_more(event){
			console.log('oo');
		},
		toggle(e){
			this.show = !this.show
		},
	},
	transition: {
		expand: {
			beforeEnter: function(el){
				el.textContent = 'beforeEnter'
			},
		},
	},
	data () {
		return {
			show: true,
			items: [
				{
					year: 2015,
					title: 'Aliquam luctus neque enim',
					img: require('../assets/computer.jpg'),
					text: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Etiam a interdum augue. Etiam ac justo eu sapien porta commodo ac vestibulum turpis. Vivamus ac diam suscipit nunc fringilla posuere. Sed vel libero nunc. Sed ipsum magna, posuere eget lorem quis, pretium viverra quam. Interdum et malesuada fames ac ante ipsum primis in faucibus. Pellentesque porta lobortis lorem ut ullamcorper. Integer volutpat tellus eget vulputate consectetur. Suspendisse potenti. Praesent in mollis dui, eget sollicitudin felis. Lorem ipsum dolor sit amet, consectetur adipiscing elit. Etiam a interdum augue. Etiam ac justo eu sapien porta commodo ac vestibulum turpis. Vivamus ac diam suscipit nunc fringilla posuere. Sed vel libero nunc. Sed ipsum magna, posuere eget lorem quis, pretium viverra quam. Interdum et malesuada fames ac ante ipsum primis in faucibus. Pellentesque porta lobortis lorem ut ullamcorper. Integer volutpat tellus eget vulputate consectetur. Suspendisse potenti. Praesent in mollis dui, eget sollicitudin felis.'
				},
				{
					year: 2015,
					title: 'Donec ut elit ligula.',
					img: require('../assets/computer.jpg'),
					text: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Etiam a interdum augue. Etiam ac justo eu sapien porta commodo ac vestibulum turpis. Vivamus ac diam suscipit nunc fringilla posuere. Sed vel libero nunc. Sed ipsum magna, posuere eget lorem quis, pretium viverra quam. Interdum et malesuada fames ac ante ipsum primis in faucibus. Pellentesque porta lobortis lorem ut ullamcorper. Integer volutpat tellus eget vulputate consectetur. Suspendisse potenti. Praesent in mollis dui, eget sollicitudin felis.'
				},
				{
					year: 2015,
					title: 'Ut augue tortor',
					img: require('../assets/computer.jpg'),
					text: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Etiam a interdum augue. Etiam ac justo eu sapien porta commodo ac vestibulum turpis. Vivamus ac diam suscipit nunc fringilla posuere. Sed vel libero nunc. Sed ipsum magna, posuere eget lorem quis, pretium viverra quam. Interdum et malesuada fames ac ante ipsum primis in faucibus. Pellentesque porta lobortis lorem ut ullamcorper. Integer volutpat tellus eget vulputate consectetur. Suspendisse potenti. Praesent in mollis dui, eget sollicitudin felis.'
				},
			]
		}
	}
}
</script>
