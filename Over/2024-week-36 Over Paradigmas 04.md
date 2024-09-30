*Over ...*

# Over Programmeerparadigma's (IV)

Dit is deel vier uit de serie **Programmeerparadigma's gaan niet over software**. 

*Programmeerparadigma's gaan niet alleen over software. Programmeerparadigma's gaan meer over hardware dan we denken. Een programmeerparadigma probeert een probleem op te lossen van het medium waarop het "leeft". In deze serie van artikelen leg ik uit welk paradigma welk hardware probleem oplost.*

## Deel 4: Functional programming

Met de komst van F# in .NET staat [Functional programming](https://nl.wikipedia.org/wiki/Functioneel_programmeren) (FP) weer iets meer in de belangstelling in de wereld van software ontwikkeling. De belangstelling is ook toegenomen doordat de ontwikkelingen in hardware functionele programmeertalen makkelijker maken.

> **NB:** Ervaring in FP of F# heb ik niet, anders dan die ene keer dat ik een review deed van een unit test die in F# was geschreven. Hierin verbaasde ik mij over hoe weinig code je nodig had om een setup + test te doen.
>
> Gedreven door nieuwsgierigheid heb ik jaren later [F# for Fun and Profit](https://fsharpforfunandprofit.com/) bestudeerd. Het was (en is?) een site die mij hierin veel inzicht heeft gegeven.

Maar waarom zijn er functionele talen (en het bijbehorende paradigma) nodig? De vraag die gesteld moet worden, is dus:<br/>*Wat is het probleem dat FP probeert op te lossen?*

Toen ik eens een sessie bij [gebruikersgroep dotNed](https://www.dotned.nl/) bijwoonde ([september 2009](https://dotned.nl/dotned-bijeenkomst?id=17)), waarin [Oliver Sturm](https://www.linkedin.com/in/oliversturm/) het één en ander over FP uitlegde, viel het tweede kwartje.

### Het probleem van OO

In OO, zoals we hiervoor hebben kunnen zien, wordt gedrag en "state" in een `class` ingekapseld. De interne state van een object mag natuurlijk niet worden geopenbaard aan de buitenwereld. De interne state mag alleen gewijzigd worden door de publieke methoden (mutators) van een object. Deze "mutators" dienen dan ook zeer nauwgezet de parameters te inspecteren en de interne state te valideren voordat de state wordt gewijzigd. Programmeren is mensenwerk (ondanks de recente komst van ChatGPT). En mensen maken fouten. De state van een object wordt vaker "gelekt" dan lief is, wat weer allerlei side-effects doet ontstaan, wat weer fouten oplevert, wat weer kosten/ergernis/complexiteit ... You get the drill.

Managing state is complex. En "OO is about managing state". Enter: Functional programming.

### Het Functionele paradigma 101

Het paradigma van functioneel programmeren bestaat uit het elimineren van state door "alles" te beschrijven in de vorm van functies. Maar zijn we dan weer terug bij structured programming?, hoor ik jullie al denken. Nee. Dit paradigma is gebaseerd op de wiskundige theorie van de [Lambda calculus](https://nl.wikipedia.org/wiki/Lambdacalculus). Het is een hoger niveau van denken, begrijpen en berekenen waarbij functies geen side-effects hebben want deze functies kennen geen state (in FP ook wel "pure functions" genoemd). En de parameters van een functie kunnen ook als functie worden beschreven (ook wel [currying](https://en.wikipedia.org/wiki/Currying) genoemd). Oftewel: een functie kan ook een andere functie als argument kan meekrijgen. Functies in FP zijn veelal referentieel transparant. Dit houdt in dat een expressie vervangen kan worden door zijn waarde zonder de werking van het programma te veranderen.

### FP == Thread

Dit is in een hele kleine notendop de essentie van FP. Ik weet dat ik aan een heleboel theorie ervan voorbij ga. Maar de crux van FP zit in het feit dat doordat een functie (op het allerlaagste niveau) stateless is, zijn er geen side-effects waardoor FP-programma's veel makkelijker haar berekeningen parallel uit kan voeren.

In FP "leeft" een functie dus op een processor-thread. En met de komst van multi-core processoren kan FP het probleem van inefficiënt processor gebruik (ongebruikte processor capaciteit) beter oplossen. Zij doet dit doordat zij functies veel makkelijker parallel uit kan voeren.

* FP is uiteindelijk ontstaan om efficiënter en goedkoper 'state' als gedrag (=complexiteit) op een medium zonder state (= processor thread) te beheren;
 
Dat er niet zoiets als "inheritance" bestaat in FP talen, is omdat dit een concept is dat niet van toepassing is in het probleemdomein van "functional programming".

Heb je vragen en/of opmerkingen: schroom niet om mij de contacten :smile:

Volgende week: over internet / web programming.

---

🍐 schrijft elke week een stukje. Over ... van-alles-en-nog-wat. 
En vooral over programmeren, techniek en hoe jij je daar, als &#9432;Naut toe kan verhouden.

---
