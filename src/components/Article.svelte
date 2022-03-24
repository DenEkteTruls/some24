<script>
    export let article;
    import Emne from "./Emne.svelte";


    function clicked()
    {
        localStorage.setItem("article_id", article.id);
        window.location.assign("article");
    }

</script>



<div class="container" on:click={clicked}>
    <div class="image-container">
        <img src={article.image_src} alt=""/>
    </div>
    <div class="info-container">
        {#if article.emne == "sikkerhet"}
            <Emne text={article.emne} color="--green"/>
        {:else if article.emne == "nyheter"}
            <Emne text={article.emne} color="--purple"/>
        {:else if article.emne == "presentasjon"}
            <Emne text={article.emne} color="--blue"/>
        {:else if article.emne == "Viste du?"}
            <Emne text={article.emne} color="--orange"/>
        {/if}
        <h1 id="title">{article.title}</h1>
        <p id="undertitle">Dette er en undertittel til artikkelen, advarers.</p>
    </div>
</div>



<style>
    .container {
        display: flex;
        flex-direction: row;
        height: 220px;
        background-color: var(--dark-article-background-color);
        border-radius: 10px;
        margin: 15px;
        user-select: none;
        transition: background-color 0.2s;
    }

    .image-container {
        min-width: 255px;
        display: flex;
        align-items: center;
        justify-content: center;
    }

    .image-container > img {
        width: 220px;
        height: 80%;
        object-fit: cover;
        border-radius: 15px;
    }

    .info-container {
        display: flex;
        flex-direction: column;
        margin: 10px;
        margin-top: 22px;
    }

    h1 {
        color: white;
        font-size: 37px;
        font-weight: 600;
        margin-bottom: 0;
        margin-top: 10px;
    }

    p {
        color: var(--subtext);
        font-size: 18px;
        font-weight: 400;
    }

    .container:hover {
        cursor: pointer;
        background-color: var(--dark-article-hover-color);
    }

    @media (max-width: 850px) {
        p {
            visibility: hidden;
            height: 0;
        }
    }
</style>