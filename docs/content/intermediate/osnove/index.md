# Osnove programiranja u JavaScriptu

## Kreiranje našeg prvog programa

Kreiranje prvog JavaScript programa je jednostavan korak koji vam omogućuje upoznavanje s osnovnim sintaksama jezika. Možete otvoriti svoj omiljeni tekstualni uređivač i stvoriti novu datoteku s `.js` ekstenzijom. Na primjer, stvorite datoteku `hello.js`. Zatim unesite osnovni JavaScript kod unutar te datoteke, kao što je `console.log("Hello, world!");`. Spremite datoteku i izvršite je koristeći Node.js. To će ispisati "Hello, world!" u vašem terminalu ili konzoli.

```js
// hello.js
console.log("Hello, world!");
```

## Varijable

> Varijable su temeljna građevna blokova svakog programske jezika.

### Kreiranje varijabli (let i const)

Deklariranje varijabli je ključni koncept u programiranju, a u JavaScriptu imamo nekoliko načina kako to možemo učiniti. Korištenje `let` i `const` ključnih riječi omogućuje nam deklariranje varijabli s različitim svojstvima. `let` se koristi za deklariranje promjenjivih vrijednosti, što znači da vrijednost varijable može kasnije biti promijenjena. S druge strane, `const` se koristi za deklariranje konstanti, što znači da se vrijednost varijable ne može mijenjati nakon inicijalne dodjele. Primjerice, `let x = 5;` stvara promjenjivu varijablu x, dok `const y = 10;` stvara konstantu `y`. Korištenje odgovarajuće deklaracije varijabli važno je za pravilno upravljanje podacima i očuvanje konzistentnosti u našem programu.

```js
let x = 5;
const y = 10;

x = 7; // Ovo je dozvoljeno jer je x deklariran s let
y = 12; // Ovo će rezultirati greškom jer se pokušava promijeniti vrijednost konstante y
```

### Tipovi varijabli

U JavaScriptu, varijable mogu sadržavati različite tipove podataka, uključujući stringove, brojeve, boolean vrijednosti, nizove, objekte, funkcije, null i undefined. JavaScript je dinamički tipizirani jezik, što znači da tip varijable nije fiksiran i može se automatski mijenjati tijekom izvođenja programa. Na primjer, varijabla koja je inicijalno deklarirana kao string može kasnije postati broj. Ova fleksibilnost omogućava programerima da brzo reagiraju na promjene i dinamički manipuliraju podacima. Razumijevanje različitih tipova varijabli ključno je za uspješno rukovanje podacima u JavaScriptu i sprječavanje grešaka tijekom izvršenja programa.

```js
let name = "John";
let age = 30;
let isMale = true;
let hobbies = ["reading", "swimming", "cooking"];
let person = { name: "Alice", age: 25 };

console.log(typeof name); // string
console.log(typeof age); // number
console.log(typeof isMale); // boolean
console.log(typeof hobbies); // object (niz se smatra objektom)
console.log(typeof person); // object
```

## Da li je JavaScript strongly ili weakly type jezik?

Pitanje o tome je li JavaScript strongly ili weakly type jezik često izaziva rasprave i nejasnoće. Razumijevanje ove karakteristike je bitno za pravilno korištenje jezika. JavaScript se općenito smatra weakly typed jezikom zbog svoje fleksibilnosti u automatskom pretvaranju tipova podataka tijekom izvršavanja programa. To znači da JavaScript dopušta operacije među različitim tipovima podataka bez eksplicitne konverzije. Na primjer, možemo dodavati brojeve i stringove bez posebne konverzije tipova. Ova fleksibilnost može biti korisna, ali istovremeno može dovesti do neočekivanih rezultata ako se ne upravlja pažljivo.

S druge strane, JavaScript također pokazuje neke karakteristike strongly typed jezika. Na primjer, kada koristimo strogu usporedbu operatorom `===`, JavaScript provjerava i tipove i vrijednosti varijabli. Ako tipovi nisu isti, usporedba će biti false. To pokazuje da JavaScript može imati i aspekte strongly typed jezika, gdje su tipovi varijabli važni prilikom provođenja operacija.

Razumijevanje ove dvojnosti je ključno za efikasno programiranje u JavaScriptu. Programerima omogućuje da iskoriste fleksibilnost jezika, ali istovremeno ih upozorava na potencijalne zamke prilikom manipulacije podacima i provođenja operacija. Kao rezultat toga, programeri bi trebali biti svjesni i razumjeti kako JavaScript tretira tipove podataka kako bi izbjegli greške i neželjene rezultate.
