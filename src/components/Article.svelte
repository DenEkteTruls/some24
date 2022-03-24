<script>
    export let article;
    import Emne from "./Emne.svelte";


    function clicked()
    {
        localStorage.setItem("article_id", article.id);
        window.location.assign("article");
    }

</script>


{#if article.size == "small"}
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
{:else if article.size == "big"}
<div class="container-big" on:click={clicked}>
    <div class="image-container-big">
        <img src="{article.image_src}" alt=""/>
        <div class="subimgdiv">
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
                <p id="undertitle">{article.alt}</p>
            </div>
        </div>
    </div>
</div>
{/if}



<style>
    .container {
        display: flex;
        flex-direction: row;
        height: 220px;
        background-color: var(--dark-article-background-color);
        border-radius: 10px;
        margin: 15px;
        user-select: none;
        transition: all 0.2s;
    }

    .container-big {
        display: flex;
        flex-direction: column;
    }

    .image-container {
        min-width: 255px;
        display: flex;
        align-items: center;
        justify-content: center;
    }

    .image-container-big {
        display: flex;
        flex-direction: column;
        flex-wrap: nowrap;
        max-width: 900px;
        background-color: var(--dark-article-background-color);
        border-radius: 15px;
        padding: 15px;
        margin: 13px;
        transition: all 0.2s;
    }

    .image-container-big img {
        border-radius: 10px;
        margin-bottom: 0px;
    }

    .image-container-big .subimgdiv {
        color: var(--subtext);
        padding: 0;
        margin: 0;
        font-size: 15px;
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
        font-weight: 600    ;
        margin-bottom: 0;
        margin-top: 10px;
    }

    p {
        color: var(--subtext);
        font-size: 18px;
        font-weight: 400;
        margin-top: 8px;
    }

    .info-container > #undertitle {
        margin-bottom: 0;
    }

    .container:hover {
        cursor: pointer;
        background-color: var(--dark-article-hover-color);
    }

    .image-container-big:hover {
        cursor: pointer;
        background-color: var(--dark-article-hover-color);
        display: flex;
        flex-direction: column;
        flex-wrap: nowrap;
        max-width: 900px;
        border-radius: 15px;
        padding: 15px;
        margin: 13px;
    }

    @media (max-width: 850px) {
        p {
            visibility: hidden;
            height: 0;
        }
    }
</style>