*Over ...*

# Over het "relationele" van een relationele databases

Zeg nu zelf: wie gebruikt er bij het maken van een app, systeem of micro-service geen gebruik van een database? Een database is de defacto state van een applicatie. En niet zelden is dit een *relationele* database. Maar wat is er zo relationeel aan een relationele database? Of voluit: een relationele database management system (RDBMS).

Is dat het werken met tabellen? Zie figuur 1:

![Tabel](./2024-week-18%20table.png)<br/><cite>Figuur 1</cite>

Of zit het relationele van de database in het kunnen leggen van relaties tussen tabellen (foreign key constraints)? Zie figuur 2:

![Relatie](./2024-week-18%20erd.png)<br/><cite>Figuur 2</cite>

Is dat Figuur 1 of Figuur 2?


Het is "Figuur 1": in database parlando heet een tabel een relatie daar de waarde in een tabel wordt gevonden op het snijpunt van een tuple en een attribute. Het feit dat er tussen tabellen een "foreign key constraint" kan bestaan (figuur 2) is niet de reden waarom een relationele database "relationeel" heet; het is omdat de gegevens in een tabel-formaat worden opgeslagen.

Zie hieronder:

![A table is called a relation](./2024-week-18%20table_is_relation.png)<br/><cite>Figuur 3: A table is called a relation</cite>

> A relation, also known as a table or file, is a subset of the Cartesian product of a list of domains characterized by a name. And within a table, each row represents a group of related data values. A row, or record, is also known as a tuple. The columns in a table is a field and is also referred to as an attribute.<br/><cite>
https://opentextbc.ca/dbdesign01/chapter/chapter-7-the-relational-data-model/</cite>


Zie ook: [Why are Relational Databases “Relational”?](https://vertabelo.com/blog/why-are-relational-databases-relational/)


---

🍐 schrijft elke week een stukje. Over ... van-alles-en-nog-wat. 
En vooral over programmeren, techniek en hoe jij je daar, als &#9432;Naut toe kan verhouden.

---
