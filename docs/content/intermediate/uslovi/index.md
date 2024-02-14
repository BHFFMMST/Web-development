## Provjere (If Statements) u JavaScriptu

Provjere omogućuju programima da donose odluke na temelju uslova. U JavaScriptu postoje tri osnovna oblika provjera: `if`, `if...else` i `switch`.

### If Statement

Provjerava je li navedeni uslov istinit. Ako je uslov istinit, izvršava se blok koda unutar if petlje.

```
let temperature =  30;
if (temperature >=  30) {
  console.log("It's hot outside!");
}
```

### If...Else Statement

Provjerava je li navedeni uslov istinit. Ako je uslov istinit, izvršava se blok koda unutar if petlje. Ako nije, izvršava se blok koda unutar else petlje.

```
let temperature =  20;
if (temperature >=  30) {
  console.log("It's hot outside!");
} else {
  console.log("It's cold outside.");
}
```

### Switch Statement

Omogućuje upoređivanje jedne promenljive s više mogućih vrijednosti. Svaka vrijednost ima svoje blok koda koje se izvršavaju kada se uslov zadovoljava.

```
let fruit = "apple";
switch (fruit) {
  case "banana":
    console.log("Bananas are good for healthy living.");
    break;
  case "apple":
    console.log("Apples are tasty and crunchy.");
    break;
  default:
    console.log("I like all fruits!");
}
```

### Ternary Operator

Kratka sintaksa za if...else provjeru. Prva vrijednost predstavlja uvjet, druga vrijednost rezultat ako je uvjet istinit, a treća vrijednost rezultat ako je uvjet lažan.

```
let age =  15;
let beverage = (age >=  21) ? "Beer" : "Juice";
console.log(beverage); // Juice
```

### Razlika između == i ===

Operator `==` provjerava samo vrijednosti, dok operator `===` provjerava vrijednosti i tipove. To znači da `==` može vratiti `true` za dvije različite vrste podataka, dok `===` vratit će `false`.

```
0 == "0"  // true
0 === "0" // false
```

Provjere su ključni deo programerskog jezika jer omogućuju dinamičko izvršavanje koda na temelju stanja aplikacije ili uticaja na korisnika.
