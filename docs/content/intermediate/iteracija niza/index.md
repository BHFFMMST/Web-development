## Iteracija Nizova

JavaScript nudi razne metode za iteraciju nad nizovima. Ove metode omogućuju prolazak kroz svaki element niza i primjenu funkcija na njima.

### Metode Iteracije Nizova

#### Array forEach()

Izvršava funkciju za svaki element niza, bez vraćanja nikakve vrijednosti [0][1][3].

```
const fruits = ["apple", "orange", "cherry"];

fruits.forEach(function(item, index, array) {
  console.log(item, index);
});
// apple  0
// orange  1
// cherry  2
```

#### Array map()

Stvara novi niz s rezultatima funkcije provedenih na svakom elementu niza.

```
const numbers = [1,  2,  3,  4];
const squares = numbers.map(x => x * x);
// squares: [1,  4,  9,  16]
```

#### Array flatMap()

Prvo mapa sve elemente niza, a zatim stvori novi niz tako što spaja elemente.

```
const nestedNumbers = [[1], [2,  3], [4,  5,  6]];
const flattenedNumbers = nestedNumbers.flatMap(x => x);
// flattenedNumbers: [1,  2,  3,  4,  5,  6]
```

#### Array filter()

Stvara novi niz koji sadrži elemente niza koji prolaze test.

```
const numbers = [1,  2,  3,  4,  5];
const evens = numbers.filter(x => x %  2 ===  0);
// evens: [2,  4]
```

#### Array reduce()

Primjenjuje funkciju na svaki element niza da bi stvorio jednu konačnu vrijednost.

```
const numbers = [1,  2,  3,  4];
const sum = numbers.reduce((accumulator, currentValue) => accumulator + currentValue,  0);
// sum:  10
```

#### Array reduceRight()

Radi slično kao `reduce()`, ali počinje s desne strane niza.

```
const numbers = [1,  2,  3,  4];
const sum = numbers.reduceRight((accumulator, currentValue) => accumulator + currentValue,  0);
// sum:  10
```

#### Array every()

Provjerava da li svi elementi niza prolaze test.

```
const numbers = [1,  2,  3,  4];
const allArePositive = numbers.every(x => x >  0);
// allArePositive: true
```

#### Array some()

Provjerava da li barem jedan element niza prolazi test.

```
const numbers = [1,  2,  3,  4];
const hasNegativeNumber = numbers.some(x => x <  0);
// hasNegativeNumber: false
```

#### Array from()

Kreira niz iz iterabilnog objekta.

```
const string = 'hello';
const arrayFromString = Array.from(string);
// arrayFromString: ['h', 'e', 'l', 'l', 'o']
```

#### Array keys()

Vraća `Array Iterator` objekt koji sadrži ključeve originalnog niza.

```
const numbers = [1,  2,  3,  4];
const iterator = numbers.keys();
// iterator: ArrayIterator {}
```

#### Array entries()

Vraća `Array Iterator` objekt koji sadrži parove ključ-vrijednost originalnog niza.

```
const numbers = [1,  2,  3,  4];
const iterator = numbers.entries();
// iterator: ArrayIterator {}
```

#### Array with()

Napravi novi niz s ažuriranim elementima bez mijenjanja originalnog niza.

```
const numbers = [1,  2,  3,  4];
const newNumbers = numbers.with(0,  10);
// newNumbers: [10,  2,  3,  4]
```

#### Array Spread (...)

Operator proširuje iterabilne objekte, poput nizova, u više elemenata.

```
const numbers = [1,  2,  3,  4];
const spreadNumbers = [...numbers,  5];
// spreadNumbers: [1,  2,  3,  4,  5]
```

```

```
