<template>
	<v-app>
		<sidebar></sidebar>
		<main>
			<section class="page">
				<v-fade-transition mode="out-in">
					<router-view></router-view>
				</v-fade-transition>
			</section>
		</main>
	</v-app>
</template>
<script>
import sidebar from'@/components/sidebar';

export default {
	components: {
			sidebar,
		},
	name: 'app',

	data () {
	 	return {
		}
	}
}
</script>

<style>
</style>
