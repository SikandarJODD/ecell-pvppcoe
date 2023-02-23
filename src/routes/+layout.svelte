<script>
	import '../app.css';
	let showMenu = false;
	import logoIcon from './logo1.png';
	import logoName from './logo2.png';
	function toggleNavbar() {
		showMenu = !showMenu;
	}
	import { page } from '$app/stores';
	$: routeId = $page.route.id;

	let navs = [
		{
			navtitle: 'Home',
			navlink: '/'
		},
		{
			navtitle: 'Events',
			navlink: '/events'
		},
		{
			navtitle: 'Gallery',
			navlink: '/gallery'
		},
		{
			navtitle: 'About Us',
			navlink: '/about'
		}
	];
	// logic Building
	//  <a class="text-gray-800 hover:text-blue-400" href="/event">Events</a>
</script>

<nav
	class="border-b-2 border-blue-300 bg-blue-50  px-6 py-3 mx-auto md:flex md:justify-around md:items-center "
>
	<div class="flex items-center justify-between">
		<a
			class="text-xl font-bold text-gray-800 md:text-2xl hover:text-blue-500 transition-all"
			href="/"
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
		class="flex-col mt-5 space-y-4 md:flex md:space-y-0 md:flex-row md:items-center md:space-x-10 md:mt-0 {showMenu
			? 'flex items-center'
			: 'hidden'} "
	>
		{#each navs as item}
			<a
				class="text-base text-gray-800 hoverState {item.navlink === routeId
					? 'text-blue-700 bg-blue-200  rounded-lg border-1 border-cyan-400'
					: ''}"
				href={item.navlink}>{item.navtitle}</a
			>
		{/each}
	</div>
</nav>

<slot />

<style lang="postcss">
	.hoverState {
		padding: 6px 15px;
		margin: 0 7px !important;
	}
	nav {
		padding: 1rem;
	}

	:global(html) {
		/* padding: 0 3%; */
		background-color: theme(colors.gray.100);
	}
</style>
