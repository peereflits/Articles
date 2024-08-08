*Over ...*

# Over Programmeerparadigma's (VI)

Dit is het laatste artikel uit de serie **Programmeerparadigma's gaan niet over software**. 

*Programmeerparadigma's gaan niet alleen over software. Programmeerparadigma's gaan meer over hardware dan we denken. Een programmeerparadigma probeert een probleem op te lossen van het medium waarop het "leeft". In deze serie van artikelen leg ik uit welk paradigma welke hardware probleem oplost.*

## Deel 7: Conclusies

In de voorgaande artikelen heb ik gesproken over databases (relationeel & NoSQL), object oriëntatie, functional programming, internet / web programming en cloud computing.

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

In tabel-vorm:

| Paradigma | Medium | State | Taal |
| --------- | ------ | ----- | ---- |
| RDBMS databases        | Disk                 | durable, structured | Table, Key, CRUD, ACID |
| NoSQL databases        | Distributed disks    | durable, massive, schemaless | Document, Key-value, Column, Graph, CAP |
| Object Orientation     | Memory (RAM)         | volatile   | Encapsulation, Abstraction, Inheritance, Polymorphism |
| Functional Programming | Processor (-threads) | unmutable | first-class-, higher-order- and pure functions, recursion, referential transparency, currying |
| Web Programming        | Kabel                | stateless | Request/Response, ABC |
| Cloud Computing        | Rekencentra          | unlimited | SLA, IAAS, PAAS, SAAS |

Applicaties gebruiken veelal meerdere paradigma's: gegevens in de database, logica in het geheugen, publieke interface (API) "on the wire". 

En:

> Crossing the boundaries of a paradigm always aches due to a paradigm mismatch.

De bekendste hiervan is de [Object-relational impedance mismatch](https://en.wikipedia.org/wiki/Object-relational_impedance_mismatch)). Wees je ervan bewust dat er ook een object-request/response mismatch is!

Wordt de "next big wave" [Quantum computing](https://en.wikipedia.org/wiki/Quantum_computing)? Daar moet ik nog eens rustig over nadenken. Is het omdat quantum computing vragen kan beantwoorden die cloud computing/AI (nog) niet kan beantwoorden?

Ik hoop dat deze serie artikelen jullie het inzicht heeft verschaft dat ik heb beloofd: dat (programmeer-)paradigma's een sterkere relatie hebben met hardware dan dat je op het eerste gezicht zou denken.

Enjoy coding.<br/>
Stay curious.<br/>
Keep thinking!


---

🍐 schrijft elke week een stukje. Over ... van-alles-en-nog-wat. 
En vooral over programmeren, techniek en hoe jij je daar, als &#9432;Naut toe kan verhouden.

---
