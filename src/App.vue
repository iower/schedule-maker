<template>
	<div id="app">
		<div id="nav">
			<!-- <router-link to="/">Home</router-link> |
			<router-link to="/about">About</router-link> -->
		</div>
		<router-view/>
	</div>
</template>


<style lang="sass">

*
	box-sizing: border-box


html
	background-color: #eee

html,
body
	margin: 0
	padding: 0

#app
	

#nav
	
	a
		
		&.router-link-exact-active
			font-weight: bold

h2
	margin-top: 0
	margin-bottom: 0

select
	height: 30px

hr
	margin-top: 1em
	margin-bottom: 1em

</style>
