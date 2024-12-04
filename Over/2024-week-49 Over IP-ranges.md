*Over ...*

# Over IP-ranges

Vandaag wil ik het eens hebben over IP-range notaties. IP-**4** adres ranges dus, ook wel adresblok. Wanneer ik dit tegenkom, loop ik er telkens tegenaan dat ik moet opzoeken wat-het-ook-alweer-betekent. Maar eigenlijk is het niet zo moeilijk.

Een IP-adres bestaat uit 4 x een getal van 0 t/m 255 (=2<sup>8</sup> verschillende waarden) gescheiden door een punt: `xxx.xxx.xxx.xxx`. Daarmee zijn er maximaal 2<sup>8</sup>  x 2<sup>8</sup> x 2<sup>8</sup> x 2<sup>8</sup> = 2<sup>32</sup> == 4.294.967.296 IP adressen.

Nu zijn er een aantal adressen gereserveerd voor speciaal gebruik: zie [Reserved IP addresses](https://en.wikipedia.org/wiki/Reserved_IP_addresses). De bekendste adressen zijn:

* `10.x.x.x` voor private bedrijfsnetwerken
* `192.168.x.x` voor private thuis-netwerken
* `127.0.0.0` bekend als 'localhost'

Maar een computer draait zelden stand-alone; En voor het (goed) kunnen inrichten van een netwerk heb je een adressenreeks nodig: een IP block, zogezegd. En om te voorkomen dat je telkens "van X tot en met Y" moet opschrijven, is er een notatiemanier uitgevonden.

Zo'n “block” (of range) van adressen wordt aangeduid door achter een IP-adres `/x` te zetten waarbij `x` een getal is van 0 t/m 32 (dit is de 32 van 2<sup>32</sup>). De range wordt berekend door de som van 32 - `x` als macht van 2 te nemen. Dus:

<code># IP adressen = 2<sup>(32–x)</sup></code>

Oftewel:
* `0.0.0.0/0` zijn alle IP adressen ter wereld
* `192.168.0.0/32` is een reeks van 1 IP adres.

Deze adresnotaties komen niet voor.

Als handig opzoeklijstje:

| Notatie     |    # | Eerste IP | Laatste  |
| ---         | ---: | ---:    | ---:       |
| 10.0.0.0/32 |   1 | 10.0.0.0 | 10.0.0.0   |
| 10.0.0.0/31 |   2 | 10.0.0.0 | 10.0.0.1   |
| 10.0.0.0/30 |   4 | 10.0.0.0 | 10.0.0.3   |
| 10.0.0.0/29 |   8 | 10.0.0.0 | 10.0.0.7   |
| 10.0.0.0/28 |  16 | 10.0.0.0 | 10.0.0.15  |
| 10.0.0.0/27 |  32 | 10.0.0.0 | 10.0.0.31  |
| 10.0.0.0/26 |  64 | 10.0.0.0 | 10.0.0.63  |
| 10.0.0.0/25 | 128 | 10.0.0.0 | 10.0.0.127 |
| 10.0.0.0/24 | 256 | 10.0.0.0 | 10.0.0.255 |
| 10.0.0.0/23 | 512 | 10.0.0.0 | 10.0.1.255 |
| 10.0.0.0/22 | 1024 | 10.0.0.0 | 10.0.2.255 |
| 10.0.0.0/21 | 2048 | 10.0.0.0 | 10.0.3.255 |
| 10.0.0.0/16 | 65536 | 10.0.0.0 | 10.0.255.255 |
| 10.0.0.0/12 | 1048576 | 10.0.0.0 | 10.31.255.255 |
| 10.0.0.0/10 | 4194304 | 10.0.0.0 | 10.127.255.255 |
| 10.0.0.0/8  | 16777216 | 10.0.0.0 | 10.255.255.255 |

Doe er je voordeel mee.

---

🍐 schrijft elke week een stukje. Over ... van-alles-en-nog-wat. 
En vooral over programmeren, techniek en hoe jij je daar, als &#9432;Naut toe kan verhouden.

---
