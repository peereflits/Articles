*Over ...*

# Over de Generaties van programmeertalen

Programmeertalen kan je op verschillende manieren indelen: imperatief vs declaratief, high-level vs low-level, naar paradigma (structured, object-oriented, functional) of anders. Ook worden programmeertalen ingedeeld naar generatie. Maar daar is iets bijzonders mee. Talen worden in vier- of vijf generaties onder verdeeld. En de eerste verzameling aan programmeertalen die werd erkend als een generatie van programmeertalen was niet de eerste maar de derde! Pas toen er in de IT-wereld consensus begon te ontstaan dat de (toenmalige) huidige generatie computertalen een derde generatie taal was, toen moest er ook worden teruggerekend van drie, naar twee, naar de eerste.

Waar bestaan die generaties van talen uit?

## De eerste generatie

Dit is het laagste niveau van programmeertalen. Alle opdrachten en gegevens worden, op processor niveau, weergegeven in reeksen van enen en nullen. Dit komt overeen met de elektrische toestanden "aan" en "uit" in een computer is is de basis voor het binaire rekensysteem van computers. Dit is ook het enige dat een processor "begrijpt".

In de jaren vijftig had elke computer zijn eigen "machinetaal" en programmeurs hadden primitieve systemen voor het combineren van getallen om instructies weer te geven, zoals optellen en vergelijken. In machinetaal worden alle instructies, geheugenlocaties, cijfers en tekens weergegeven in reeksen nullen en enen. Hoewel machinetaalprogramma's doorgaans worden weergegeven met de binaire getallen vertaald in octaal (base-8) of hexadecimaal (base-16), zijn deze programma's voor mensen niet gemakkelijk te lezen, schrijven of debuggen.

## Generatie II

Assembler/Assembly-talen zijn computertalen die een symbolische notatie gebruiken om machinetaalinstructies weer te geven. Zij zijn sterk verbonden met machinetaal en de interne architectuur van het computersysteem waarop ze worden gebruikt. Ze worden low-level-talen genoemd omdat ze zo nauw verwant zijn aan de machines. Bijna alle computersystemen beschikken over een assembleertaal die kan worden gebruikt.

Normaal gesproken bestaat een zo'n taalinstructie uit een label, een bewerkingscode en een of meer operanden. Labels worden gebruikt om instructies in het programma te identificeren en ernaar te verwijzen. De bewerkingscode is een symbolische notatie die de specifieke uit te voeren bewerking specificeert, zoals verplaatsen, optellen, aftrekken of vergelijken. De operand vertegenwoordigt het register of de locatie in het hoofdgeheugen waar de te verwerken gegevens zich bevinden. 

Programma's die in Assembly zijn geschreven, hebben een vertaler nodig om ze in machinetaal om te zetten. Een assembleertaalinstructie voor vermenigvuldigen, MP, heeft geen betekenis voor de computer, omdat deze alleen opdrachten in de vorm van `11010110` begrijpt. Daarom is een programma, genaamd **assembler**, nodig om elke assembleertaalinstructie te vertalen naar een machinetaalinstructie.

## 3GL

De derde generatie programmeertalen worden ook wel de "procedurele talen" genoemd. Dit omdat de vierde generatie veelal non-procedurele talen omvat. Derde generatie talen, en die erna, worden ook wel de *high-level* talen genoemd, in tegenstelling tot Gen1/Gen2 die *low-level* wordt genoemd. De meest kenmerkende eigenschap van deze talen is dat één instructie op dit niveau veelal wordt vertaald naar meerdere machinetaalinstructies. Dit in tegenstelling tot assembly-talen, waarbij één instructie normaal gesproken één machinetaalinstructie genereert. Deze talen zijn ontwikkeld om het programmeren eenvoudiger en minder foutgevoelig te maken. Qua "taligheid" houden deze talen het midden tussen mensentaal & machinetaal.

Er bestaat geen volledige overeenstemming over wat exact 3GL-talen omvat. Daarom wordt er vaker onderscheid gemaakt naar paradigma: structured programming (C, Cobol), object-oriented programming (C++, Java, C#), functional programming (OCaml, Haskel, F#). 3GL-talen zijn echter wel [imperatief](https://nl.wikipedia.org/wiki/Imperatief_programmeren).

## GEN4

Deze generatie van programmeertalen kenmerken zich door non-procedurele karakter omdat deze [declaratief](https://nl.wikipedia.org/wiki/Declaratieve_taal) van aard zijn. De programmeur geeft, in bijna menselijke taal, een opdracht waarbij de opdracht alleen beschrijft *wat* het verwachte resultaat is. De applicatie bepaalt zelf wel *hoe* dat resultaat wordt bereikt. De bekendste declaratieve taal is `SQL`. Maar ook opmaak-talen als `HTML` en `XML` behoren hiertoe.

Soms worden ook Low-code/No-code platformen als Mendix & OutSystems hiertoe gerekend.

## De 5<sup>de</sup> Generatie

In de jaren '80 (van de vorige eeuw) zijn er al pogingen ondernomen om een nieuwe generatie computers & talen te ontwikkelen waarbij een computer een "probleem" kan oplossen door aan het programma een set van "contraints" op te geven (constraint-based, logic programming). Het idee was dat een programmeur dus niet meer een serie van algoritmes hoeft te schrijven maar dat een computer dat zelf kan doen.

Die pogingen zijn destijds gesneuveld niet alleen omdat de hardware & software niet toereikend waren. Het was ook omdat het afleiden van een efficiënt algoritme om het probleem op te lossen, op zichzelf een heel moeilijk probleem is (gegeven een reeks beperkingen die een bepaald probleem definiëren).

Met de komst van cloud-computing, met zijn schier onuitputtelijke hoeveelheid compute, en de daaruit voortvloeiende ontwikkelingen op het gebied van AI beginnen er weer nieuwe mogelijkheden te ontstaan. Lees: co-pilots. Met co-pilots (en de daarbij behorende LLM's -Large Language Models-) kan je in mensentaal opdrachten geven aan de computer.

Is "prompt-engineering" echt programmeren?

---
Voor meer informatie, zie:

1. https://en.wikipedia.org/wiki/Programming_language_generations
2. https://en.wikipedia.org/wiki/Non-structured_programming
3. https://en.wikipedia.org/wiki/Assembly_language
4. https://en.wikipedia.org/wiki/Structured_programming
5. https://nl.wikipedia.org/wiki/Declaratieve_taal
6. https://nl.wikipedia.org/wiki/Imperatief_programmeren
7. https://en.wikipedia.org/wiki/Fourth-generation_programming_language
8. https://en.wikipedia.org/wiki/Fifth-generation_programming_language


---

🍐 schrijft elke week een stukje. Over ... van-alles-en-nog-wat. 
En vooral over programmeren, techniek en hoe jij je daar, als &#9432;Naut toe kan verhouden.

---
