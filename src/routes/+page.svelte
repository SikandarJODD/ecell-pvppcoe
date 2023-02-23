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
		content="https://img.freepik.com/free-vector/cute-baby-penguin-cartoon-vector-icon-illustration-animal-nature-icon-concept-isolated-premium-vector-flat-cartoon-style_138676-3770.jpg?w=740&t=st=1676591055~exp=1676591655~hmac=9a7ff300e68fbe82cf78cf8b1f592290d999885d079c7549bda8a655ba78e7e8"
	/>
</svelte:head>

<!-- <div class="container"> -->
<HeaderMain />
<MidSection />
<!-- </div> -->
