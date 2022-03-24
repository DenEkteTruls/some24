<script>
    let articles = [
        {id: 0, title: "Biden - Styrk cyberforsvaret i Ukraina.", emne: "sikkerhet", subtext: "Dette er en undertittel til artikkelen, advarers.", alt: "Litt informasjon om bilde som vi ser ovenfor denne tekten i dag har jeg penger i lomma ja", image_src: "https://www.kode24.no/images/75665214.jpg?imageId=75665214&x=0&y=0&cropw=100&croph=100&width=940&height=626", content: "<b>Biden - Styrk cyberforsvaret i Ukraina.</b><br><br>I løpet av et tiår har sosiale medier forandret måten vi kommuniserer med hverandre på. Vi går i retning av et mer teknologibasert samfunn, og Norge blir ofte omtalt som ett av de mest digitale samfunnene i verden. Ungdom bruker opp mot sju timer i gjennomsnitt på nettet daglig. Ungdom bruker mindre tid sammen med venner ansikt til ansikt, og mer tid på Internett og sosiale medier. Varig lagring: Kommunikasjonen i s"},
        {id: 1, title: "Fake News eller Real News :- Hvordan skiller vi dem?", emne: "nyheter", subtext: "Dette er en undertittel til artikkelen, advarers.", alt: "Litt informasjon om bilde som vi ser ovenfor denne tekten i dag har jeg penger i lomma ja", image_src: "https://international.usc.edu/wp-content/uploads/fake.jpg", content: "Heisann jeg er også en artikkel med tekst"},
        {id: 2, title: "Snapchat", emne: "presentasjon", subtext: "Dette er en undertittel til artikkelen, advarers.", alt: "Litt informasjon om bilde som vi ser ovenfor denne tekten i dag har jeg penger i lomma ja", image_src: "https://www.howtogeek.com/wp-content/uploads/2021/08/snaptchat-logo-welcome-iphone.jpg?width=1198&trim=1,1&bg-color=000&pad=1,1", content: "Heisann jeg er også en artikkel med tekst"},
        {id: 3, title: "Viste du :- Du eier egentlig ikke bildene dine på nett!", emne: "Viste du?", image_src: "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcT408l0LpFepyCzl1XdKeahlWsIISoC8092ew&usqp=CAU", subtext: "Dette er en undertittel til artikkelen, advarers.", alt: "Litt informasjon om bilde som vi ser ovenfor denne tekten i dag har jeg penger i lomma ja", content: "Du er dum ass..."}
    ];

    let article = articles[localStorage.getItem("article_id")];

    function stringToHTML(str)
    {
        var parser = new DOMParser();
        var doc = parser.parseFromString(str, "text/html");

        var bold_tags = doc.getElementsByTagName("b");
        for(var i = 0; i < bold_tags.length; i++)
        {
            doc.getElementsByTagName("b")[i].style = "\
            color: white; \
            font-size: 30px; \
            letter-spacing: 2px; \
            ";
        }
        return doc.body.innerHTML;
    }

    function load_bottom()
    {
        console.log("in");
        document.getElementById("article").innerHTML = stringToHTML(article.content);
    }

    window.onload = () => {
        load_bottom();
    }
</script>


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
    <div class="bottom" id="article"></div>
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
        max-width: 950px;
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
        max-width: 750px;
        font-size: 20px;
        color: var(--subtext);
        margin: 50px 0;
    }

    :global(body.light-mode)
    {
		color: black;
	}

    :global(body.light-mode) .subimgdiv {
        background-color: var(--article-hover-color);
    }

    @media (max-width: 1000px){
        .top {
            max-width: 800px;
        }

        .bottom {
            max-width: 650px;
        }
    }

    @media (max-width: 850px) {
        .top {
            max-width: 700px;
        }

        .bottom {
            max-width: 600px;
        }
    }

    @media (max-width: 770px) {
        .top {
            max-width: 600px;
        }

        .bottom {
            max-width: 550px;
        }
    }
</style>