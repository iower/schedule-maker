<template>
	<div class="home">
		<Interval text="Some-title-1"/>
		<Interval text="Some-title-2"/>
	</div>
</template>

<script>

import Interval from '@/components/Interval.vue'

export default {
	name: 'home',
	components: {
		Interval
	}
}

</script>
