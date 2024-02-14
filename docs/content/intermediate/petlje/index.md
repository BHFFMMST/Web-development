## Petlje u JavaScriptu

Petlje su korisne kada želite ponovno pokrenuti isti kod, svaki put s drugom vrijednošću. JavaScript nudi različite vrste petlji za rukovanje različitim situacijama.

### Vrste Petlji

#### For Loop

Petlja `for` prolazi kroz blok koda određeni broj puta.

```
for (let i =  0; i <  5; i++) {
  console.log(i);
}
// Output:  0  1  2  3  4
```

#### While Loop

Petlja `while` prolazi kroz blok koda dok je navedena tvrdnja istinita.

```
let i =  0;
while (i <  5) {
  console.log(i);
  i++;
}
// Output:  0  1  2  3  4
```

#### Do While Loop

Petlja `do...while` prvo izvršava blok koda, a zatim provjerava uvjet. Ova petlja će se izvršiti barem jednom jer provjera uvjeta dolazi nakon izvršenja bloka koda.

```
let i =  0;
do {
  console.log(i);
  i++;
} while (i <  5);
// Output:  0  1  2  3  4
```

### Ostale Petlje

#### For/In Loop

Petlja `for...in` prolazi kroz svojstva objekta.

```
let person = {firstName:"John", lastName:"Doe", age:25};
for (let property in person) {
  console.log(property + ": " + person[property]);
}
// Output: firstName: John
//         lastName: Doe
//         age:  25
```

#### For/Of Loop

Petlja `for...of` prolazi kroz vrijednosti iterabilnog objekta, poput polja.

```
let colors = ['red', 'green', 'blue'];
for (let color of colors) {
  console.log(color);
}
// Output: red
//         green
//         blue
```

Petlje su temeljna konstrukcija u programiranju koja omogućuje ponavljanje određene akcije. Različite vrste petlji omogućuju fleksibilno rukovanje različitim scenarijima, od jednostavnog prolaska kroz niz do složenih uvjeta i logike.
