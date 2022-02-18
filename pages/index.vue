<template>
	<div>
		<h1>{{ title }}</h1>
		<pre>{{ data }}</pre>
		<Hello />
	</div>
</template>

<script lang="ts">
	export default defineComponent({
		asyncData( context ) {
			return { data: { data: 'hello', error: false } }
		},

		setup() {
			const title = ref<string>('Home Page')
			return { title }
		},
	})
</script>