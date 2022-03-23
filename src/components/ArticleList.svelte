<script>
    import Article from "./Article.svelte";

    // firebase get method
    let articles = [
        {id: 0, title: "Biden - Styrk cyberforsvaret i Ukraina.", emne: "sikkerhet", image_src: "https://www.kode24.no/images/75665214.jpg?imageId=75665214&panox=0&panoy=8.0213903743316&panow=100&panoh=52.406417112299&heighty=0&heightx=20.068027210884&heightw=41.156462585034&heighth=100&width=245&height=218&compression=80", content: "Biden - Styrk cyberforsvaret i Ukraina.I løpet av et tiår har sosiale medier forandret måten vi kommuniserer med hverandre på. Vi går i retning av et mer teknologibasert samfunn, og Norge blir ofte omtalt som ett av de mest digitale samfunnene i verden. Ungdom bruker opp mot sju timer i gjennomsnitt på nettet daglig. Ungdom bruker mindre tid sammen med venner ansikt til ansikt, og mer tid på Internett og sosiale medier. Varig lagring: Kommunikasjonen i s"},
        {id: 1, title: "Ove (32) liker seg i hengekøya: - Blir ofte lange lunsjer", emne: "ferie", image_src: "https://www.kode24.no/images/75644945.jpg?imageId=75644945&panox=0&panoy=36.363636363636&panow=100&panoh=63.636363636364&heighty=0&heightx=44.53781512605&heightw=33.893557422969&heighth=100&width=245&height=205&compression=80", content: "Heisann jeg er også en artikkel med tekst"},
    ];
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