<script>
	import MediaQuery from "./MediaQuery.svelte";

	import Navbar from "./desktop/Navbar.svelte";
	import Footer from "./desktop/Footer.svelte";
	import Description from "./desktop/Description.svelte";
	import TabBar from "./desktop/TabBar.svelte";
	import Episodes from "./desktop/Episodes.svelte";

	import MobileNavbar from "./mobile/Navbar.svelte";
	import MobileFooter from "./mobile/Footer.svelte";
	import MobileDescription from "./mobile/Description.svelte";
	import MobileTabBar from "./mobile/TabBar.svelte";
	import MobileEpisodes from "./mobile/Episodes.svelte";

	let headerHeight;
	let footerHeight;
	let contentHeight;

	$: height = headerHeight + footerHeight + contentHeight;
</script>

<MediaQuery query="(min-width: 481px)" let:matches>
	{#if matches}
		<Navbar bind:headerHeight />
		<main>
			<div>
				<div bind:clientHeight={contentHeight}>
					<Description />
					<TabBar />
				</div>

				<Episodes {height} />
			</div>
		</main>
		<Footer bind:footerHeight />
	{/if}
</MediaQuery>

<MediaQuery query="(max-width: 480px)" let:matches>
	{#if matches}
		<MobileNavbar bind:headerHeight />
		<main>
			<div>
				<div bind:clientHeight={contentHeight}>
					<MobileDescription />
					<MobileTabBar />
				</div>

				<MobileEpisodes {height} />
			</div>
		</main>
		<MobileFooter bind:footerHeight />
	{/if}
</MediaQuery>

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
