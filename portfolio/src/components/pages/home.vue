<template>
	<div class="content-bg--home">
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
		}
	},
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss">
	.content-bg--home {
		position: absolute;
		width: 100%;
		height: 100%;
		background-image: url('../images/space-bg.jpg');
	}

</style>
