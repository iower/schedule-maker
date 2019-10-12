<template>
	<div class="timeline">
		
		<h2>Daily timeline</h2>
		
		<hr>
		
		<div class="settings">
			<div class="setting precision">
				<label>Precision</label>
				<select>
					<option>5 min</option>
					<option>10 min</option>
					<option>15 min</option>
					<option>20 min</option>
					<option>30 min</option>
					<option>1 h</option>
				</select>
			</div>
			<div class="setting start-time">
				<label>Start time</label>
				<select>
					<option>08:00</option>
					<option>09:00</option>
				</select>
			</div>
		</div>
		
		<hr>
		
		<div class="items">
			<div class="scale">
				<div class="scale-period">
					<div class="time start">8:00</div>
				</div>
				<div class="scale-period">
					<div class="time start">8:30</div>
				</div>
				<div class="scale-period">
					<div class="time start">9:00</div>
				</div>
				<div class="scale-period">
					<div class="time start">9:30</div>
				</div>
				<div class="scale-period">
					<div class="time start">10:00</div>
				</div>
				<div class="scale-period">
					<div class="time start">10:30</div>
					<div class="time finish">11:00</div>
				</div>
			</div>
			<div class="intervals">
				<Interval text="Some-title-1" />
				<Interval text="Some-title-2" />
				<Interval text="Some-title-3" />
				<Interval text="Some-title-4" />
				<Interval text="Some-title-5" />
				<Interval text="Some-title-6" />
			</div>
		</div>
	</div>
</template>


<script>

import Interval from '@/components/Interval.vue'

export default {
	name: 'Timeline',
	props: {
		//text: String
	},
	components: {
		Interval
	}
}

</script>


<style scoped lang="sass">

// ...

.timeline
	width: 300px
	margin-top: 20px
	margin-bottom: 20px
	margin-left: auto
	margin-right: auto
	box-shadow: 0px 0px 4px 4px #aaa5
	border: 1px solid #aaa
	border-radius: 5px
	background-color: #fff
	padding: 10px 8px 25px
	
	h2
		text-align: center
	
	.settings
		display: grid
		grid-template-columns: 1fr 1fr
		//margin-bottom: 20px
		
		.setting
			
			label
				margin-right: 0.5em
	
	.items
		display: grid
		grid-template-columns: 0fr 1fr

.scale
	margin-left: 40px
	margin-right: 10px
	
	.scale-period + .scale-period
		margin-top: -1px
	
	.scale-period
		height: 30px
		width: 1px
		background-color: #aaa
		color: #888
		position: relative
		
		&::before,
		&::after
			display: block
			content: ''
			position: absolute
			left: -4px
			width: 9px
			height: 1px
			background-color: #aaa
		
		&::before
			top: 0
		
		&::after
			bottom: 0
		
		.time
			position: absolute
			right: 8px
			
			&.start
				top: -0.5em
			
			&.finish
				bottom: -0.5em


</style>
