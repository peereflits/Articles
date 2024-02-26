*Over ...*

# Zeemeerminnen

"We are authors" zegt Robert C. Martin op pag. 13 in zijn boek "[Clean Code: A Handbook of Agile Software Craftsmanship](https://www.amazon.com/Clean-Code-Handbook-Software-Craftsmanship/dp/0132350882)" (een boek dat, naar mijn mening, elke zichzelf respecterende software ontwikkelaar gelezen zou moeten hebben). Wij zijn schrijvers en schrijven in een taal die "computer"- of "programmeer" heet.

De verhalen die we schrijven, schrijven we niet alleen in broncode. Omdat broncode + alles wat ermee samenhangt, doorgaans een (zeer) complex resultaat oplevert, schrijven we documentatie. Vaak niet van harte, omdat we ons liever uitdrukken in cryptische computer code dan in voor gewone stervelingen begrijpelijke mensentaal. Maar het hoort nu eenmaal bij de job.

Maar tekst alleen voldoet vaak niet. "A picture tells more than a 1.000 words". Daarom staan veel software architecten graag met een stift bij een white-board. Blokjes, lijntjes en diagrammen "spreken" zoveel makkelijker tot de technologische verbeelding dan de archaïsche proza van menselijke taal. 

Een tool, waar ik in het verleden mee heb gewerkt om diagrammen te maken, is mermaid.js. In mermaid teken je geen diagrammen maar beschrijf je deze in een markdown-achtige syntax. Het voordeel is dat dit "platte tekst" is, waardoor er bij wijzigingen in bijv. een class diagram, niet een apart tekenprogramma hoeft te worden opgestart en je ook geen versie beheer van tekeningen hebt: het is tekst in de documentatie zelf. Hierdoor hebt je minder snel kans dat er documentatie-rot (i.t.t. code-rot) ontstaat.

Een klein voorbeeldje van een flowchart diagram:

```
flowchart TD
    A[Christmas] -->|Get money| B(Go shopping)
    B --> C{Let me think}
    C -->|One| D[Laptop]
    C -->|Two| E[iPhone]
    C -->|Three| F[fa:fa-car Car]  
```

Dat ziet er dan zo uit:

[![](https://mermaid.ink/img/pako:eNpVkM1qw0AMhF9F6NRC_AI-FBq7zSWlhebm9UF45eyS7A9rmRBsv3vXMYVWJ6H5RgwzYRc0Y4n9Ndw6Q0ngVCsPeV6byiQ7iKOhhaJ4mQ8s4ILn-wz7p0OAwYQYrT8_b_x-haCajivGIMb6y7JJ1cP_6XmGujlSlBDbv8rpFmZ4a-yXye__KyZxdr03PZU9FR0lqCi1uEPHyZHVOfq0GhSKYccKy7xq7mm8ikLll4zSKOH77jssJY28wzFqEq4tnRO53yNrKyF9bG08Sll-ALI2XDY?type=png)](https://mermaid.live/edit#pako:eNpVkM1qw0AMhF9F6NRC_AI-FBq7zSWlhebm9UF45eyS7A9rmRBsv3vXMYVWJ6H5RgwzYRc0Y4n9Ndw6Q0ngVCsPeV6byiQ7iKOhhaJ4mQ8s4ILn-wz7p0OAwYQYrT8_b_x-haCajivGIMb6y7JJ1cP_6XmGujlSlBDbv8rpFmZ4a-yXye__KyZxdr03PZU9FR0lqCi1uEPHyZHVOfq0GhSKYccKy7xq7mm8ikLll4zSKOH77jssJY28wzFqEq4tnRO53yNrKyF9bG08Sll-ALI2XDY) 

Te gek hè, nietwaar?

Je kan een heleboel verschillende soorten diagrammen "schrijven": Flowchart, Sequence Diagram, Class Diagram, State Diagram, ERD e.v.a. 

Er is een [online editor](https://mermaid.live/) waarin je diagrammen kunt maken. In deze editor vind je ook (onder `Actions`) een `Copy Markdown`-knop waarmee je jouw diagram in markdown-formaat in een MD-bestand kunt plakken. 

De documentatie vind je [hier](https://mermaid.js.org/intro/).

Doe er je voordeel mee.

---

🍐 schrijft elke week een stukje. Over ... van-alles-en-nog-wat. 
En vooral over programmeren, techniek en hoe jij je daar, als &#9432;Naut toe kan verhouden.

---
