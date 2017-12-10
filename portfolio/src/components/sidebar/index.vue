<template>
	<v-navigation-drawer app dark class="sidebar" :mini-variant="mini">
		<v-app>
			<v-navigation-drawer permanent dark :mini-variant.sync="mini">
				<v-toolbar flat class="transparent">
					<v-list class="pa-0">
						<v-list-tile avatar>
							<v-list-tile-avatar>
								<img src="https://randomuser.me/api/portraits/men/34.jpg" />
							</v-list-tile-avatar>
							<v-list-tile-content>
								<v-list-tile-title>{{ title }}</v-list-tile-title>
							</v-list-tile-content>
							<v-list-tile-action>
								<v-btn icon @click.native.stop="mini = !mini">
									<v-icon>chevron_left</v-icon>
								</v-btn>
							</v-list-tile-action>
						</v-list-tile>
					</v-list>
				</v-toolbar>

				<v-list class="pt-0" dense>
					<v-divider></v-divider>
					<v-list-tile v-for="item in navitems" :key="item.title" @click="">
						<v-list-tile-action>
							<router-link class="navbar__link" :to="item.href"><v-icon>{{ item.icon }}</v-icon></router-link>
						</v-list-tile-action>
						<v-list-tile-content>
							<router-link class="navbar__link" :to="item.href">{{ item.title }}</router-link>
						</v-list-tile-content>
					</v-list-tile>
				</v-list>
			</v-navigation-drawer>
		</v-app>
	</v-navigation-drawer>
</template>

<script>
	export default {
		data () {
			return {
				title: 'Twan Nieborg',
				navitems: [
					{
						title: 'Home', icon: 'home', href: '/'
					},
					{
						title: 'About me', icon: 'account_box', href: '/about'
					}
				],
				mini: true,
				right: null
			}
		}
	}
</script>

<<style lang="scss">
	.navbar {
		&__link {
			text-decoration: none;
		}
	}
</style>

