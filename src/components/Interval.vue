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

.interval + .interval
	margin-top: -1px

.interval
	border: 1px solid gray
	border-radius: 4px
	padding: 5px
	height: 30px


</style>
