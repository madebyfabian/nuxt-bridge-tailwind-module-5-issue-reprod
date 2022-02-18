<template>
	<div>
		<p>Names</p>
		<ul>
			<li v-for="user in users" :key="user.id">{{ user.name }}</li>
		</ul>
	</div>
</template>

<script setup lang="ts">
	interface User {
		id: number;
		name: string;
	}

	const users = ref<User[]>([{
		id: 1,
		name: 'John'
	}]);

	users.value.push({
		id: 2,
		name: 'Jane'
	});
</script>
