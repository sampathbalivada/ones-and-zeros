<script>
	import Navbar from "./Navbar.svelte";
	import Footer from "./Footer.svelte";
	import Description from "./Description.svelte";
	import TabBar from "./TabBar.svelte";
	import Episodes from "./Episodes.svelte";

	let headerHeight;
	let footerHeight;
	let contentHeight;

	$: height = headerHeight + footerHeight + contentHeight;
</script>

<Navbar bind:headerHeight />
<main>
	<div>
		<div bind:clientHeight={contentHeight}>
			<Description />
			<TabBar />
		</div>
		
		<Episodes height={height} />
	</div>
</main>
<Footer bind:footerHeight />

<style>
	main {
		display: flex;
		justify-content: center;
	}

	div {
		display: flex;
		justify-content: space-between;
		flex-direction: column;
	}
</style>
