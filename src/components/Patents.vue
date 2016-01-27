<template>
	<div class="ui container">
		<div class="ui inverted segment">
			<div class="ui centered huge header">
				PATENTS
			</div>
			<div id="patents_list" class="ui segment">
				<ul class="ui list">
					<li v-for="item in items">
						{{item.text}}
					</li>
				</ul>
			</div>
		</div>
	</div>
</template>

<style scoped>

.ui.header{
	margin-top: 30px;
	margin-bottom: 30px;
}

.ui.container{
	padding-bottom: 30px;
}

#patents_list{
	margin: auto;
	max-width: 65%;
	margin-bottom: 50px;
}
</style>

<script>
export default{
	data () {
		return {
			items: [
				{
					text: 'Aliquam lobortis sollicitudin finibus. Duis mattis eleifend est, at blandit ex imperdiet vel.'
				},
				{
					text: 'Aliquam lobortis sollicitudin finibus. Duis mattis eleifend est, at blandit ex imperdiet vel.'
				},
				{
					text: 'Aliquam lobortis sollicitudin finibus. Duis mattis eleifend est, at blandit ex imperdiet vel.'
				},
				{
					text: 'Aliquam lobortis sollicitudin finibus. Duis mattis eleifend est, at blandit ex imperdiet vel.'
				},
				{
					text: 'Aliquam lobortis sollicitudin finibus. Duis mattis eleifend est, at blandit ex imperdiet vel.'
				},
				{
					text: 'Aliquam lobortis sollicitudin finibus. Duis mattis eleifend est, at blandit ex imperdiet vel.'
				},
				{
					text: 'Aliquam lobortis sollicitudin finibus. Duis mattis eleifend est, at blandit ex imperdiet vel.'
				},
				{
					text: 'Aliquam lobortis sollicitudin finibus. Duis mattis eleifend est, at blandit ex imperdiet vel.'
				},
				{
					text: 'Aliquam lobortis sollicitudin finibus. Duis mattis eleifend est, at blandit ex imperdiet vel.'
				},
			]
		}
	}
}
</script>
