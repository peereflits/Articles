*Over ...*

# Over Intention Revealing Programming

In mijn column van vorige week "Over *wat* en *hoe*" liet ik het volgende code voorbeeld zien:

```java
public int Add(int term1, int term2) {
    return term1 * term2;
}
```

*De functiesignatuur (de wat) vertelt dat het twee getallen optelt en het resultaat (de som) ervan terug geeft. De body van de functie (de hoe) zegt dit te realiseren door de eerste input variabele te vermenigvuldigen met de tweede.*

Dit bovenstaande voorbeeld levert natuurlijk meteen een enorme cognitieve dissonantie op. Maar er gaat nog meer fout. Ik onderscheid hier drie soorten, drie categorieën fouten. Ga eens uit van de aanroep `Add(2147483646, 2);`.

1. **Logisch fout:** deze is het gevolg van een verschil tussen daadwerkelijke uitkomsten en verwachte uitkomsten;
Afgaande op de naam van de functie (wat doet het?), zou het resultaat van de functie 2.147.483.648 moeten zijn; niet 4.294.967.294. Maar wellicht zijn de uitkomsten correct (hoe doet de functie het?) en zet de naam je op het verkeerde been.
1. **Technisch fout:** dit is een fout als gevolg van wijzigingen "in de omgeving" en/of het gebruik waarop niet is geanticipeerd;<br/>Wat gebeurt er als de aanroep plaatsvindt? Een "Integer overflow exception". Defensief programmeren, goede foutafhandeling en de filosofie "Never trust public input" hanteren, zijn methoden om dit soort fouten enigszins tegen te gaan;
1. **Functioneel fout:** een functionele fout treed op wanneer een functie minder kan of doet (of juist te veel kan/doet) dan wat er wordt verwacht. Denk bijvoorbeeld aan: `Add(1.5, 3.333);` of `Add(1,2,3);`. Veelal liggen aan dit soort fouten onduidelijke, onvolledige, ambivalente of zelfs foute specificaties (requirements) ten grondslag.

Natuurlijk is de logische fout een flagrante schending van het adagium "Use Intention-Revealing Names". Zie pagina 18 in [Clean Code](https://www.amazon.com/Clean-Code-Handbook-Software-Craftsmanship/dp/0132350882 "Clean Code: A Handbook of Agile Software Craftsmanship"). En een houding van "The Code is the Truth", want dat is wat in productie draait, draagt ook niet bij aan het wegnemen van de verwarring. 

Wat mij vaak helpt wanneer ik tegen zo'n cognitieve dissonantie oploop, is te kijken wat de unit-testen vertellen over de verwachte uitkomsten. Wellicht zijn de uitkomsten correct en is de naam ietwat onzorgvuldig gekozen?

---

🍐 schrijft elke week een stukje. Over ... van-alles-en-nog-wat. 
En vooral over programmeren, techniek en hoe jij je daar, als &#9432;Naut toe kan verhouden.

---
