## Objekti u JavaScriptu

Objekti u JavaScriptu su strukture koje omogućuju grupiranje podataka u parove ključ-vrijednost. Ključevi su nizovi, a vrijednosti mogu biti bilo koja vrsta podataka, uključujući funkcije, koje se često nazivaju metodama objekta.

### Definicija Objekta

Objekti se definiraju kao skupovi parova ključ-vrijednost unutar zagradi `{ }`.

```
const car = {
  make: "Toyota",
  model: "Corolla",
  year:  2005,
  color: "blue",
  displayCar: function() {
    return this.make + " " + this.model;
  }
};
```

### Pristupanje Svojstvima Objekta

Svojstvima objekta pristupa se koristeći notaciju tačka ili notaciju kvadratnih zagradi.

```
console.log(car.make); // Ispisuje "Toyota"
console.log(car['year']); // Ispisuje  2005
```

### Metode Objekta

Metode objekta su funkcije koje su svojstva objekta. Metode se mogu pozvati koristeći notaciju tačka ili notaciju kvadratnih zagradi.

```
console.log(car.displayCar()); // Ispisuje "Toyota Corolla"
```

### Pridruživanje Svojstava Objektima

Svojstva se mogu dodati objektima nakon njihovog stvaranja.

```
car.speed = "fast";
console.log(car.speed); // Ispisuje "fast"
```

### Iteriranje Preko Svojstava Objekta

Petlja `for...in` se može koristiti za iteraciju preko svih svojstava objekta.

```
for (let key in car) {
  console.log(key + ": " + car[key]);
}
```

### Prototip Objekta

Svi objekti nasljeđuju svojstva od prototipa. Promjena prototipa objekta utječe na sve objekte koji nasljeđuju od tog prototipa.

```
function Car(make, model, year) {
  this.make = make;
  this.model = model;
  this.year = year;
}

const myCar = new Car("Ford", "Mustang",  1969);
console.log(myCar.make); // Ispisuje "Ford"
```

### Objekti i Povratne Vrijednosti

Objekti su mutable, što znači da se mogu mijenjati nakon što su stvoreni. Kada se objekt proslijedi funkciji, proslijeduje se referenca na objekt, a ne kopija objekta.

### Ključne Riječi `this`

Unutar metoda objekta, ključna riječ `this` se odnosi na objekt na kojem se metoda poziva.

Objekti su ključni dio JavaScripta i omogućuju strukturiranje podataka na složenije načine od jednostavnih nizova i brojeva.
