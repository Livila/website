---
author: mos
revision:
    2016-11-14: (G, mos) Förenklade kraven och gjorde endast två delar.
    2016-11-04: (F, mos) Tillbaka och förtydliga krav om dubbla kolumner.
    2016-11-04: (E, mos) Bort med krav om dubbla kolumner.
    2016-11-01: (D, mos) Bort med krav om makefile för typografiskt grid.
    2016-10-31: (C, mos) Förtydligade hur man jobber med typografi och det hotrisontella gridet, kopiering kontra modifiering.
    2016-10-26: (B, mos) Omarbetad efter feedback.
    2016-06-22: (A, mos) Första utgåvan.
category:
    - kurs/design
    - tema
    - less
...
Bygg ut ditt tema med stöd för vertikalt och horisontellt grid
===================================

Du skall fortsätta utveckla ditt tema till Anax Flat. Du skall implementera stöd för ett vertikalt grid och för ett horisontellt grid. Du skall bygga ut ditt tema så att det blir responsivt och samtidigt fylla det med ett medvetet val av typografi.

<!--more-->



Förkunskaper {#forkunskaper}
-----------------------

Du har jobbat igenom artiklarna "[Använd ett vertikalt grid med Anax Flat](kunskap/anvand-vertikalt-grid-med-anax-flat)" och "[Skapa ett horisontellt grid för typografi](kunskap/skapa-ett-horisontellt-grid-for-typografi)".



Introduktion {#intro}
-----------------------

Du har en version av Anax Flat som ligger i katalogen `me/anax-flat`. Det är ett eget repo på GitHub som är taggat i minst version 2.\*.

Du har en version av temat som ligger i katalogen `me/anax-flat/theme`. Det är ett eget repo på GitHub som är taggat i minst version 2.\*.

En filosofi som kan komma till nytta här är [POGE - Principle of good enough](https://en.wikipedia.org/wiki/Principle_of_good_enough). Att försöka matcha gridet <abbr title="En sak eller uppfattning har drivits bortom vad som är rimligt.">in absurdum</abbr> kan vara kostsamt, beroende på ens förmåga.



Krav {#krav}
-----------------------



###Del 1 Vertikalt grid {#vertikalt}

1. Kopiera de grid-filer som finns i exemplet under `example/grid/fluid/less/grid*`. Lägg till dem så att de finns med i ditt tema. Lägg till båda i din `modules.less`, men kommentera bort den ena så att du bara har ett grid aktivt.

1. Skapa ett target för `upgrade-grid` i din Makefile som hämtar hem senaste versionen av grid-filerna från [kursrepot på GitHub](https://github.com/dbwebb-se/design/tree/master/example/grid/fluid/less).

1. Skapa en fil `modules/layout.less` där du stylar din Anax Flat enligt ditt valda grid. Förslagsvis använder du mellan 960px till 1200px som största storlek och du använder 12 eller 24 kolumner, eller välj efter eget huvud. Detta är nu basen i ditt aktiva tema. Kommentera bort din tidigare `modules/regions.less` så den inte används från `modules.less`.

1. Skapa en `modules/grid-helpers.less` och lägg en mixin som visualiserar gridet. Mixinen skall heta `.showGrid()` och ta ett argument som är gridets maximala storlek. De bilder du behöver lägger du enklast i `htdocs/img/grid`.

1. Skapa en ny sida `content/grid.md`. Lägg in den sidan i menyn. När man tittar på den sidan skall gridet visas i bakgrunden. Se till att sidan är fylld med innehåll. Sidan skall innehålla minst en [sidebar](t/5890) (sidebar-left eller sidebar-right) med innehåll.

1. Gör ditt tema responsivt med media queries och förberett för mindre skärmar.



###Del 2 Horisontellt grid (testa) {#horisontellt}

1. Aktivera det typografiska grider genom att kopiera de relevanta LESS-filer som finns i exemplet under `example/typography-grid/less/typography-*`. Lägg till dem så att de finns med i ditt tema. Aktivera typografin och förändra den som du vill.

1. Skapa en sida `content/typography.md`. Lägg in sidan i menyn. Fyll sidan med text och typografiska element som visar hur du stylat dem. Ungefär som textmassan som fanns i [exemplet](/repo/design/example/typography-grid/typography.html). När man tittar på sidan skall gridet visas i bakgrunden. De typografiska elementen skall *någorlunda väl* matcha gridet.

1. Gör så att alla regioner på sidan (till exempel flash, main och footer-regionerna) matchar det magiska numret och lutar mot det typografiska gridet. Använd `@magicNumber` där det finns möjlighet och jobba främst med `margin-bottom`. Gör det *tillräckligt bra*.



<!--

###Del 3 Typografisk layout (anpassa) {#typografi}

1. Ta exempelkoden för det horisontella grider och *gör den till din egen*. Du kan fritt modifiera grundfilerna för det horisontella grid som du kopierat i föregående steg.

1. Kodstruktur. Försök separera basen för ditt horisontella grid och din specifika anpassning av typografin. Lägg det som går att återanvända på en plats, och den specifika anpassningen på en annan plats, i dina LESS-moduler.

1. Bygg ut ditt tema med en egenvald typografisk layout. Gör ett aktivt val för typsnitt och storlekar och eventuella ramar, etc.
-->



###Klar och taggad {#tag}

1. Se till att ditt tema passerar testerna som körs vid `make test`.

1. Kör `git status`och se till att alla filer, som skall vara en del av dina båda repon `me/anax-flat` och `me/anax-flat/theme`, verkligen är en del av repot.

1. Du committar och taggar de båda repona som version 3.0.0.

1. Pusha upp repona till GitHub, inklusive taggarna.

1. Om du behöver göra fler taggar så gör du enligt 3.0.1, 3.0.2 och så vidare. Om du får komplettering så skall du alltid tagga en ny version när du är klar med kompletteringen samt pusha upp till GitHub.

1. Gör en `dbwebb publish` för att kolla att allt fungerar.

```bash
$ dbwebb publish me
```



Extrauppgift {#extra}
-----------------------

Det finns inga extrauppgifter.



Tips från coachen {#tips}
-----------------------

Ta det lugnt och försök förstå hur LESS-koden fungerar. Lägg också tid på att försöka finna en god struktur i hur du fördelar koden i dina LESS-moduler. Dela upp det som är grunden och återanvändbart kontra det som är specifik anpassning av grunden.

Kom ihåg att om du förändrar innehåll i temat så kan du även behöva committa och tagga om din version av Anax Flat, eftersom temats filer kopieras dit. Tipset är att tagga i slutet, när du känner dig klar.

Lycka till och hojta till i forumet om du behöver hjälp!
