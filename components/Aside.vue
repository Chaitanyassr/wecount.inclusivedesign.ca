<template>
	<aside>
		<nav v-if="headers.length > 0">
			<ul>
				<li v-for="h in headers" :key="h.id">
					<nuxt-link :to="h.href">
						{{ h.title }}
					</nuxt-link>
				</li>
			</ul>
		</nav>
	</aside>
</template>

<script>
export default {
	props: {
		headers: {
			type: Array,
			default: () => []
		}
	}
}
</script>
