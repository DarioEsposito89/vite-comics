<script>
import TheHeader from './components/TheHeader.vue'
import TheLightBlueBar from './components/TheLightBlueBar.vue'
import TheFooter from './components/TheFooter.vue'
	export default {
		name: 'App',
		components: {
			TheHeader,
			TheLightBlueBar,
			TheFooter,
		}
	}
</script>

<template>
	<TheHeader />
	<TheLightBlueBar />
	<TheFooter />
</template>

<style lang="scss">

</style>
