*Over ...*

# Over goedkope opslag

Is opslag tegenwoordig goedkoop? Vergeleken met de prijzen van jaren geleden, lijkt het er inderdaad op dat de prijs per GB/TB enorm is gedaald. 

Maar dat betekent niet dat wij (= developers) niet meer hoeven na te denken over hoe we zaken in een database of op filesystem opslaan. 
De kosten van opslag behelzen meer dan alleen de kosten van disk/GB. 
Denk hierbij ook aan de grootte in geheugen, de grootte "on te wire" en de tijd die nodig is om gegevens (of een bestand) te verwerken!

**Stelling:**

`Larger size on disk => more read/write time => more throughput => more bandwidth => more memory usage => more energy => more money`

Voor database-ontwerp geldt, wat mij betreft, dan ook het advies: niet alle tekst-velden hoeven een ANSI/UTF-16/NVARCHAR (double byte) character set te hebben omdat dit vaak de standaard is. 

Denk bijvoorbeeld eens aan het opslaan van IBAN-nummers, telefoonnummers, kentekens of postcodes: deze passen in een ASCII character set (= single byte).

Voor hele grote datasets scheelt dit al snel de helft aan grootte zonder dat je informatie verliest.

Tel uit je winst!

> **NB:** Voor een overzicht van de geschiedenis van disk- & memory storage, zie:
> * https://en.wikipedia.org/wiki/History_of_hard_disk_drives
> * https://www.computerhistory.org/timeline/memory-storage/

---

🍐 schrijft elke week een stukje. Over ... van-alles-en-nog-wat. 
En vooral over programmeren, techniek en hoe jij je daar, als &#9432;Naut toe kan verhouden.

---
