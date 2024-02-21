# Operatori

Operatori u JavaScriptu su simboli koji predstavljaju određene operacije te povezuju jedan ili više operanada u jedan izraz, bilo da je riječ o aritmetičkim, logičkim ili drugim operacijama.

Ovisno o broju operanada koje operator povezuje, razlikujemo unarne, binarne ili ternarne operatore.

## Operatori dodjeljivanja

Vrijednost varijabli se dodjeljuje korištenjem operatora dodjeljivanja. Najčešći operator dodjeljivanja je znak jednako `=`. Operator dodjeljivanja može se pisati zajedno s binarnim aritmetičkim operatorima. Primjerice, operator dodjeljivanja zbroja je `+=`, što je istovjetno s `x = x + y`.

```js
var x = 10;
var y = 5;
x += y; // x sada ima vrijednost 15 (x = x + y)
```

Tablica operatora usporedbe:

| Operator | Opis                                                                    |
|----------|-------------------------------------------------------------------------|
| =        | Dodjeljuje vrijednost varijable ili izraza s desne strane varijabli s lijeve strane (x = y;) |
| +=       | Zbraja dvije varijable i dodjeljuje zbroj varijabli s lijeve strane     |
| -=       | Oduzima dvije varijable i dodjeljuje razliku varijabli s lijeve strane  |
| *=       | Množi dvije varijable i dodjeljuje umnožak varijabli s lijeve strane    |
| /=       | Dijeli dvije varijable i dodjeljuje kvocijent varijabli s lijeve strane |
| %=       | Cjelobrono dijeli dvije varijable i dodjeljuje ostatak od dijeljenja varijabli s lijeve strane |

## Logički operatori

Logički operatori povezuju dva ili više logičkih izraza i vraćaju ovisno o vrijednosti logičkih izraza `true` ili `false`.

| Operator | Opis                                                                    |
|----------|-------------------------------------------------------------------------|
| &&       | Logički AND vraća vrijednost true ako su oba izraza true               |
| \|\|     | Logički OR vraća vrijednost true ako je barem jedan izraz true         |
| !        | Logički NOT vraća vrijednost true ako je izraz false odnosno false ako je izraz true |

## Uvjetni operator

Uvjetni operator ispituje je li uvjet ispunjen (vrijednost `true`) i ako je dodjeljuje vrijednost iza upitnika, a ako nije ispunjen vraća vrijednost iza dvotačke. Naprimjer:

```js
let email = "Da";
let poruka = (email == "Da") ? "Primio si poštu." : "Nema pošte.";
```

U ovom primjeru, ako je vrijednost varijable `email` jednaka "Da", varijabli `poruka` će biti dodijeljena vrijednost "Primio si poštu.". U suprotnom, bit će dodijeljena vrijednost "Nema pošte."
