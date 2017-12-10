<template>
	<div class="content-bg--about">
		<h1 class="titles">{{ msg }}</h1>
	</div>
</template>

<script>
export default {
	name: 'About',
	data () {
		return {
			msg: 'About me'
		}
	}
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss">
	.content-bg--about {
		position: absolute;
		width: 100%;
		height: 100%;
		background-image: url('../images/nerd-bg.png');
		background-size: 100% 100%;
	}
</style>
