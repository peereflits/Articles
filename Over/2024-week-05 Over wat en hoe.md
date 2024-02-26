*Over ...*

# Over *wat* en *hoe* (declaratief versus imperatief)

De vraagwoorden *wat* en *hoe* zijn van fundamenteel belang binnen de wereld van software development.

> In de informatica worden computertalen ingedeeld in  [declaratieve talen](https://nl.wikipedia.org/wiki/Declaratieve_taal "declaratieve talen op Wikipedia") en [imperatieve talen](https://nl.wikipedia.org/wiki/Imperatief_programmeren "imperatieve talen op Wikipedia"). Heel kort gezegd is dat men in een declaratieve taal opschrijft <em>wat</em> er moet gebeuren, en in een imperatieve taal <em>hoe</em> iets moet gebeuren om wat te bereiken. Een volkomen helder onderscheid is niet te maken.<br/>
<cite>--- Wikipedia ---</cite>

Een functie in een imperatieve taal laat het verschil zien: de signatuur van een functie openbaart "wat" het doet; een body van een functie beschrijft "hoe" het dat doet. Zie het onderstaande voorbeeld:

```java
public int Add(int term1, int term2) {
    return term1 * term2;
}
```

De functiesignatuur (de wat) vertelt dat het twee getallen optelt en het resultaat (de som) ervan terug geeft. De body van de functie (de hoe) zegt dit te realiseren door de eerste input variabele te vermenigvuldigen met de tweede.

Bij declaratieve talen hoeft de hoe-vraag niet meer gesteld te worden; dat lost de "runtime" voor je op. In het geval van SQL (de meest bekende declaratieve taal) is dit het RDBMS. Derhalve hoef je je alleen te concentreren op de wat-vraag: geef deze velden (`SELECT`-clause) uit deze tabellen (`FROM`-clause) waarvoor geldt dat &lt;predicate&gt; (`WHERE`-clause). Waar de database de tabellen en veldwaarden opslaat of ophaalt (hoe) dat regelt de database engine zelf.

HTML, XML en CSS zijn ook declaratieve talen.

Nu lijken declaratieve talen makkelijker dat imperatieve: je hoeft namelijk één vraag minder te beantwoorden. "Geef mij ... " (wat). En hoe? Dat mag een runtime zelf uitzoeken.

Nu lijkt er een trend gaande om software steeds makkelijker te maken met de low-code/no-code beweging als meest recente voorbeeld. Waarom zijn er dan niet veel meer declarative talen ontstaan en main-stream geworden (SQL uitgezonderd)?

Omdat gedrag heel erg moeilijk volledig declaratief is uit te schrijven (zo niet onmogelijk). Events (een reactie op een gebeurtenis -dat is gedrag-) zijn bijvoorbeeld zaken die niet goed declaratief zijn te beschrijven. Daarom worden beide soorten veelal door elkaar gebruikt.

Het bekendste voorbeeld? HTML + CSS (declaratief) + Javascript (imperatief).


---

🍐 schrijft elke week een stukje. Over ... van-alles-en-nog-wat. 
En vooral over programmeren, techniek en hoe jij je daar, als &#9432;Naut toe kan verhouden.

---
