*Over ...*

# Over de wet van Goodhart in software engineering

*TL;DR;* Ik lees veel blogs en artikelen. Eén van de mensen die ik volg is [Hillel Wayne](https://www.hillelwayne.com/). Onlangs schreef hij een artikel dat ik jullie niet wil onthouden: [Goodhart's Law in Software Engineering](https://buttondown.com/hillelwayne/archive/goodharts-law-in-software-engineering/). Hieronder een vertaling ervan:

---

Ik raakte onlangs in discussie met een aantal mensen over de vraag of kleine functies *meestal* een goed idee waren of *altijd 100%* een goed idee. Het deed me erg denken aan de [wet van Goodhart](https://en.wikipedia.org/wiki/Goodhart%27s_law):

> Wanneer een maatregel een doel wordt, is het geen goede maatregel meer.

De *zwakke* versie hiervan is dat mensen perverse prikkels hebben om de statistieken te manipuleren. Als je metriek "aantal bugs in de bugtracker" is, zullen mensen bugs onterecht sluiten om het aantal omlaag te krijgen.

De *sterke* versie van de wet is, dat zelfs het 100% eerlijk nastreven van een metriek schadelijk is voor je doelen. Dit is een onvermijdelijk gevolg van het verschil tussen metriek en waarden. We hebben in de eerste plaats metrieken omdat wat we werkelijk belangrijk vinden niet kwantificeerbaar is. Er is iets waarvan we meer willen, maar we hebben geen manier om dat ding rechtstreeks te meten. We kunnen iets meten dat eruitziet als een ruwe benadering van ons doel. Maar dat is niet ons doel, en als we de metriek vervangen door het doel, beginnen we acties te ondernemen die de metriek boven het doel bevoordelen.

Stel dat we betrouwbaardere software willen. Hoe meet je dan "betrouwbaarheid"? Dat kan niet. Maar je kunt wel het aantal bugs in de bugtracker meten, want minder open bugs betekent: grofweg meer betrouwbaarheid. **Dat is niet hetzelfde.** Ik heb bugs opgelost zien worden op manieren die het systeem *minder* betrouwbaar maakten én resulteerden in minder geregistreerde bugs.

Ik geloof heilig in de sterke versie van de wet van Goodhart. Vooral om deze reden:

![Een pauw met zijn veren uitgespreid. De pauw schreeuwt.](./2024-week-40_Pauw.png)

Waar let een pauwin op bij een partner? Een mannetje met maximale fitheid. Wat is een metriek die fitheid benadert? Hoe mooi het verenkleed is, want mooier verenkleed = meer calorieën energie om te verspillen aan een verenkleed. Maar dat *benadert* alleen fitheid. En na generaties wordt het verenkleed zelf het punt ten koste van de algehele fitheid van de vogel. Seksuele selectie is de wet van Goodhart in actie.

## Voorbeelden in Engineering

De wet van Goodhart is een waarschuwing voor puntige bazen die met vreselijke statistieken komen: toegevoegde lijnen, voltooide feature points, etc. Ik ben meer geïnteresseerd in hoe het de statistieken beïnvloedt die we voor onszelf instellen en waar onze bazen misschien nooit van op de hoogte zijn.

* "Test coverage" is een proxy voor hoe grondig we onze software hebben getest. Het wijkt af wanneer we veel eigenschappen van dezelfde regels code moeten testen, of wanneer onze ergste bugs opduiken op het integratieniveau.
* "Cyclomatic complexity" en "function size" zijn proxy's voor code leesbaarheid. Ze wijken af ​​wanneer we denken aan globale module leesbaarheid, niet lokale functie leesbaarheid. Dan kunnen te veel functies de code en datastroom vertroebelen.
* Benchmarks zijn proxy's voor performante programma's en wijken af ​​wanneer het verbeteren van benchmarks ongebenchmarkte bewerkingen vertraagt.
* De hoeveelheid tijd besteed aan pairing/code reviewing/debugging/wat-dan-ook-proxies "productief zijn".
* [Het DORA-rapport](https://dora.dev/) is een interessant geval, omdat het beweert dat vier metrics proxies zijn voor onuitsprekelijke doelen zoals "elite performance" en werknemerstevredenheid. Het stelt ook dat je de commit-grootte moet minimaliseren om de DORA-metrics te verbeteren. Een proxy van een proxy van een doel!

## Wat kunnen we hieraan doen?

Nee, ik weet niet hoe ik een wet kan vermijden die het evolutieproces kan kapen.

Het DORA-rapport van 2023 suggereert dat lezers de wet van Goodhart moeten vermijden en "de sterkte van een team moeten beoordelen over een breed scala aan mensen, processen en technische capaciteiten" (pag. 10), wat een beetje is alsof je zegt dat de oplossing voor productiebugs is: "schrijf geen bugs". Het is een leidend principe, maar geen uitvoerbaar advies dat tot dat principe komt.

Ze zeggen ook "gebruik een combinatie van metrics om dieper begrip te krijgen" (ibid), wat in eerste instantie logischer klinkt. Als je de metriek X en Y hebt om doel G te benaderen, dan kan het overoptimaliseren van X Y schaden, wat aangeeft dat je verder van G af raakt. In de praktijk heb ik het zien veranderen in "we kunnen X niet verbeteren omdat het Y zal schaden en we kunnen Y niet verbeteren omdat het X zal schaden." Dit zou kunnen betekenen dat we op de best mogelijke plek voor G zitten, maar vaker betekent het dat we heel ver van ons doel af zitten. Je zou een gewogen combinatie van X en Y kunnen bedenken, zoals 0,7X + 0,3Y, maar dat is ook een metriek die onderhevig is aan Goodhart.

Ik denk dat het beste wat ik kan doen is zeggen "gebruik je beste technische oordeel"? Evolutie is gedachteloos, mensen niet. Nogmaals, geen bruikbaar of schaalbaar advies, maar naarmate ik ouder word, blijf ik ontdekken dat "gebruik je beste oordeel" alles is wat we kunnen doen. Kenniswerk is onuitsprekelijk en onherleidbaar.

---

🍐 schrijft elke week een stukje. Over ... van-alles-en-nog-wat. 
En vooral over programmeren, techniek en hoe jij je daar, als &#9432;Naut toe kan verhouden.

---
