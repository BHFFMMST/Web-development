## Funkcije u JavaScriptu

Funkcije su blokovi koda dizajnirani za izvršavanje specifičnih zadataka. Funkcije se izvršavaju kada ih neko pozove (poziva).

### Sintaksa Funkcija

Definira se pomoću ključne riječi `function`, nakon čega slijedi naziv funkcije, a zatim zagrada s parametrom `( )`. Parametri se mogu koristiti unutar funkcije kao lokalne varijable.

```
function greeting(name) {
  return "Hello, " + name;
}
```

### Pozivanje Funkcije

Kod unutar funkcije se izvršava kada se funkcija pozove. Pozivanje može biti automatsko, odgovor na događaj (npr. korisnik klikne gumb) ili direktno iz JavaScript koda.

```
greeting("Alice"); // Izvršavanje funkcije i vraćanje rezultata
```

### Povratna Vrijednost

Kada JavaScript dođe do naredbe `return`, funkcija prestaje s izvršavanjem. Vrijednost koju funkcija vraća se naziva povratnom vrijednošću i može se koristiti negdje drugdje u kodu.

```
function add(a, b) {
  return a + b;
}

let sum = add(1,  2); // sum sada ima vrijednost  3
```

### Funkcije Kao Varijable

Funkcije mogu biti korištene na isti način kao i varijable, u svim tipovima formula, dodjeljivanja i izračuna.

### Lokalne Varijable

Varijable deklarirane unutar JavaScript funkcije postaju lokalne za tu funkciju. Lokalne varijable mogu se pristupiti samo unutar te funkcije.

### Konstruktor Funkcija

Funkcije mogu biti definirane i pomoću ugrađenog JavaScript konstruktora funkcija nazvanog `Function()`.

```
let multiply = new Function('a', 'b', 'return a * b');
let product = multiply(4,  5); // product sada ima vrijednost  20
```

### Hoisting Funkcija

Zbog hoistinga (potezanja), JavaScript funkcije mogu biti pozvane prije nego što su deklarirane.

```
result = square(5); // Isprinta  25

function square(number) {
  return number * number;
}
```

### Arrow Funkcije

Arrow funkcije omogućuju kraću sintaksu za pisanje izraza funkcija. Ne morate koristiti ključnu riječ `function`, ključnu riječ `return`, ni zagrade `{}`.

```
const add = (a, b) => a + b;
let sum = add(1,  2); // sum sada ima vrijednost  3
```

### Argumenti i Parametri

Funkcije u JavaScriptu ne provjeravaju vrijednosti parametara. Argumenti su stvarne vrijednosti koje funkcija prima kada je pozvana. Unutar funkcije, argumenti se koriste kao lokalne varijable.

Funkcije su središte modularnog programiranja i omogućuju ponovno korištenje koda, pojednostavljuju održavanje i poboljšavaju čitljivost koda.
