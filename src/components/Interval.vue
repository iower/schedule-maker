<template>
	<div class="interval">
		interval {{ text }}
	</div>
</template>


<script>

export default {
	name: 'Interval',
	props: {
		text: String
	}
}

</script>


<style scoped lang="sass">

// ...

.interval
	border: 1px solid gray

</style>
