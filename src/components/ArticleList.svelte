<script>
    import Article from "./Article.svelte";
    let articles = JSON.parse(sessionStorage.getItem("articles"));
</script>


<div class="article-container">
    {#each articles as article}
        <Article {article}/>
    {/each}
</div>


<style>
    .article-container {
		display: flex;
		flex-direction: column;
        margin: 20px;
	}
</style>