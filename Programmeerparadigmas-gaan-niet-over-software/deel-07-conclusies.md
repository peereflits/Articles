# Programmeerparadigma's gaan niet over software (VII)

*TL;DR; Programmeerparadigma's gaan niet alleen over software. Programmeerparadigma's gaan meer over hardware dan we denken. Een programmeerparadigma probeert een probleem op te lossen van het medium waarop het "leeft". In deze serie van artikelen leg ik uit welk paradigma welke hardware probleem oplost.*

**Inhoudsopgave**

* [Deel 1](./deel-01-intro.md): Introductie
* [Deel 2](./deel-02-dbs.md): Databases (relationeel & NoSQL)
* [Deel 3](./deel-03-oo.md): Object oriëntatie
* [Deel 4](./deel-04-fp.md): Functional programming
* [Deel 5](./deel-05-wp.md): Internet / Web programming
* [Deel 6](./deel-06-cc.md): Cloud computing
* Deel 7: Conclusies
* [Referenties](./deel-08-referenties.md)


## Deel 7: Conclusies

Gefeliciteerd! Heb je de andere delen gelezen?

Samenvattend kom ik tot de volgende conclusies:

Programmeerparadigma's gaan niet alleen over software. Programmeerparadigma's gaan meer over hardware dan we denken. Een programmeerparadigma probeert een probleem op te lossen van het medium waarop het "leeft". Het gebruikt hierbij een taal die van dat medium afhankelijk is. En die taal is niet van toepassing op een ander medium. Dat medium is een onderdeel van de computer zoals geheugen, disk, processor, IO/(netwerk-)kabel, of zelfs de hele computer zelf in geval van cloud computing. Het op te lossen probleem heeft vaak de maken met "state". Het heeft vrijwel altijd te maken met geld want de oplossing is (uiteindelijk) efficiënter en effectiever. Lees: goedkoper.

> ~~OO is about managing state.~~<br/>OO is about managing *volatile* state.


* **Relationele databases**
   * gaan over het beheren van 'state' op een duurzaam medium
   * omdat een RDBMS database "leeft" op "één" disk (state on durable media)
   * deze 'state' is "structurered state"; oftewel schema gebonden data;
* **NoSQL databases**
   * gaan over het beheren van massale hoeveelheden 'state' op duurzame media
   * omdat een NoSQL database "leeft" op "vele" disks (= data lake)
   * deze 'state' is "unstructurered state"; oftewel niet-schema gebonden data in een gedistribueerde massa opslag;
* **Object oriëntatie**
   * gaat over het beheren van 'state' en gedrag (=complexiteit) in een vluchtig medium (volatile media)
   * omdat een programma "leeft" in het geheugen (RAM);
* **Functional Programming**
   * gaat over het beheren van 'state' als gedrag (=complexiteit) op een medium zonder state
   * omdat berekeningen "leven" in processor-threads;
* **Web Programming**
   * gaat over het beheren van niet-locatie gebonden 'state' en gedrag op een "stateless" medium
   * omdat web-applicaties "leven" op de kabel;
* **Cloud Computing**
   * gaat over het beheren van meerdere locatie-ongebonden systemen (data, gedrag en complexiteit)
   * omdat deze "leven" in een datacenter;

In zijn meest gecondenseerde vorm:

* Disk == durable structured state => RDBMS databases
* Distributed disks == durable schemaless state => NoSQL databases
* Memory == volatile state => OO
* Processor (-threads) == no state => FP
* Wire == stateless => WP
* Cloud == massive state => CC

Applicaties gebruiken veelal meerdere paradigma's: gegevens in de database, logica in het geheugen, publieke interface (API) "on the wire". 

En:

> Crossing the boundaries of a paradigm always aches due to a paradigm mismatch.

De bekendste hiervan is de [Object-relational impedance mismatch](https://en.wikipedia.org/wiki/Object-relational_impedance_mismatch)). Wees je ervan bewust dat er ook een object-request/response mismatch is!

Wordt de "next big wave" [Quantum computing](https://en.wikipedia.org/wiki/Quantum_computing)? Daar moet ik nog eens rustig over nadenken. Is het omdat quantum computing vragen kan beantwoorden die cloud computing/AI (nog) niet kan beantwoorden?

Ik hoop dat dit artikel jullie het inzicht heeft verschaft dat ik heb beloofd: dat (programmeer-)paradigma's een sterkere relatie hebben met hardware dan dat je op het eerste gezicht zou denken.

Rest mij af te sluiten met: bedankt voor het lezen.

Enjoy coding.<br/>
Stay curious.<br/>
Keep thinking!
