# Nasljeđivanje

Nasljeđivanje je jedan od najvažnijih koncepata u objektno orijentiranom programiranju. To je proces u kojem jedna klasa preuzima atribute i metode druge klase. Nova klasa se naziva *podklasa* ili *dijete klasa*, a klasa koja je naslijeđena se naziva *nadklasa* ili *bazna (osnovna) klasa*. Podklasa nasljeđuje sve metode i atribute od nadklase, ali isto tako ima mogućnost da definiše nove atribute i metode ili da predefiniše postojeće.

Zašto je ovo korisno?
Zato jer nam omogućava da kreiramo nove klase koje su bazirane na postojećim klasama. Na taj način možemo iskoristiti atribute i metode postojeće klase bez da ih moramo ponovo pisati. Ovo nam omogućava da brže i lakše kreiramo nove klase koje imaju slične atribute i metode kao postojeće klase.


**Primjer 1:**

```python
class Zivotinja:
    def __init__(self, ime):
        self.ime = ime

    def oglasavanje(self):
        pass

class Pas(Zivotinja):
    def __init__(self, ime):
        super().__init__(ime)

    def oglasavanje(self):
        return "vau vau"
    
class Macka(Zivotinja):
    def __init__(self, ime):
        super().__init__(ime)

    def oglasavanje(self):
        return "mijau mijau"
```

U ovom primjeru, klasa `Zivotinja` je nadklasa koja sadrži konstruktor i metodu `oglasavanje`. Klase `Pas` i `Macka` su podklase koje nasljeđuju konstruktor i metodu `oglasavanje` od klase `Zivotinja`. Svaka podklasa ima svoj konstruktor koji poziva konstruktor nadklase i prosljeđuje mu ime životinje. Metoda `oglasavanje` je predefinirana u svakoj podklasi na odgovarajući način.

Kada se pozove metoda `oglasavanje` za objekt tipa `Pas`, Python će prvo tražiti metodu `oglasavanje` u klasi `Pas`. Ako je ne pronađe, tražit će je u klasi `Zivotinja` (nadklasa). Ako je ne pronađe ni tamo, tražiće je u svim ostalim nadklasama. Ako je ne pronađe nigdje, Python će vratiti grešku. 

Funkcija `super()` je specijalna funkcija koja nam omogućava pozivanje metoda nadklase. U primjeru iznad, funkcija `super()` se koristi u konstruktoru podklase kako bi se pozvao konstruktor nadklase.

Važno je napomenuti da nadklasa mora biti definirana prije podklase.

## Polimorfizam

Polimorfizam je sposobnost objekta da se ponaša na više načina. Naziv polimorfizam dolazi od grčkih riječi *poly* (mnogo) i *morphe* (oblik). 

U prethodnom primjeru smo vidjeli da klase `Pas` i `Macka` nasljeđuju klasu `Zivotinja` i implementiraju metodu `oglasavanje`. Obje metode imaju isti naziv, ali se razlikuju po tome što vraćaju različite vrijednosti. Ovo je primjer polimorfizma - koristili smo isto ime metode ali različite implementacije.

**Napomena:** Polimorfizam postoji i bez OOP-a.

```python
def sabiranje(a, b):
    return a + b

print(sabiranje(2, 3))

print(sabiranje("2", "3"))
```

Ova funkcija ima isto ime, ali se ponaša na različite načine u zavisnosti od tipova argumenata. Ovo je takođe primjer polimorfizma.


**Primjer 2:**

```python
class Automobil:
    def __init__(self, marka, model, godina):
        self.marka = marka
        self.model = model
        self.godina = godina
        self.kilometraza = 0

    def opis(self):
        opis = f"{self.marka} {self.model} {self.godina}"
        return opis.title()
    
    def get_kilometraza(self):
        return self.kilometraza
    
    def set_kilometraza(self, kilometraza):
        if kilometraza >= self.kilometraza:
            self.kilometraza = kilometraza
        else:
            print("Ne možete smanjiti kilometražu automobila.")
    
class Baterija:
    def __init__(self, kapacitet_baterije=40):
        self.kapacitet_baterije = kapacitet_baterije
    
    def opis_baterije(self):
        return f"Ovaj automobil ima bateriju kapaciteta {self.kapacitet_baterije}kWh."
    
    def get_domet(self):
        if self.kapacitet_baterije == 40:
            domet = 270
        elif self.kapacitet_baterije == 60:
            domet = 380
        elif self.kapacitet_baterije == 135:
            domet = 510
        
        print(f"Domet je {domet} kilometara.")

class ElektricniAutomobil(Automobil):
    def __init__(self, marka, model, godina, kapacitet_baterije=40):
        super().__init__(marka, model, godina)
        self.baterija = Baterija(kapacitet_baterije)
    
    def opis(self):
        opis = f"{self.marka} {self.model} {self.godina}"
        return opis.title()
    
    def get_bat_kapacitet(self):
        return self.baterija.opis_baterije()
    
    def get_domet(self):
        return self.baterija.get_domet()


tesla_m3 = ElektricniAutomobil("Tesla", "Model 3", 2022, 60)
print(tesla_m3.opis())
print(tesla_m3.get_bat_kapacitet())
tesla_m3.get_domet()

rivian_1s = ElektricniAutomobil("Rivian", "R1S", 2023, 135)
print(rivian_1s.opis())
print(rivian_1s.get_bat_kapacitet())
rivian_1s.get_domet()
```

U ovom primjeru smo modelovali električni automobil. Klasu `ElektricniAutomobil` smo definisali kao podklasu klase `Automobil`, a definisali smo i pomoćnu klasu `Baterija` koja predstavlja atribut klase `ElektricniAutomobil`. 
