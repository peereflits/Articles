*Over ...*

# Over Programmeerparadigma's (II)

Dit is het tweede deel uit de serie **Programmeerparadigma's gaan niet over software**. 

*Programmeerparadigma's gaan niet alleen over software. Programmeerparadigma's gaan meer over hardware dan we denken. Een programmeerparadigma probeert een probleem op te lossen van het medium waarop het "leeft". In deze serie van artikelen leg ik uit welk paradigma welk hardware probleem oplost.*


## Deel 2: Databases

Wie maakt er gebruik van een database bij het maken van (nieuwe) applicaties? En wie van jullie een *relationele* database? Wie eigenlijk niet? Databases zijn in de IT zo'n beetje alomtegenwoordig. Maar waarom gebruiken we eigenlijk (relationele) databases?

> **NB:** In database parlando heet een tabel een relatie. Het feit dat er tussen tabellen een "foreign key constraint" kan bestaan, is niet de reden waarom een relationele database "relationeel" heet; het is omdat de gegevens in een tabel-formaat worden opgeslagen [[1]](https://vertabelo.com/blog/why-are-relational-databases-relational/).

### Het waarom

Omdat relationele databases al zo heel lang bestaan, zijn er, vanaf de jaren '70, hele generaties programmeurs opgegroeid met de alomtegenwoordige beschikbaarheid van databases als MySQL, Ms Access, SQL Server, Oracle e.a.. Daarbij is ook het denken in tabellen gemeengoed geworden. Dus als "we" denken in termen van "opslaan" van POJO's / POCO's / records / models / entities, dan denken we vrijwel meteen aan "tabellen". En dus aan relationele databases. Zelfs met de relatief recente komst van NoSQL databases is dat niet anders (ik kom hier nog op terug).

Misschien moet ik de vraag anders stellen:<br/>
*Wat is het probleem dat relationele databases proberen op te lossen?*<br/>
Antwoord: dat is het oplossen van het probleem van gestructureerde gegevensopslag.

Wat is dat probleem?

Voordat er relationele databases bestonden (het RDBMS -Relational Database Management System-), moesten programmeurs zelf systemen programmeren die lezen en schrijven van en naar bestanden. Dat was (en is) een heidens karwei. En je kan je voorstellen dat daar fouten in werden gemaakt. Naast de tijdrovendheid en foutgevoeligheid van dat karwei was er nog een probleem: schijfruimte in die tijd was heel-heel-heel erg duur.

> **NB:** Voor een overzicht van de geschiedenis van disk- & memory storage, zie:
> * https://en.wikipedia.org/wiki/History_of_hard_disk_drives
> * https://www.computerhistory.org/timeline/memory-storage/

In 1970 schreef [Dr. Codd](https://en.wikipedia.org/wiki/Edgar_F._Codd "Edgar F. Codd") het baanbrekende artikel "[A Relational Model of Data for Large Shared Data Banks](https://learnsql.com/blog/codd-article-databases/)" waarin hij voorstelde om databases op basis van relationele algebra te beschrijven. Dit wordt nu het relationele model genoemd. Dit model had een aantal hele grote voordelen ten opzichte van de toendertijd bekende "network database model" en "hierarchical database model". Network- en hierarchical databases waren erg duur en complex in ontwikkeling en onderhoud. Met het gebruik van het relationele model kon men vele malen eenvoudiger gegevens beheren ten opzichte van de oudere opslagmodellen.

Op basis van dit artikel is later [SQL](https://learnsql.com/blog/history-of-sql/) ontstaan en het principe van [database normalisatie](https://en.wikipedia.org/wiki/Database_normalization). Data normalisatie is een methode om redundantie in (de structuur van) verzamelingen weg te modelleren. Een groot voordeel is dat gegevens in deze vorm opslaan veel minder ruimte in beslag neemt (als je tenminste de derde normaal vorm [3NF] gebruikt). En dit gold (en geldt) zeker voor de andere vormen van data opslag in die tijd. Nogmaals: schijfruimte was in de jaren '70 & '80 heel erg duur.

**In essentie "leven" databases op de harde schijf.**

> **NB:** Sommige "disks" hebben weinig meer met schijven te maken, maar de 'D' in SSD is nog steeds die van "disk".

### NoSQL Databases

Toen het probleem van "dure schijfruimte" steeds minder een probleem werd, als gevolg van de ontwikkelingen op dat gebied, en in samenhang met de toegenomen rekenkracht en interconnectiviteit tussen systemen, begon de hoeveelheid gegevens die in databases terecht kwam te groeien tot een hoeveelheid die een decennium ervoor nog niet voor mogelijk werd gehouden. En niet alleen de hoeveelheid data werd steeds meer een uitdaging. Ook ontstond steeds meer de behoefte om "ongestructureerde" data (zoals bijvoorbeeld PDF documenten) te kunnen "queriën".

Als gevolg van deze behoefte begon een aantal grote tech bedrijven te experimenteren met het bouwen aan grote gedistribueerde databases. Zo ontstond de [**N**ot-**O**nly-**SQL**](https://www.geeksforgeeks.org/difference-between-sql-and-nosql/) beweging met zijn [verschillende soorten databases](https://www.geeksforgeeks.org/types-of-nosql-databases/). Dit betekende het einde van het tijdperk van de alleenheersende relationele database (lees: SQL).

> **NB:** Voor meer info:
> * [Difference between SQL and NoSQL](https://www.geeksforgeeks.org/difference-between-sql-and-nosql/)
> * [The CAP Theorem in DBMS](https://www.geeksforgeeks.org/the-cap-theorem-in-dbms/)

De vraag die je zou moeten stellen, is:<br/>
*Wat is het probleem dat NoSQL databases proberen op te lossen?*<br/>
Antwoord: dat is het oplossen van het probleem van **massale ongestructureerde** gegevensopslag.

### Database == Disk

De reason d'être van "disk" is om "durable" state (persistente state) mogelijk te maken. Het medium "disk" kent zijn eigen taal (r/w). Databases "leven" binnen dit medium en hebben een paradigma dat aan dit medium schatplichtig is. De database paradigma/taal (SQL) gaat dus, in essentie, over het lezen en schrijven van bestanden naar disk. En het managen van de complexiteit hiervan is het oplossen van het probleem van gestructureerde gegevensopslag. Het managen van deze complexiteit is uitbesteed aan het RDBMS. Dit geldt analoog ook voor NoSQL oplossingen.

* Databases (RDBMS) zijn uiteindelijk ontstaan om efficiënter en kosteneffectiever gestructureerde gegevens (schema-bound data) op durable state (= disk) te beheren;
* NoSQL databases/systemen zijn ontwikkeld om efficiënter en kosteneffectiever massaal ongestructureerde gegevens (schemaless data) op gedistribueerde durable state te beheren.
  
Dat er niet zoiets als "overerving" bestaat in database talen, is omdat dit een concept is dat niet van toepassing is in het probleemdomein van "gestructureerde gegevensopslag".

---

🍐 schrijft elke week een stukje. Over ... van-alles-en-nog-wat. 
En vooral over programmeren, techniek en hoe jij je daar, als &#9432;Naut toe kan verhouden.

---
