# Programmeerparadigma's gaan niet over software (IV)

*TL;DR; Programmeerparadigma's gaan niet alleen over software. Programmeerparadigma's gaan meer over hardware dan we denken. Een programmeerparadigma probeert een probleem op te lossen van het medium waarop het "leeft". In deze serie van artikelen leg ik uit welk paradigma welk hardware probleem oplost.*

**Inhoudsopgave**

* [Deel 1](./deel-01-intro.md): Introductie
* [Deel 2](./deel-02-dbs.md): Databases (relationeel & NoSQL)
* Deel 3: Object oriëntatie
* [Deel 4](./deel-04-fp.md): Functional programming
* [Deel 5](./deel-05-wp.md): Internet / Web programming
* [Deel 6](./deel-06-cc.md): Cloud computing
* [Deel 7](./deel-07-conclusies.md): Conclusies
* [Referenties](./deel-08-referenties.md)


## Deel 3: Object oriëntatie

Wie van jullie maakt er bij het maken van nieuwe applicaties gebruik van een objectgeoriënteerde taal en/of framework? En vooral, *waarom* gebruiken jullie deze?

Voor de hand liggende antwoorden zijn: dit is wat ik heb geleerd op school of in de praktijk; dit wordt gebruikt bij de klant/in het project; Maar waarom wordt dit gedoceerd op opleidingen? Het wordt gevraagd door de industrie. En waarom vraagt de industrie om objectgeoriënteerde talen?

Om een probleem op te lossen!

Welk probleem? Wat voor probleem? 

De vraag die je zou moeten stellen, is:<br/>
*Wat is het probleem dat object oriëntatie probeert op te lossen?*<br/>
Antwoord: Object oriëntatie (OO) is een antwoord op het probleem van toenemende complexiteit.

> Goede object oriëntatie is het efficiënt toepassen van een effectieve "verdeel- en heerstactiek" op complexiteit.<br/>
*--- Peereflits ---*

Om te begrijpen wat die complexiteit behelst, moeten we eerst de geschiedenis van computers en hun programmeertalen eens bekijken.

### De geschiedenis van toenemende complexiteit

> In the beginning when we had no computers, we had no problems.<br/>Then when we had small computers, we had small problems.<br/>Now that we have big computers, we have big problems.<br/>*--- Edsger W. Dijkstra ---*

Toen de eerste computers werden ontwikkeld, bestond het beroep "software ontwikkelaar" niet. De eerste programma's die werden geschreven bestonden vooral uit een enorme sequentie van uitgeschreven processor instructies. Het scopen van routines was slechts mogelijk door het toepassen van `GOTO` statements. Hierdoor waren computer programma's nauwelijks leesbaar en werd dit soort code al snel "spaghetti code" genoemd. 

Om de problemen van "spaghetti code" het hoofd te kunnen bieden werden er aan computer talen [block structures](https://en.wikipedia.org/wiki/Block_(programming)) en [subroutines (functions)](https://en.wikipedia.org/wiki/Function_(computer_programming)) toegevoegd. En zo ontstond "[structured programming](https://en.wikipedia.org/wiki/Structured_programming)". Een belangrijk kenmerk van "Structured programming" is dat routines gescoped worden door "functions" en/of subroutines.

> **NB:** De Nederlands professor [Edsger W. Dijkstra](https://en.wikipedia.org/wiki/Edsger_W._Dijkstra) valt de eer ten deel de term "structured programming" te hebben uitgevonden.

En toen was het leven weer mooi. Totdat ...

Zoals jullie weten, kan je aan functies parameters meegeven. En hier begint het sprookje van structured programming scheuren te vertonen.

Functie modules uit die vroege tijd waren (soms) enorme libraries met niets anders dan alleen maar (publieke) methodes. Windows libraries als `kernel32.dll` en `user32.dll` zijn nog steeds niets anders dan grote bakken met "procedurele" functies. En als een methode/functie meer of andere functionaliteit moest gaan ondersteunen, dan werden er vaak parameters aan een functie toegevoegd om die functionaliteit te kunnen ondersteunen.

> **NB:** Ik ben ooit eens een methode tegen gekomen (in Visual Basic) waarbij de signatuur uit 22 parameters bestond en 2409 karakters lang was om te lezen. De functie body was een enorme spaghetti van `If-Then-Else-en` en loops. Deze was meer dan 800 regels lang.

Als het aantal parameters van een functie toeneemt, neemt ook de [cyclomatische complexiteit](https://en.wikipedia.org/wiki/Cyclomatic_complexity) toe. Cyclomatische complexiteit wordt bepaald door de hoeveelheid mogelijke paden die de code in en functie kan doorlopen. `Grotere cyclomatische complexiteit == meer complexiteit`. En we weten ook: Complexity kills!

![Complexity kills. It sucks the life out of users, developers and IT. Complexity makes products difficult to plan, build, test and use. Complexity introduces security challenges. Complexity causes administrator frustration.](complexity_kills.png)

Toen een aantal knappe koppen hierover nadachten, ontstond het idee: als we nu eens het gedrag en de bijbehorende data van een functionaliteit (= één functie) zouden kunnen encapsuleren in één construct, één ding, één object ... ? En voilà: hier heb je "object oriëntatie".

### Object oriëntatie 101

[Object oriëntatie](https://en.wikipedia.org/wiki/Object-oriented_programming) is al "uitgevonden" in de jaren '60. Maar het duurde tot eind jaren '80 voordat OO echt gemeengoed werd. Ook wordt OO tegenwoordig anders begrepen dan in haar ontstaansfase. Zaken als "inheritance" & "polymorphism" zijn geen concepten in de oorspronkelijke opzet van OO. Zie [The Forgotten History of OOP](https://medium.com/javascript-scene/the-forgotten-history-of-oop-88d71b9b2d9f). Dat er tegenwoordig anders over wordt gedacht is, volgens mij, o.a. een gevolg van het feit dat veel OO-talen inmiddels multi-paradigmale computertalen zijn geworden.

Wie weet wat de vier uitgangspunten van OO zijn? Zoek maar eens op internet naar "four tenets/pillars/principles of object oriented programming" en je krijgt dit lijstje:

* Encapsulation
* Abstraction
* Inheritance
* Polymorphism

### Over Abstraction, Inheritance en Polymorphism

> Program against abstractions, not concretions.<br/>*--- OO Design principle ---*
 
Over "Abstraction" wordt vaak iets geroepen als dat het iets is dat gemodelleerd is naar iets uit te "echte" werkelijkheid. Soms wordt ook nog het concept "interface" genoemd. "Inheritance" definieert een "is-een" of "heeft-een" relatie tussen objecten (een vis "is-een" dier). En "Polymorphism" is een "het-kan" relatie tussen objecten (een vogel "kan" vliegen).

> Voor elk probleem is in OO wel een juist abstractie niveau te vinden. Behalve voor het probleem van teveel abstracties.<br/>*--- [The Problem Solver](https://www.theproblemsolver.nl/) ---*

Maar daar gaat het helemaal niet om! Deze drie begrippen gaan maar over één ding: contract! Zowel abstractie (=interface) als overerving en polymorfisme worden in C# op één en dezelfde manier uitgedrukt:

```csharp
public interface ICanFly { ... }             // Abstraction
    
public abstract class Animal { ... }         // Abstraction

public abstract class Mammal: Animal { ... } // Inheritance

public class Bat: Mammal, ICanFly { ... }    // Inheritance & Polymorphism
 ```
       
Er wordt in alle drie de gevallen gebruik gemaakt van de inheritance operator "`:`". Waarom? Het gaat in alle gevallen om het gegeven dat een class aan een contract voldoet. En waarom is dat dan zo belangrijk?

Toen OO een grote vlucht begon te nemen, werd "inheritance" bejubeld als één van haar meest belangrijkste features. Maar dit jubelen werd vooral gedaan door IT-managers die "inheritance" vooral vertaalde in herbruikbaarheid. In de documentatie van Microsoft wordt dit nog steeds aangehaald:

> Inheritance enables you to create new classes that reuse, extend, and modify the behavior defined in other classes.<br/>*--- [bron: microsoft](https://learn.microsoft.com/en-us/dotnet/csharp/fundamentals/object-oriented/inheritance) ---*

Ik maak een nieuwe functionaliteit (= `class`). Jij wilt deze functionaliteit ook, maar dan net even iets anders. Dan overerf je mijn class en pas je het gedrag aan naar jouw smaak en hoef je niet zelf alles opnieuw te schrijven (inclusief de bugs) en breek je bestaande implementaties niet. Zie hier: herbruikbaarheid door "inheritance".

> Favor polymorphism over inheritance.<br/>*--- OO Design principle ---*

De developer blij want eenvoudig (ahum). De manager blij want de developer is sneller klaar (met minder bugs). Bedrijf blij, want `sneller == goedkoper`.

### De contract georiënteerdheid van OO

Maar er zit nog een ander verhaal achter deze "inheritance" / herbruikbaarheid. En deze begint bij de vraag: waar "leeft" een (in een OO-taal geschreven) programma? In welk medium?

Programma's leven primair in het RAM-geheugen van een computer. Dat zal niemand verbazen. Computertalen en compilers moeten dus slim kunnen omgaan met geheugen en het beheren ervan. De werkelijke reden achter de contract georiënteerdheid van OO zit in het feit dat met "fixed contracts" geheugenblokken beter te beheren zijn.

En hier begint mijn redenatie wankel te worden. Ik heb jaren geleden een artikel gelezen dat de start betekende van dit verhaal. Dat artikel kan ik helaas niet meer terugvinden. Vooral één van de afbeeldingen erbij was voor mij een eye-opener. Het eerste kwartje viel!

In dat artikel legde de auteur uit dat in een objecten-hiërarchie van overerfde objecten in een OO-programmeertaal (C++?) delen van geheugenblokken werden hergebruikt omdat zij dezelfde geheugen-layout deelden. Iets met pointers, structs en v-tables enzovoort. In de afbeelding eronder was dit schematisch zeer verhelderend uitgetekend. Het hebben van dezelfde geheugen-layout was mogelijk doordat er aan een "contract" werd voldaan (een vis "is-een" dier). Hierdoor konden geheugenblokken worden gedeeld en werd geheugenruimte genormaliseerd (lees: ontdubbeld, zoals in database-normalisatie). Deze normalisatie leidde dan tot een kleinere memory-footprint en dat was weer voordelig. Want in die tijd was geheugen duur en zeker niet onbeperkt adresseerbaar (wie kent de 640Kb limiet in MS-Dos nog?).

### OO == RAM

Het managen van het geheugen is iets wat gemakkelijk fout kan gaan wanneer je dat zelf moet doen (lees: null-pointers). Java & .NET/C# zijn ook "expres" uitgevonden om o.a. dit probleem op te lossen.

Van OO wordt ook wel gezegd dat het gaat om het managen van state. Mijn stelling is:

`Inheritance == herbruikbaarheid van functionaliteit;`<br/>
`Inheritance == herbruikbaarheid van code;`<br/>
**`Inheritance == herbruikbaarheid van geheugen!`**

> OO is about managing state.<br/>*--- General opinion ---*

Een kenmerk van (RAM-)geheugen is dat zij zeer vluchtig is. `RAM == volatile state``. De grammatica van het managen deze "volatile state" bestaat uit begrippen als: heap, stack, struct, v-table, allocation, de-allocation, GC, lock e.a.. en is een zeer complexe aangelegenheid. Object oriëntatie is o.a. een poging een antwoord te geven op dit complexe probleem.

* OO is uiteindelijk ontstaan om efficiënter en goedkoper 'state' en complexiteit in een 'volatile medium' (= RAM) te beheren;

Dat er niet zoiets als een "foreign key constraint" bestaat in OO talen, is omdat dit een concept is dat niet van toepassing is in het probleemdomein van "object oriëntatie".
