## Sortiranje Nizova

JavaScript nudi razne metode za sortiranje nizova. Ove metode omogućuju sortiranje nizova na osnovu njihovih vrijednosti, obrnutim redoslijedom ili na osnovu specifičnih kriterija.

### Metode Sortiranja Nizova

#### Array sort()

Sortira elemente niza u alfabetske redoslijede i vraća sortirani niz.

```
let numbers = [40,  100,  1,  5,  25,  10];
numbers.sort((a, b) => a - b); // [1,  5,  10,  25,  40,  100]
```

#### Array reverse()

Obrće redoslijed elemenata unutar niza.

```
let numbers = [1,  2,  3,  4,  5];
numbers.reverse(); // [5,  4,  3,  2,  1]
```

### Math.min() i Math.max()

Vraćaju najmanji i najveći element u nizu, respektivno.

```
javascript
let numbers = [40,  100,  1,  5,  25,  10];
console.log(Math.min(...numbers)); //  1
console.log(Math.max(...numbers)); //  100
```

### Home Made Min() i Max()

Ručno implementirane funkcije za pronalaženje najmanjeg i najvećeg elementa u nizu.

```
javascript
function homeMadeMin(arr) {
    return arr.reduce((min, current) => current < min ? current : min, Infinity);
}

function homeMadeMax(arr) {
    return arr.reduce((max, current) => current > max ? current : max, -Infinity);
}

let numbers = [40,  100,  1,  5,  25,  10];
console.log(homeMadeMin(numbers)); //  1
console.log(homeMadeMax(numbers)); //  100
```
