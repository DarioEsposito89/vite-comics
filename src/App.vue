<script>
import TheHeader from './components/TheHeader.vue'
import TheMain from './components/TheMain.vue'
import TheLightBlueBar from './components/TheLightBlueBar.vue'
import TheFooter from './components/TheFooter.vue'
	export default {
		name: 'App',
		components: {
			TheHeader,
			TheMain,
			TheLightBlueBar,
			TheFooter,
		}
	}
</script>

<template>
	<TheHeader />
	<TheMain />
	<TheLightBlueBar />
	<TheFooter />
</template>

<style lang="scss">

</style>
