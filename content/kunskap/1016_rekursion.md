---
author: lew
revision:
    "2017-02-08": (A, lew) First version.
category:
    - oopython
...
Rekursion
===================================

[FIGURE src=/image/oopython/kmom05/recursion_top.png?w=c5 class="right"]

Med rekursion menas en funktion som refererar till sig själv. Antingen direkt eller via en annan funktion. Det handlar om ett annat tankesätt än vad vi är vana vid, till exempel for-loopar och andra iterativa och linjära tankesätt.

<!--more-->



Förutsättning {#pre}
-------------------------------

Du kan grunderna i Python och du vet vad variabler, typer och funktioner innebär.



The Three Laws of Recursion {#the-three-laws-of-recursion}
------------------------------

Rekursion har tre lagar (The Three Laws of Recursion):  

1. En rekursiv algoritm måste ha ett basfall

2. En rekursiv algoritm måste ändra sitt tillstånd och arbeta sig mot basfallet

3. En rekursiv algoritm måste kalla på sig själv, rekursivt.

En viktig sak att tänka på är att det är lätt att hamna i ett "infinite" läge. Tänk dig följande kod som är tänkt att summera alla heltal från 1 till n:  

```python
def recursive_sum(n):
    # Här kallar vi på funktionen rekursivt
    return n + recursive_sum(n-1)

```

Den kommer aldrig sluta snurra, då vi inte har ett basfall. Vi behöver en tröskel där det tar stopp och rekursionen avslutas:
```python
def recursive_sum(n):
    # Här är basfallet. När n kommer till 1 så returneras bara värdet.
    if n <= 1:
        return n
    else:
        # Vi ändrar tillståndet och jobbar oss mot basfallet
        return n + recursive_sum(n-1)
```

Nu uppfyller vi alla 3 kraven. Ett tips är att alltid börja implementera basfallet för att förhindra ett infinite-läge.



Varför rekursion? {#varfor-rekursion}
------------------------------

Om man ska använda rekursion eller inte beror på olika faktorer. Som med allt annat så finns det fördelar och nackdelar jämfört med en iterativ funktion.  

###Fördelar {#fordelar}  

1. Rekursiva funktioner gör att koden blir renare.  
2. En komplex uppgift kan brytas ner till små problem.  
3. Beroende på problem kan det vara enklare med en rekursiv funktion.  



###Nackdelar {#nackdelar}  

1. Rekursiva funktioner tar upp mer minne.  
2. Rekursiva funktioner är ofta långsammare.
3. Rekursiva funktioner är svårare att debugga.
4. Rekursiva funktioner kan vara svåra att förstå.  



Typer av rekursion {#typer-av-rekursion}
------------------------------

###Linear recursion {#linear-recursion}  

"Linear recursion" är när en rekursiv funktion kallar på sig själv en gång varje gång funktionen körs. Det är den vanligaste modellen av en rekursiv funktion.  

###Tail recursive {#tail-recursion}  

"Tail recursion" är en form utav Linear recursion. Det rekursiva anropet är det sista som görs i funktionen, vilket gör att den passar bra för iterativa funktioner. Om man byter ut det rekursiva anropet mot en loop kan samma resultat uppnås.  


###Binary recursive {#binary-recursion}  

"Binary recursions" har två eller fler rekursiva anrop i funktionen.



Avslutningsvis {#avslutning}
------------------------------  

Rekursion kan vara en ovärderlig struktur, vid rätt tillfälle. Oftast klarar man sig bra med vanliga loopar men med den här vetskapen finns i alla fall alternativet till hands.
