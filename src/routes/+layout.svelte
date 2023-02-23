<script>
	import '../app.css';
	let showMenu = false;
	import logoIcon from './logo1.png';
	import logoName from './logo2.png';
	function toggleNavbar() {
		showMenu = !showMenu;
	}
</script>

<nav class=" px-6 py-8 mx-auto md:flex md:justify-around md:items-center">
	<div class="flex items-center justify-between">
		<a class="text-xl font-bold text-gray-800 md:text-2xl hover:text-blue-400" href="/"
			>E-CELL PVPPCOE
		</a>
		<!-- Mobile menu button -->
		<!-- svelte-ignore a11y-click-events-have-key-events -->
		<div on:click={toggleNavbar} class="flex md:hidden">
			<button
				type="button"
				class="text-gray-800 hover:text-gray-400 focus:outline-none focus:text-gray-400"
			>
				<img src={showMenu ? logoIcon : logoName} alt="logo" width="30" />
			</button>
		</div>
	</div>

	<!-- Mobile Menu open: "block", Menu closed: "hidden" -->
	<div
		class="flex-col mt-8 space-y-4 md:flex md:space-y-0 md:flex-row md:items-center md:space-x-10 md:mt-0 {showMenu
			? 'flex items-center'
			: 'hidden'} "
	>
		<a class="text-gray-800 hover:text-blue-400" href="/">Home</a>
		<a class="text-gray-800 hover:text-blue-400" href="/event">Events</a>
		<a class="text-gray-800 hover:text-blue-400" href="/gallery">Gallery</a>
		<a class="text-gray-800 hover:text-blue-400" href="/about">About Us</a>
	</div>
</nav>

<slot />

<style lang="postcss">
	nav {
		padding: 1rem;
	}

	:global(html) {
		/* padding: 0 3%; */
		background-color: theme(colors.gray.100);
	}
</style>
