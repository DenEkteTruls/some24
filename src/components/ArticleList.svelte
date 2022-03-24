<script>
    import Article from "./Article.svelte";

    // firebase get method
    let articles = [
        {id: 0, title: "Biden - Styrk cyberforsvaret i Ukraina.", emne: "sikkerhet", subtext: "Dette er en undertittel til artikkelen, advarers.", alt: "Litt informasjon om bilde som vi ser ovenfor denne tekten i dag har jeg penger i lomma ja", image_src: "https://www.kode24.no/images/75665214.jpg?imageId=75665214&x=0&y=0&cropw=100&croph=100&width=940&height=626", content: "<b>Biden - Styrk cyberforsvaret i Ukraina.</b><br><br>I løpet av et tiår har sosiale medier forandret måten vi kommuniserer med hverandre på. Vi går i retning av et mer teknologibasert samfunn, og Norge blir ofte omtalt som ett av de mest digitale samfunnene i verden. Ungdom bruker opp mot sju timer i gjennomsnitt på nettet daglig. Ungdom bruker mindre tid sammen med venner ansikt til ansikt, og mer tid på Internett og sosiale medier. Varig lagring: Kommunikasjonen i s"},
        {id: 1, title: "Fake News eller Real News :- Hvordan skiller vi dem?", emne: "nyheter", subtext: "Dette er en undertittel til artikkelen, advarers.", alt: "Litt informasjon om bilde som vi ser ovenfor denne tekten i dag har jeg penger i lomma ja", image_src: "https://international.usc.edu/wp-content/uploads/fake.jpg", content: "Heisann jeg er også en artikkel med tekst"},
        {id: 2, title: "Snapchat", emne: "presentasjon", subtext: "Dette er en undertittel til artikkelen, advarers.", alt: "Litt informasjon om bilde som vi ser ovenfor denne tekten i dag har jeg penger i lomma ja", image_src: "https://www.howtogeek.com/wp-content/uploads/2021/08/snaptchat-logo-welcome-iphone.jpg?width=1198&trim=1,1&bg-color=000&pad=1,1", content: "Heisann jeg er også en artikkel med tekst"},
        {id: 3, title: "Viste du :- Du eier egentlig ikke bildene dine på nett!", emne: "Viste du?", image_src: "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcT408l0LpFepyCzl1XdKeahlWsIISoC8092ew&usqp=CAU", subtext: "Dette er en undertittel til artikkelen, advarers.", alt: "Litt informasjon om bilde som vi ser ovenfor denne tekten i dag har jeg penger i lomma ja", content: "Du er dum ass..."}
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