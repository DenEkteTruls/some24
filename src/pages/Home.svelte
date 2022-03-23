<script>
	import ArticleList from "../components/ArticleList.svelte";
</script>



<body>
	<div class="menu">
		<div class="logo-container">
			<img src="logo.PNG" alt=""/>
			<h1>Some24</h1>
		</div>
		<div class="mid-part"></div>
		<div class="right-controls"></div>
	</div>
	<ArticleList/>
</body>



<style>
	.menu {
		margin: 30px 0;
		user-select: none;
		display: flex;
		flex-direction: column;
		flex-wrap: nowrap;
		max-width: 1000px;
	}

	.logo-container {
		width: 20%;
		display: flex;
		align-items: center;
		justify-content: center;
		margin: 0 40px;
	}

	.logo-container > img {
		height: 80px;
	}

	.logo-container > h1 {
		color: lightgray;
		margin-left: 10px;
		font-weight: 400;
	}

	.logo-container:hover {
		cursor: pointer;
	}

	.mid-part {
		width: 60%;
	}

	.right-controls {
		width: 20%;
	}

</style>