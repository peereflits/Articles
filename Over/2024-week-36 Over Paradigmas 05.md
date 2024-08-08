*Over ...*

# Over Programmeerparadigma's (V)

Het vijfde deel uit de serie **Programmeerparadigma's gaan niet over software**. 

*Programmeerparadigma's gaan niet alleen over software. Programmeerparadigma's gaan meer over hardware dan we denken. Een programmeerparadigma probeert een probleem op te lossen van het medium waarop het "leeft". In deze serie van artikelen leg ik uit welk paradigma welk hardware probleem oplost.*

## Deel 5: Internet / Web programming

Internet is niet meer uit ons leven weg te denken. Sterker nog: we kunnen (bijna) niet meer zonder. Maar wat is het aan internet (en daardoor het daaraan verbonden paradigma WP) dat het zo immens populair is geworden?

De vraag is dus:<br/>
*Wat is het probleem dat internet/WP probeert op te lossen?*<br/>
Antwoord: Het grootste probleem dat internet oplost, is de lokaliteit van data.

> **NB:** Op technisch niveau lost internet het probleem van RPC (Remote Procedure Call) op.

### Het probleem van lokaliteit van data

In de begindagen van de grote computers ('50-'70) moesten programmeurs op hun fiets, met in hun hand een broodtrommel met pons-kaarten, naar een rekencentrum om hun code de laten compileren en uit te voeren. Mainframes hadden terminals waar programmeurs naar toe moesten gaan om iets van een computer gedaan te krijgen. In de jaren '80, met de komst van de PC, werd dit probleem deels verholpen. Na de Mainframe, ontstonden nu client-server systemen. Met name bij "fat-clients" rees het probleem: hoe krijg ik een nieuwe versie van mijn client applicatie op de PC van de gebruiker? 

Spoiler alert: internet!

De opkomst van internet (in Nederland [in de jaren '90](https://nl.wikipedia.org/wiki/Geschiedenis_van_het_internet_in_Nederland)) was, met "[a computer on every desk and in every home](https://www.businessinsider.nl "De mission statement van Microsoft in '80 & `90")", en de beschikbaarheid het van internet voor het grote publiek door ISP's en [Mosaic](https://nl.wikipedia.org/wiki/Mosaic_(browser)), niet meer te stuiten. Door de groeiende beschikbaarheid van computers, kabels, (gestandaardiseerde) protocollen en applicaties (browsers en servers) kon internet ontstaan. Internet betekende, en betekent, dat "alle" informatie voor "iedereen", overal beschikbaar is.

> **NB:** De publieke alomtegenwoordigheid van informatie a.g.v. internet werkt ook als een [democratiserende kracht](https://assets.cambridge.org/97811070/49130/excerpt/9781107049130_excerpt.pdf).

Internet betekende ook dat het deployment probleem bij client-server applicaties kon worden opgelost. En met de toenemende volwassenheid en functionaliteit in protocollen (HTML5) en applicaties (=browsers) zijn client-server systemen op sterven na dood.

Dus rest ons applicaties te ontwikkelen "op internet". Deze applicaties bestaan uit een client deel (front-end) en een server deel (back-end), waarbij elk deel zijn eigen technologieën/talen/frameworks tot haar beschikking heeft. Dat lijkt natuurlijk niet handig. Maar beide verschillen omdat zij beide verschillende problemen oplossen: 

* de client app "leeft" in de browser op het beeldscherm;<br/>Een browser weet hoe het HTML e.a. op een beeldscherm moet *tekenen*.
* De backend applicatie "leeft" in het geheugen van een server;<br/>Het weet hoe het HTML e.a. moet *genereren*.

### WP == kabel

De essentie van een web applicatie is, dat zij "leeft" op de kabel (Wifi is een virtuele kabel). En een kabel is stateless. In een kabel kan een signaal alleen van de client naar de server of van de server naar de client gaan. En hiermee is het `Request-Response model` een feit.

De grammatica van het Request-Response model bestaat uit [ABC](https://en.wikipedia.org/wiki/Windows_Communication_Foundation):

* **A**ddress: dit is de URL van het endpoint. Waar vindt ik de resource;
* **B**inding: specificeert de te gebruiken communicatie- & beveiliging protocols. Hoe bevraag ik de resource;
* **C**ontract: definieert de interface van de resource. Wat kan ik van de resource vragen;

De kabel lost een lokaliteitsprobleem op. Daarvoor gebruikt het een taal (ABC) die dat kan adresseren. Daarom kent web-programming (aan haar randen) niet zoiets als polymorfisme, overerving e.a.. Deze begrippen maken geen onderdeel uit van het probleemdomein van het Request-Response model. 

> **NB:** In zowel Java/spring als in ASP.NET core wordt tegenwoordig alleen nog als *binding* JSON over HTTP gebruikt. Protocols als SOAP over HTTP, SOAP over TCP en SOAP over MQ zijn in onbruik geraakt. Als contract is [OpenAPI](https://www.openapis.org/) in zwang geraakt en "de" standaard. SOAP gebruikte WSDL als contract taal.

Wanneer een request op de back-end server aankomt, moet dat request "vertaald" worden van een rijtje bits (serieel) in de kabel, naar een "request object", een complex type, in het geheugen van de server (deserialize). Na het verwerken van het request moet de server het resultaat, de response, weer vertalen naar een rijtje bits op de kabel (serialize). 

Frameworks als Java Spring en ASP.NET doen veel om de "paradigm mismatch" weg te poetsen maar ergens blijft het altijd schuren als je de grens van een paradigma (= de grens van een medium) oversteekt. In dit geval gaat het van OO naar Web (lees: van geheugen naar kabel). In geval van database interactie is het van OO naar RDBMS (lees: van geheugen naar disk).

> Crossing the boundaries of a paradigm always aches due to a paradigm mismatch (like the object-relational mismatch).<br/>*--- Peereflits ---*

Zal de toekomst uit gaan wijzen dat FP-talen OO-talen gaan vervangen omdat zij beter aansluiten op het Web-programming paradigma daar FP en internet/HTTP beide stateless van nature zijn?


---

🍐 schrijft elke week een stukje. Over ... van-alles-en-nog-wat. 
En vooral over programmeren, techniek en hoe jij je daar, als &#9432;Naut toe kan verhouden.

---
