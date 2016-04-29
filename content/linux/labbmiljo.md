---
author: mos
revision:
  "2015-06-26": (A, mos) Första utgåvan.
category: unix
...
Introduktion till labbmiljö i linux
==================================

Här får du en snabb översikt för att se vilka verktyg och applikationer du behöver installera för att erhålla den labbmiljö som krävs för kursen linux.

<!--more-->

Du kan se detta som en referensinstallation av labbmiljön. Det är inget absolut krav att din miljö ser ut så här. Du kan välja alternativa vägar. Men, om du hamnar i bekymmer så får du komma tillbaka hit och göra som det står här.



Operativsystem  {#os}
---------------------------------

Till din primära utvecklingsmiljö kan du använda Windows, Mac OS eller någon variant av Linux/Unix. Du undviker enklast eventuella problem genom att hålla dig till de senaste versionerna av operativsystemen.

Om du kör Windows, se då till att göra det som en användare som har Administratörsrättigheter.

Behöver du hjälp med frågor om operativsystem så finns följande subforum.

* [Windows för Webbprogrammerare](forum/viewforum.php?f=55)
* [Unix och Linux](forum/viewforum.php?f=49)



Texteditor {#editor}
---------------------------------

I kurserna används texteditorn Atom som standard. Men du kan i princip välja en annan editor, eller utvecklingsmiljö, om du vill. Så länge editorn klarar av *soft tabs*, *tab-size 4 spaces*, *UTF-8 NOBOM*, samt *Unix-style line endings*.

Du [installerar Atom från dess webbplats](https://atom.io/).

Här är en guide till hur du [installerar och kommer igång med Atom](kunskap/installera-texteditorn-atom).



Terminal {#terminal}
---------------------------------

Du behöver ha tillgång till en terminal där du kan köra Unix-kommandon. På Unix/Linux och Mac har du alltid en terminal, men på Windows behöver du installera en Unix-terminal i form av [Cygwin](https://www.cygwin.com/).

På ett Unix-system använder man ofta en pakethanterare för att installera, uppdatera och avinstallera de program som finns. Det är ett enkelt sätt att hålla sitt system uppdaterat. Olika operativsystem har olika pakethanterare.

Här är guider för hur du kommer igång med terminalen, för respektive operativsystem.

* [Installera Unix-terminalen Cygwin på Windows](kunskap/installera-unix-terminalen-cygwin-pa-windows)
* [Terminalen och pakethantering med Brew på Mac OS](kunskap/terminalen-och-pakethantering-med-brew-pa-mac-os)
* [Terminalen och pakethantering i Unix/Linux](kunskap/terminalen-och-pakethantering-i-unix-linux)

Om du är osäker på grunderna i en Unix-terminal så finns det en [guide som hjälper dig att komma igång med Unix på kommandoraden](kunskap/20-steg-for-att-komma-i-gang-med-unix-och-terminalen).



Git {#git}
---------------------------------

Versionshanteringverktyget Git används till och från i kurserna. Du behöver ha det installerat på din dator. På Mac finns Git redan för-installerat, så använder du en senare utgåva av Mac OS så behöver du inte göra något.

Du kan [installera det från Gits hemsida](http://git-scm.com/download).

Här är en [guide till hur du installerar Git](kunskap/installera-versionshanteringssystemet-git).



Webbläsare  {#webblasare}
---------------------------------

Se till att du har minst [Firefox](https://www.mozilla.org/download) och [Google Chrome](https://www.google.com/chrome/) installerade på din dator. Vi använder Firefox som referens. Om det visar sig att koden fungerar olika i olika webbläsare så testar vi alltid i Firefox.

I Firefox behöver du även [installera pluginen Firebug](http://getfirebug.com/) som är ett utvecklarverktyg för Firefox.

Här en guide för att dig som vill se [hur Firebug fungerar](coachen/kom-i-gang-och-installera-firebug-som-utvecklarverktyg).




VirtualBox {#vb}
--------------------------------------

I kursen använder vi virtualiseringsmiljön VirtualBox för att installera Debian/Linux. Det är en central del av kursen.

Här är en guide hur du "[Installera virtualiseringsmiljön VirtualBox](kunskap/installera-virtualiseringsmiljon-virtualbox)".

Även om du väljer att köra Debian på en annan server så är det en bra idé att bekanta sig med VirtualBox. Det är ett utmärkt verktyg som passar en webbprogrammerar.



Debian som server {#debian}
--------------------------------------

I kursen har vi senaste stabila versionen av Debian Linux som referenssystem och vi använder det som en server. 

Här är guiden hur du "[Installera Debian (på VirtualBox)](kunskap/installera-debian-pa-virtualbox)".

Du kan också välja att installera Debian på annat vis. Vi kommer använda Debian som en server och du behöver installera ett antal saker på den. Det måste vara en separat maskin, så det kan inte vara samma maskin som din desktopmiljö. 

Alternativa sätt att köra kursen på är bland annat.

* Debian Linux på egen hårdvara.
* Debian Linux på en virtuell server.
* Rasbian på Raspberry Pi.
* Annan dialekt av Linux.
* Annan dialekt av Unix, likt FreeBSD med mera.

Om du väljer ett alternativt sätt så är det inte säkert att vi kan supporta dig. Det kan kräva att du själv löser vissa problem. Men det går säkert bra. Det är dialektala skillnader. Men om du är en erfaren Linux/Unix-användare så kommer du säkert att lösa det.



Avslutningsvis {#avslutning}
--------------------------------------

Nu har du kommit igång och du har den labbmiljö som krävs för att genomföra det första kursmomentet i kursen.

Om du stöter på problem så kan du alltid [fråga direkt i forumet om kursens forum](forum/utbildning/linux).



