# Programmeerparadigma's gaan niet over software (VI)

*TL;DR; Programmeerparadigma's gaan niet alleen over software. Programmeerparadigma's gaan meer over hardware dan we denken. Een programmeerparadigma probeert een probleem op te lossen van het medium waarop het "leeft". In deze serie van artikelen leg ik uit welk paradigma welke hardware probleem oplost.*

**Inhoudsopgave**

* [Deel 1](./deel-01-intro.md): Introductie
* [Deel 2](./deel-02-dbs.md): Databases (relationeel & NoSQL)
* [Deel 3](./deel-03-oo.md): Object oriëntatie
* [Deel 4](./deel-04-fp.md): Functional programming
* [Deel 5](./deel-05-wp.md): Internet / Web programming
* Deel 6: Cloud computing
* [Deel 7](./deel-07-conclusies.md): Conclusies
* [Referenties](./deel-08-referenties.md)


## Deel 6: Cloud computing

Over Cloud computing wordt veel geschreven: het is immers hip & happening. En hoewel ik hierover nog het nodige kan vertellen, loop ik het risico dat ik ga vertellen wat andere reeds hebben geblogd, gepodcast of gestreamed.

Dus dan meteen maar de vraag: Waarom Cloud computing? Oftewel:<br/>
*Wat is het probleem dat cloud computing wil oplossen?*<br/>
Antwoord: om het probleem van ongebruikte hardware op te lossen.

### Het probleem van ongebruikte hardware

Het opzetten van een goed serverpark is duur; heel erg duur. Denk niet alleen aan de servers, maar ook aan de kabels, routers, switches, UPS'es en andere hardware. Tel daarbij op: dat dit alles ook nog in een geconditioneerde ruimte moet staan, personeel, verzekeringen en andere zaken. Dan begrijp je: een goed serverpark is duur. En dit alles moet betaald worden voordat er ook maar één applicatie kan draaien (= capital expense).

Daarnaast moet het serverpark worden ingericht op zijn piekbelasting. Terwijl deze piek geen 24 uur per dag duurt. Dus de hardware wordt niet volledig benut. Dat maakt de exploitatie van een serverpark nog duurder (een hogere TCO)! Daarom geven organisaties vaker de voorkeur aan [OpEx boven CapEx](https://github.com/undergroundwires/Azure-in-bullet-points/blob/master/AZ-900%20Microsoft%20Azure%20Fundamentals/6.2.%20Capital%20Expenditure%20(CapEx)%20vs%20Operational%20Expenditure%20(OpEx).md).

> **NB:** OpEx = operational expenditure (operationele uitgaven), CapEx = capital expenditure (kapitaaluitgaven).

De belofte van cloud computing is dan ook: wij, de grote tech bedrijven, kunnen hardware (en alles wat daar omheen hangt) goedkoper beheren dan dat je dat zelf doet (o.a. omdat je alleen betaalt voor wat je gebruikt).

Maar daarmee zal je ook afspraken moeten maken over wie waarvoor verantwoordelijk is. Daar is het IAAS-PAAS-SAAS model voor ontwikkeld. Zie deze welbekende onderstaande afbeelding:

![SaaS vs PaaS vs IaaS: What's The Difference & How To Choose](./iaas-paas-saas.jpg)

### CC == Data center

Cloud computing "leeft" in een Data center/rekencentrum. Haar grammatica bestaat o.a. uit: public-, private- & hybrid cloud, IAAS, PAAS, SAAS, open standaarden, platform onafhankelijkheid, MPP, AI, Big Data. Cloud computing gaat uiteindelijk meer over TCO (Total Cost of Ownership) en het verdelen van verantwoordelijkheid (aansprakelijkheid & SLA) dan over technologie. Cloud computing is ook meer een "technologieparadigma" dan een "programmeerparadigma"; het is een duidelijke verschuiving in de "mindset" over hoe we omgaan met technologie.

Cloud computing maakt door een ongekende beschikbaarheid van compute + storage mogelijk dat technologieën als AI, Big Data en MPP (massive parallel processing) tot wasdom komen. Doordat cloud computing leunt op internet protocollen is zij eveneens niet (direct) locatie gebonden.

* CC is uiteindelijk ontstaan om efficiënter en goedkoper meerdere locatie-ongebonden systemen (data, gedrag en complexiteit) te beheren;

Dat er niet zoiets als "polymorphisme" bestaat in CC, is omdat dit een concept is dat niet van toepassing is in het probleemdomein van "cloud computing".
