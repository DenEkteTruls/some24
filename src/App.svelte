<script>
	import router from "page";
	import Article from "./pages/Article.svelte";
	import Home from "./pages/Home.svelte";

	let page = Home;

	router("/", () => page = Home);
	router("/article", () => page = Article);

	router.start();
</script>

<svelte:component this={page}/>