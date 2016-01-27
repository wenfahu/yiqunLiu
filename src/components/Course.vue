<template>
	<div class="ui container">
		<h2 class="ui centered header">
			<div class="content">
				COURSES
				<div class="sub header">
					An open course in the school as a professor
				</div>
			</div>
		</h2>
		<div class="ui three column centered grid">
			<div v-for="item in items" class="column">
				<div class="ui centered segment">
					<div id="course_video">
						<img class="ui centered medium image" :src="item.src" />
						<i class="massive grey video play outline icon"></i>
					</div>
					<h3 class="ui centered header">
						{{item.title}}
					</h3>
					<p class="meta">
						{{item.text}}
					</p>
				</div>
			</div>
		</div>
	</div>
</template>

<style scoped>
#course_video{
	position: relative;
}
.video.icon{
	position: absolute;	
	left: 30%;
	top: 25%;
}

</style>

<script>
export default {
	data () {
		return {
			items: [
				{
					src: require('../assets/computer.jpg'),
					title: 'introduction to search engine',
					text: 'Maecenas sit amet est sit nec orci. Vestibulum sed tortor nec nibh ornare sollicitudin sed ac lacus. Sed nec mi , ultricies justo eget, ornare sapien. Ut suscipit, ligula non tempus sagittis, mauris a mi'
				},
				{
					src: require('../assets/computer.jpg'),
					title: 'introduction to search engine',
					text: 'Maecenas sit amet est sit nec orci. Vestibulum sed tortor nec nibh ornare sollicitudin sed ac lacus. Sed nec mi , ultricies justo eget, ornare sapien. Ut suscipit, ligula non tempus sagittis, mauris a mi'
				},
				{
					src: require('../assets/computer.jpg'),
					title: 'introduction to search engine',
					text: 'Maecenas sit amet est sit nec orci. Vestibulum sed tortor nec nibh ornare sollicitudin sed ac lacus. Sed nec mi , ultricies justo eget, ornare sapien. Ut suscipit, ligula non tempus sagittis, mauris a mi'
				},
			]
		}
	}
}
</script>
