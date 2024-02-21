# Naredbe grananja

U skriptnom jeziku JavaScript postoje više naredbi grananja:

| Naredba grananja           | Opis                                                                                     |
|----------------------------|------------------------------------------------------------------------------------------|
| if naredba                 | Koristi se za izvođenje različitih akcija ovisno je li zadani uvjet ispunjen ili nije.   |
| if...else naredba          | Omogućava veći nadzor nad izvođenjem ovisno o vrijednosti izraza.                         |
| if...else if naredba       | Omogućava izvođenje različitih dijelova koda ovisno o više uvjeta.                         |

## if naredba : if Statement

Kao i za većinu programskih jezika, i JavaScript ima na raspolaganju naredbu uvjeta (if naredbu) koja se koristi za izvođenje različitih akcija ovisno o tome je li zadani uvjet ispunjen ili nije.

Sintaksa if naredbe:

```javascript
if (izraz) {
    //if blok naredbi koje se izvršavaju samo ako je uvjet true;
}
```

Kod ove naredbe najprije se izračunava vrijednost izraza u zagradi. Ako je rezultat `true`, izvode se sve naredbe unutar vitičastih zagrada. Ako je vrijednost `false`, niti jedna naredba se neće izvršiti. Unutar izraza u zagradi često se koristi operator usporedbe. Naprimjer:

```js
var godina = 20;
if( godina > 18 ){
    document.write("<strong>Punoljetna osoba.</strong>");
}
```

Budući da je vrijednost varijable godina veća od 18, metoda `document.write` upisuje HTML kod:

```html
<strong>Punoljetna osoba.</strong>
```

## if...else naredba : if...else Statement

if...else naredba omogućava veći nadzor nad izvođenjem ovisno o vrijednosti izraza.

Sintaksa if...else naredbe:

```js
if (izraz) {
    // naredbe koje će se izvršiti ako je vrijednost izraza true;
} else {
    // naredbe koje će se izvršiti ako je vrijednost izraza false;
}
```

Kod ove naredbe najprije se izračunava vrijednost izraza u zagradi. Ako je rezultat `true`, izvode se sve naredbe unutar vitičastih zagrada nakon naredbe `if`. Ako je vrijednost `false`, izvode se sve naredbe unutar vitičastih zagrada nakon naredbe `else`. Naprimjer:

```js
var godina = 15;
if( godina > 18 ){
    document.write("<strong>Punoljetna osoba.</strong>");
} else {
    document.write("<strong>Maloljetna osoba.</strong>");
}
```

Budući da je vrijednost varijable godina manja od 18, metoda `document.write` upisuje HTML kod:

```html
<strong>Maloljetna osoba.</strong>
```

## if...else if naredba : if...else if Statement

if...else if naredba omogućava izvođenje različitih dijelova koda ovisno o više uvjeta.

Sintaksa if...else if naredbe:

```js
if (izraz1) {
    // naredbe koje će se izvršiti ako je vrijednost izraza true;
} else if (izraz2) {
    // naredbe koje će se izvršiti ako je vrijednost izraza 2 true;
} else if (izraz3) {
    // naredbe koje će se izvršiti ako je vrijednost izraza 3 true;
} else {
    // naredbe koje će se izvršiti ako su i izraz1, izraz2 i izraz3 false;
}
```

Niz if naredbi, svaki slijedeći `if` je dio else prethodne naredbe. `if` i `else if` dolaze u parovima. Prva naredba `else if` ispituje uvjet samo ako je izraz1 `false`. Ako je izraz1 `true`, niti jedna od preostalih naredbi `else if` se ne ispituje. Ako je izraz1 `false`, ispituje se izraz2, i tako dalje. Naprimjer:

```js
var info = "javascript";
if( info == "html" ){
    document.write("<strong>Vodič kroz HTML</strong>");
} else if( info == "css" ){
    document.write("<strong>Vodič kroz CSS</strong>");
} else if( info == "javascript" ){
    document.write("<strong>JavaScript vodič</strong>");
} else {
    document.write("<strong>Nepostojeći vodič</strong>");
}
```

Kao rezultat ovog primjera, `document.write` će upisati na web stranicu sljedeći HTML kod:

```js
<strong>JavaScript vodič.</strong>
```
