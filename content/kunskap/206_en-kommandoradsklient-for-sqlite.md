---
author: mos
category: sql
revision:
  "2015-06-05": (A, mos) Första utgåvan för htmlphp version 2 av kursen.
updated: "2015-06-05 13:40:03"
created: "2015-06-05 13:03:25"
...
En kommandoradsklient för SQLite
==================================

[FIGURE src=/image/snapvt15/sqlite3.png?w=c5&a=10,50,50,0 class="right"]

Programmet `sqlite3` är en kommandoradsklient för databsen SQLite. Med programmet kan du titta på databasens innehåll och skriva SQL-satser för att skapa tabeller och redigera innehållet i databasen. 

En kommandoradsklient är behändig för den som jobbar i terminalen. 

<!--more-->




Förutsättningar {#pre}
--------------------------------------

Du har koll på terminalen på [Mac OS](kunskap/terminalen-och-pakethantering-med-brew-pa-mac-os), [Linux](kunskap/terminalen-och-pakethantering-i-unix-linux) eller [Windows/Cygwin](kunskap/installera-unix-terminalen-cygwin-pa-windows) och du har koll på [databasen SQLite](kunskap/kom-igang-med-databasen-sqlite).



Installera kommandoradsklient `sqlite3` {#sqlite3}
--------------------------------------

Till databasen SQLite finns det en kommandoradsklient som heter `sqlite3`. 

På Mac OS finns den förinstallerad. 

På Linux och Windows/Cygwin installerar du den med pakethantering.

```text
# Linux
apt-get install sqlite3

# Windows/Cygwin
apt-cyg install sqlite3
```

Nu finns kommandot installerat. Dubbelkolla att det fungerar genom att visa upp hjälptexten.

```text
sqlite3 -help
```




Koppla upp sig mot en databas {#koppla}
--------------------------------------

Nja, koppla upp sig blir lite fel. SQLite är en filbaserad databas så man anger den filen som databasen finns i. För att testa kan du använde en exempeldatabas. Hämta den så här.

```text
wget -O jetty.sqlite https://github.com/mosbth/htmlphp/blob/master/example/sqlite/jetty.sqlite?raw=true

ls -l jetty.sqlite                       
-rw-r--r-- 1 mos mos 7.0K Jun  5 15:27 jetty.sqlite
```

Nu kan du öppna databasen och se vad den innehåller.

```text
sqlite3 jetty.sqlite 
```



Inspektera och fråga databasen {#inspekt}
--------------------------------------

Pröva följande kommandon för att bekanta dig med hanteringen.

```text
.help
.tables
.schema
```

Nu kan du ställa en SQL-fråga mot tabellen `Jetty`.

```sql
SELECT * from Jetty;
```

Så här kan det se ut när du jobbar med `sqlite3`.

[ASCIINEMA src=21079]



Avslutningsvis {#avslutning}
--------------------------------------

Det var ett par korta steg för att komma igång med kommandoradsklienten för SQLite. Ibland kan det vara det snabbaste sättet att tillgå och prata med en SQLite-databas.

Ställ gärna frågor om [SQLite och kommandoradsklienten i forumet](t/4308).




