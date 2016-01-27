<template>
	<div class="ui container">
		<h2 class="ui centered header">
			<div class="content">
				Recent Research
				<div class="sub header">
					recent research issue
				</div>
			</div>
		</h2>
		<div class="ui three column centered grid">
			<div v-for="item in items" class="column">
				<img class="ui centered medium image" :src="item.src" />
				<h3 class="ui centered header">
					<div class="content">{{item.text}}
						<div class="sub header">{{item.extra}}</div>
					</div>
				</h3>
			</div>
		</div>
	</div>
</template>

<style scoped>
.ui.three.column.centered.grid{
	margin-top: 40px;
	margin-bottom: 40px;
}
</style>

<script>
export default{
	data(){
		return {
			items: [
				{
					src: require('../assets/computer.jpg'),
					text: 'fundamentals of search engine',
					extra: 'with Google'
				},
				{
					src: require('../assets/computer.jpg'),
					text: 'fundamentals of search engine',
					extra: 'with Google'
				},
				{
					src: require('../assets/computer.jpg'),
					text: 'fundamentals of search engine',
					extra: 'with Google'
				},
				{
					src: require('../assets/computer.jpg'),
					text: 'fundamentals of search engine',
					extra: 'with Google'
				},
				{
					src: require('../assets/computer.jpg'),
					text: 'fundamentals of search engine',
					extra: 'with Google'
				},
				{
					src: require('../assets/computer.jpg'),
					text: 'fundamentals of search engine',
					extra: 'with Google'
				},

			]
		}
	}
}
</script>
