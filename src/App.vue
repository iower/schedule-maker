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

#app

#nav
	
	a
		
		&.router-link-exact-active
			font-weight: bold

</style>
