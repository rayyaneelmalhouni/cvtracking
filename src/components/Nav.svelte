<script>
	let isOpen = false;
	export let segment;
	function toggleNav() {
		isOpen = !isOpen;
	}
</script>

<style>
	@media (min-width: 769px) {
		nav {
			border-bottom: solid gray 1px;
		}
	}
</style>
<nav class="navbar" role="navigation" aria-label="main navigation">
	<div class="navbar-brand">
	<a href="/" class="navbar-item">
		<img src="logo.jpg" alt="virus">
	</a>
	<span class="navbar-burger" 
	aria-label="menu" 
	aria-expanded="false" 
	on:click={toggleNav}
	class:is-active={isOpen}>
	<span aria-hidden="true" />
	<span aria-hidden="true" />
	<span aria-hidden="true" />
	</span>
	</div>
	<div class="navbar-menu" class:is-active={isOpen}>
		<div class="navbar-start">
			<a href="/" class="navbar-item" class:is-active={segment === undefined}>Home</a>
			<a href="/about" class="navbar-item" class:is-active={segment === "about"}>About</a>
		</div>
	</div>
</nav>	
