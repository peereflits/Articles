*Over ...*

# Over Compileren, Transpileren & Interpreteren

Als developer spreken we vaak over het compileren van "onze" code. En code in .NET of Java wordt zelfs in twee stappen gecompileerd.

Front-enders kennen het begrip "interpreteren" wellicht vanuit Javascript: dit is een geïnterpreteerde taal. En typescript wordt niet gecompileerd maar ge-transpiled?

Maar wat is nu precies wat?

Wanneer een computertaal wordt vertaald van een hogere generatie naar een lagere dan heet dat compileren. Dat vertalen wordt door een computer programma gedaan, die we [complier](https://nl.wikipedia.org/wiki/Compiler) noemen.

In Java wordt programma code vertaald van Java (3<sup>e</sup> generatie) naar Java-byte code (een assembly-taal -dat is een 2<sup>e</sup> generatie taal-). De Java runtime (JVM) vertaalt deze uiteindelijk maar machine instructies (= 1<sup>e</sup> generatie). Technisch gesproken heet deze stap "assembleren".

In .NET wordt iets vergelijkbaars gedaan: C# (3<sup>e</sup> generatie) wordt tijdens het "build"-en gecompileerd naar MSIL (Microsoft Intermediate Language -een assembly taal/2<sup>e</sup> generatie-). Tijdens het uitvoeren van de applicatie wordt deze MSIL via de JIT-compiler (Just-In-Time-compiler) vertaald van MSIL naar uitvoerbare machine code (op Windows-computers heet dat formaat "Portable Executable" [`PE`]). (Ik laat [AOT-compilation](https://learn.microsoft.com/en-us/dotnet/core/deploying/native-aot/) hier buiten beschouwing.)

Bij "transpilatie" wordt code vertaald van één formaat naar een ander formaat, waarbij beide formaten/talen van dezelfde generatie zijn. Een bekend voorbeeld is [TypeScript](https://www.typescriptlang.org/): TypeScript (3<sup>e</sup> generatie) wordt tijdens de transpilatie vertaald naar JavaScript (ook een 3<sup>e</sup> generatie taal). [Bicep](https://learn.microsoft.com/en-us/azure/azure-resource-manager/bicep/overview?tabs=bicep) wordt getranspileerd in [ARM templates](https://learn.microsoft.com/en-us/azure/azure-resource-manager/templates/). [Domain-specific-languages](https://en.wikipedia.org/wiki/Domain-specific_language) (DSL's) lenen zich doorgaans goed voor transpilatie.

[Script-talen](https://nl.wikipedia.org/wiki/Scripttaal), zoals Javascript, PHP e.a., worden (tijdens uitvoering) gelezen en vertaald naar iets wat een processor kan begrijpen (= 1<sup>e</sup> generatie = machine-instructies). Dit "lezen-en-vertalen" heet interpreteren en gebeurt regel-voor-regel. Script-talen zijn doorgaans langzamer dan code die gecompileerd wordt uitgevoerd.

Het compileren heeft voor- en nadelen; en dat geldt ook voor geïnterpreteerde talen. Maar dat is iets voor een volgende keer.

---

🍐 schrijft elke week een stukje. Over ... van-alles-en-nog-wat. 
En vooral over programmeren, techniek en hoe jij je daar, als &#9432;Naut toe kan verhouden.

---

> **NB:** In de openingszin spreek ik 'over het compileren van "onze" code.' Maar hoeveel van de code die jij schrijft, is daadwerkelijk van jou? Alle code die je schrijft tijdens een "klus" is niet van jou maar van de opdrachtgever. En de code die wordt gegenereerd door [GitHub Copilot](https://docs.github.com/en/copilot)? Is die van jou? Wat is jouw aandeel hierin?
