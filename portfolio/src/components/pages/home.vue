<template>
	<div class="content-bg--home" @click.native="emit">
		<h1 class="titles" @click="works">{{ msg }}</h1>
		<p class="intro">Welcome to this small website about me, what I do and what I have done :D</p>
	</div>
</template>

<script>
export default {
	name: 'Home',
	data () {
		return {
			msg: 'Welcome to my portfolio'
		}
	},
	methods: {
		works: function() {
			alert("WHAT DID YOU EXPECT?!")
		},
		emit: function() {
			this.$emit('minimize');
		}
	},
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss">
	.content-bg--home {
		position: absolute;
		top: 0;
		right: 0;
		left: 5%;
		bottom:0;
		background-image: url(/static/img/abstract-bg.de26123.jpg);
		background-position: 100% 50%;
		background-size: 100% 100%;
	}

</style>
