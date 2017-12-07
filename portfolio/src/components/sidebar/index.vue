<template>
	<v-navigation-drawer app dark class="sidebar" :mini-variant="mini">
		<v-app>
			<v-navigation-drawer permanent dark :mini-variant.sync="mini">
				<v-toolbar flat class="transparent">
					<v-list class="pa-0">
						<v-list-tile avatar>
							<v-list-tile-avatar>
								<img src="https://randomuser.me/api/portraits/men/85.jpg" />
							</v-list-tile-avatar>
							<v-list-tile-content>
								<v-list-tile-title>Twan Nieborg</v-list-tile-title>
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
						<v-icon>{{ item.icon }}</v-icon>
					</v-list-tile-action>
					<v-list-tile-content>
						<a :href="item.href">
							<v-list-tile-title>{{ item.title }}</v-list-tile-title>
						</a>
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
				title: 'Welcome to this page',
				message: new Date().toUTCString(),
				items: [
					{
						src: 'https://www.w3schools.com/w3css/img_fjords.jpg'
					},
					{
						src: 'https://images3.alphacoders.com/823/82317.jpg'
					},
					{
						src: 'https://static.pexels.com/photos/33045/lion-wild-africa-african.jpg'
					},
					{
						src: 'https://img.huffingtonpost.com/asset/5a139ce71500009d02859257.jpg?ops=1910_1000'
					}
				],
				navitems: [
					{
						title: 'Home', icon: 'dashboard', href: '/'
					},
					{
						title: 'About', icon: 'question_answer', href: 'about'
					}
				],
				mini: true,
				right: null
			}
		}
	}
</script>
