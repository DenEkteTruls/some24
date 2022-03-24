<script>
	import ArticleList from "../components/ArticleList.svelte";	
	function toggle() {
		//window.document.body.classList.toggle("light-mode");
	}
</script>

<body>
	<ArticleList/>
</body>

<style>
	:global(body.light-mode) {
		background-color: var(--light-background-color);
		color: black;
	}
</style>