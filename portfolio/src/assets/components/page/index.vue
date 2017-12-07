<template>
	<section class="page">
		<v-layout class="page-info">
			<h1 class="page-info__title">
				<slot name="title"></slot>
			</h1>
			<v-spacer></v-spacer>
			<slot name="actions"></slot>
		</v-layout>
		<section class="page-content">
			<slot></slot>
		</section>
	</section>
</template>

<script>
	export default {
		name: 'Cms-Page',
	};
</script>
