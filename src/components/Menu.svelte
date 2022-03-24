<script>
    function clicked() { window.location.assign("/"); }
</script>



<div class="menu">
    <div class="logo-container" on:click={clicked}>
		<!--
		{#if theme == "light"}
        	<img src="favicon.png" alt=""/>
		{:else}
			<img src="logo_white.png" alt=""/>
		{/if}
		-->
		<img src="logo_white.png" alt=""/>
        <h1>Some24</h1>
    </div>
    <div class="mid-part"></div>
    <div class="right-controls">
		<!--
		<button id="bulb" on:click={toggle}>
			<svg class="icon" xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><circle cx="12" cy="12" r="5"></circle><line x1="12" y1="1" x2="12" y2="3"></line><line x1="12" y1="21" x2="12" y2="23"></line><line x1="4.22" y1="4.22" x2="5.64" y2="5.64"></line><line x1="18.36" y1="18.36" x2="19.78" y2="19.78"></line><line x1="1" y1="12" x2="3" y2="12"></line><line x1="21" y1="12" x2="23" y2="12"></line><line x1="4.22" y1="19.78" x2="5.64" y2="18.36"></line><line x1="18.36" y1="5.64" x2="19.78" y2="4.22"></line></svg>
		</button>
		-->
	</div>
</div>



<style>

	button {
		color: white;
		border: none;
		background: none;
		cursor: pointer;
	}

    .menu {
		margin: 30px 0 0 0;
		user-select: none;
		display: flex;
		flex-direction: column;
		flex-wrap: nowrap;
		max-width: 950px;
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
		font-weight: 600;
		letter-spacing: 1px;
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

	:global(body.light-mode) {
		background-color: var(--light-background-color);
		color: black;
	}

	:global(body.light-mode) #bulb {
		color: black;
	}

	:global(body.light-mode) .logo-container > h1 {
		color: black;
		font-weight: 600;
	}
</style>