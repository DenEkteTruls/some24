<script>
    let articles = JSON.parse(sessionStorage.getItem("articles"));
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
            letter-spacing: 1px; \
            font-weight: 600; \
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
        letter-spacing: 1px;
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