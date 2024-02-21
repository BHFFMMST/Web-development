# Stringovi i njihove operacije

## Concatenation (Nizanje stringova)

> Nizanje stringova je proces spajanja dva ili više stringova kako bi se stvorio novi string. U JavaScriptu, to možete postići koristeći operator `+`. Naprimjer:

```js
let firstName = "John";
let lastName = "Doe";
let fullName = firstName + " " + lastName;
console.log(fullName); // Ispisuje "John Doe"
```

## Template literals ``

Template literals su poboljšanje u JavaScriptu koje omogućuje interpolaciju izraza u stringu. Koristite backticks (` `) umjesto navodnika ili apostrofa. Unutar template stringa, možete koristiti `${}` za ubacivanje varijabli ili izraza. Naprimjer:

```js
let name = "Alice";
let greeting = `Hello, ${name}!`;
console.log(greeting); // Ispisuje "Hello, Alice!"
```

## Manipulacija stringovima

### .length, .toUpperCase(), .toLowerCase()

JavaScript nudi razne korisne metode za manipulaciju stringovima. `.length` vraća broj znakova u stringu, `.toUpperCase()` pretvara sve znakove u velika slova, dok `.toLowerCase()` pretvara sve znakove u mala slova. Naprimjer:

```js
let str = "Hello, World!";
console.log(str.length); // Ispisuje duljinu stringa, u ovom slučaju 13
console.log(str.toUpperCase()); // Ispisuje "HELLO, WORLD!"
console.log(str.toLowerCase()); // Ispisuje "hello, world!"
```

### .substring()

`.substring()` metoda se koristi za izdvajanje dijela stringa na temelju indeksa. Prihvaća dva parametra: početni indeks i završni indeks. Naprimjer:

```js
let str = "Hello, World!";
let substr = str.substring(7, 12);
console.log(substr); // Ispisuje "World"
```

### .split(uslov)

`.split()` metoda se koristi za razbijanje stringa na niz podstringova na temelju zadanih uslova. Možete proslijediti separator kao argument, a rezultat će biti niz podstringova. Naprimjer:

```js
let str = "apple,banana,orange";
let fruits = str.split(",");
console.log(fruits); // Ispisuje ["apple", "banana", "orange"]
```

