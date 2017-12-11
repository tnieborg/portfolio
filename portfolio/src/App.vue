<template>
	<v-app>
		<sidebar></sidebar>
		<main>
			<section class="content">
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
	},

}
</script>

<style lang="scss">
	.navigation-drawer {
		padding: 0;
	}
	.application {
		&--wrap {
			flex-direction: row;
		}
	}

	.titles {
		display: flex;
		justify-content: center;
		margin-top: 50px;
		color: white;
		font-size: 48px;
		font-weight: 900;
	}


</style>
