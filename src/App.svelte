<script>
	import router from "page";
	import Article from "./pages/Article.svelte";
	import Home from "./pages/Home.svelte";
	import Menu from "./components/Menu.svelte";

	let page = Home;

	let articles = [
    	{"id": 0, "title": "Biden - Styrk cyberforsvaret i Ukraina.", "size": "big", "emne": "sikkerhet", "subtext": "Dette er en undertittel til artikkelen, advarers.", "alt": "Litt informasjon om bilde som vi ser ovenfor denne tekten i dag har jeg penger i lomma ja", "image_src": "https://www.kode24.no/images/75665214.jpg?imageId=75665214&x=0&y=0&cropw=100&croph=100&width=940&height=626", "content": "<b>Biden - Styrk cyberforsvaret i Ukraina.</b><br><br>I løpet av et tiår har sosiale medier forandret måten vi kommuniserer med hverandre på. Vi går i retning av et mer teknologibasert samfunn, og Norge blir ofte omtalt som ett av de mest digitale samfunnene i verden. Ungdom bruker opp mot sju timer i gjennomsnitt på nettet daglig. Ungdom bruker mindre tid sammen med venner ansikt til ansikt, og mer tid på Internett og sosiale medier. Varig lagring: Kommunikasjonen i s"},
    	{"id": 1, "title": "Fake News eller Real News :- Hvordan skiller vi dem?", "size": "small", "emne": "nyheter", "subtext": "Dette er en undertittel til artikkelen, advarers.", "alt": "Litt informasjon om bilde som vi ser ovenfor denne tekten i dag har jeg penger i lomma ja", "image_src": "https://international.usc.edu/wp-content/uploads/fake.jpg", "content": "I dag kan det være vanskelig å skille falske nyheter fra troverdige nyheter. Ifølge sikkerhverdag.no er falske nyheter; «[...] et begrep som ofte brukes om nyhetsliknende saker som virker ekte, men som helt eller delvis er basert på løgn, eller som har utelatt informasjon for å skape en bestemt vridning.»<h2>Bevist feilinformasjon</h2>Bevist falske nyheter er nyheter som blir publisert selv om redaksjonen vet at innholdet er falskt, men likevel gir dem ut. Dette kan være for å manipulere den offentlige meningen eller lede trafikk til en bestemt nettside.<h2>Ubevist feilinformasjon</h2>Ubevist falske nyheter er basert på sanne deler, men noen deler kan være feilaktige. Små feil kan gjøre hele historien generelt feil. Grunnen kan være at journalisten ikke har kontrollert fakta godt nok, eller at han har overdrevet visse aspekter for å få fram et bestemt poeng.<h2>Hvordan fungerer falske nyheter?</h2>Falske nyheter blir stadig mer utbredt, og spres oftest gjennom nettsteder. Bevist falske nyheter lages for å vekke oppmerksomheten og appellere til leserens følelser. Dette blir som regel gjort gjennom sinne eller frykt, og resultatet er at nyhetene blir spredt raskere enn ekte nyheter. Alle store sosiale medier har algoritmer basert på engasjementstatistikk, altså hvor mange som ser, liker, kommenterer og deler innlegg."},
    	{"id": 2, "title": "Snapchat", "size": "small", "emne": "presentasjon", "subtext": "Dette er en undertittel til artikkelen, advarers.", "alt": "Litt informasjon om bilde som vi ser ovenfor denne tekten i dag har jeg penger i lomma ja", "image_src": "https://www.howtogeek.com/wp-content/uploads/2021/08/snaptchat-logo-welcome-iphone.jpg?width=1198&trim=1,1&bg-color=000&pad=1,1", "content": "Heisann jeg er også en artikkel med tekst"},
    	{"id": 3, "title": "Viste du :- Du eier egentlig ikke bildene dine på nett!", "size": "small", "emne": "Viste du?", "image_src": "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcT408l0LpFepyCzl1XdKeahlWsIISoC8092ew&usqp=CAU", "subtext": "Dette er en undertittel til artikkelen, advarers.", "alt": "Litt informasjon om bilde som vi ser ovenfor denne tekten i dag har jeg penger i lomma ja", "content": "Du er dum ass..."}
	]

	sessionStorage.setItem("articles", JSON.stringify(articles));

	router("/", () => page = Home);
	router("/article", () => page = Article);

	router.start();
</script>

<svelte:component this={Menu}/>
<svelte:component this={page}/>