<script>
    let articles = [
        {id: 0, title: "Biden - Styrk cyberforsvaret i Ukraina.", emne: "sikkerhet", subtext: "Dette er en undertittel til artikkelen, advarers.", alt: "Litt informasjon om bilde som vi ser ovenfor denne tekten i dag har jeg penger i lomma ja", image_src: "https://www.kode24.no/images/75665214.jpg?imageId=75665214&x=0&y=0&cropw=100&croph=100&width=940&height=626", content: "Biden - Styrk cyberforsvaret i Ukraina.<br><h2>I løpet av et tiår har sosiale medier forandret måten vi kommuniserer med hverandre på.</h2><br>Vi går i retning av et mer teknologibasert samfunn, og Norge blir ofte omtalt som ett av de mest digitale samfunnene i verden. Ungdom bruker opp mot sju timer i gjennomsnitt på nettet daglig. Ungdom bruker mindre tid sammen med venner ansikt til ansikt, og mer tid på Internett og sosiale medier. Varig lagring: Kommunikasjonen i s"},
        {id: 1, title: "Ove (32) liker seg i hengekøya: - Blir ofte lange lunsjer", subtext: "Dette er en undertittel til artikkelen, advarers.", alt: "Litt informasjon om bilde som vi ser ovenfor denne tekten i dag har jeg penger i lomma ja", emne: "ferie", image_src: "https://www.kode24.no/images/75644945.jpg?imageId=75644945&panox=0&panoy=36.363636363636&panow=100&panoh=63.636363636364&heighty=0&heightx=44.53781512605&heightw=33.893557422969&heighth=100&width=245&height=205&compression=80", content: "Heisann jeg er også en artikkel med tekst"},
    ];

    let article = articles[localStorage.getItem("article_id")];

    function clicked() { window.location.assign("/"); }

</script>



<div class="menu">
    <div class="logo-container" on:click={clicked}>
        <img src="logo.PNG" alt=""/>
        <h1>Some24</h1>
    </div>
    <div class="mid-part"></div>
    <div class="right-controls"></div>
</div>
<div class="container">
    <div class="top">
        <h1 id="title">{article.title}</h1>
        <p id="subtext">{article.subtext}</p>
        <div class="image">
            <img src="{article.image_src}" alt=""/>
            <div class="subimgdiv">
                <p id="subimg">{article.alt}</p>
            </div>
        </div>
    </div>
    <div class="bottom">
        {article.content}
    </div>
</div>


<style>

    .container {
        max-width: 950px;
        display: flex;
        flex-wrap: nowrap;
        flex-direction: column;
        color: white;
        align-items: center;
        justify-content: center;
        margin: 0 auto;
    }

    .top {
        display: flex;
        flex-direction: column;
    }

    #title {
        font-size: 50px;
        margin-bottom: 0;
        letter-spacing: 3px;
    }

    #subtext {
        margin-top: 8px;
        margin-bottom: 20px;
        font-size: 20px;
        color: var(--subtext);
    }

    .image {
        display: flex;
        flex-direction: column;
        flex-wrap: nowrap;
    }

    img {
        border-top-left-radius: 15px;
        border-top-right-radius: 15px;
        margin-bottom: 0px;
    }

    .subimgdiv {
        background-color: var(--dark-article-hover-color);
        border-bottom-left-radius: 15px;
        border-bottom-right-radius: 15px;
        padding: 15px;
    }

    #subimg {
        color: var(--subtext);
        padding: 0;
        margin: 0;
        font-size: 15px;
    }

    .bottom {
        max-width: 700px;
        font-size: 20px;
    }



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