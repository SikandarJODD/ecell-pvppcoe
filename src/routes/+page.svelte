<script>
	import HeaderMain from '../lib/HeaderMain.svelte';
	import MidSection from '../lib/MidSection.svelte';
	import Logo from './ecellLogo.png';
</script>

<!-- Svelte Head  -->
<svelte:head>
	<title>E-CELL VPPCOE</title>
	<link rel="shortcut icon" href={Logo} type="image/x-icon" />
	<meta
		name="description"
		content="Entrepreneurship Cell, VPPCOE, popularly known as E-Cell, is a non-profit hub run by the enthusiastic students of VPPCOE."
	/>
	<meta
		name="og:image"
		itemprop="image"
		content="https://drive.google.com/file/d/1Od2f0RJIPfJkHfIlNGabGAZlhIJOw-iL/view"
	/>
</svelte:head>

<!-- <div class="container"> -->
<HeaderMain />
<MidSection />
<!-- </div> -->
