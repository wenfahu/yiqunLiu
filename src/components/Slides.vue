<template>
	<div class="ui container">
		<h2 class="ui centered header">
			Recent Slides
		</h2>
		<div class="ui three column centered grid">
			<div v-for="item in items" class="column">
				<img class="ui centered medium circular image" :src="item.src" />
				<h3 class="ui centered header">
					<div class="content">
						{{item.text}}
						<div class="description">
							<i class="large circle thin icon"></i>
						</div>
					</div>
				</h3>
			</div>
		</div>

		<div class="ui centered header">
			<div class="ui large teal button">CONTINUE<div>
		</div>
	</div>
</template>

<style scoped>

.ui.circular.image{
	width:200px;
	height:200px;
}

.description{
	margin-top: 20px;
	margin-bottom: 30px;
}

.ui.container{
	margin-top: 80px;
	margin-bottom: 80px;
}

.ui.three.column.centered.grid{
	margin-top: 60px;
}
</style>

<script>
export default{
	data() {
		return {
			items: [
				{
					src: require('../assets/computer.jpg'),
					text: 'web search click model'
				},
				{
					src: require('../assets/computer.jpg'),
					text: 'web search click model'
				},
				{
					src: require('../assets/computer.jpg'),
					text: 'web search click model'
				},
			]
		}
	}
}
</script>
