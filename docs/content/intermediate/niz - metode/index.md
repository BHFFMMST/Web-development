## Arrays

Arrays su strukture podataka koje omogućuju pohranjivanje i manipulaciju više vrijednosti u JavaScriptu. Moguće je definirati array koristeći `new Array` konstruktor ili jednostavno sintaksom `[]`.

### Metode Arrays

### Metode Arrays

#### .push()

Dodaje jedan ili više elemenata na kraj arraya i vraća novu dužinu arraya.

```
let fruits = ['apple', 'banana', 'orange'];
fruits.push('grape'); // ['apple', 'banana', 'orange', 'grape']

```

#### .unshift()

Dodaje jedan ili više elemenata na početak arraya i vraća novu dužinu arraya.

```
let fruits = ['apple', 'banana', 'orange'];
fruits.unshift('grape'); // ['grape', 'apple', 'banana', 'orange']
```

#### .pop()

Uklanja posljednji element iz arraya i vraća taj element.

```
let fruits = ['apple', 'banana', 'orange'];
let lastFruit = fruits.pop(); // 'orange'
```

#### .indexOf()

Vraća indeks prvog pojavljivanja određenog elementa u arrayu. Ako element nije pronađen, vraća -1.

```
let fruits = ['apple', 'banana', 'orange'];
let index = fruits.indexOf('banana'); // 1
```

Arrays u JavaScriptu su fleksibilni i moćni alati za rad s podacima. Mogu se koristiti za pohranjivanje različitih tipova podataka i manipulaciju njima putem raznih metoda i operatora.
