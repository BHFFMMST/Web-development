Funkcije u klasama se nazivaju **metode**.

Metode su funkcije definirane unutar klase koje 
rade na podacima ili atributima klase. 
Postoje uglavnom dvije vrste metoda:
>- metode instance
>- metode klase

##Metode instance
Metode instance su funkcije definirane unutar klase koje
 rade na podacima specifičnim za instancu. One su najčešći tip metoda u Python klasama.

>Da bi definirali metodu instance, morate uključiti **self** parametar kao prvi argument
 u definiciji metode. **self** se odnosi na instancu same klase i omogućava vam pristup i 
 izmjenu podataka specifičnih za instancu.

Metode instance se obično koriste za izvođenje radnji ili operacija koje uključuju atribute 
(podatke) instance. Oni obuhvataju ponašanje povezano s objektom.

<pre>
```python
class Pas:
    def __init__(self, ime, starost):
        self.ime = ime
        self.starost = starost

    def lajanje(self):
        return f"{self.ime} kaže av av!"


pas1 = Pas("Rex", 3)


print(dog1.lajanje()) 
```
</pre>

<pre>
```python
    Output: Rex kaže av av
```
</pre>

##Metode klase

Metode klase su metode koje su vezane za klasu, a ne za instancu.
Definirani su pomoću **@classmethod** dekoratora.

>Metode klase uzimaju samu klasu kao svoj prvi argument, obično nazvan **cls**. 
Ovo omogućava metodama klase da pristupe i modifikuju podatke na nivou klase 
(varijable klase).

Metode klase se često koriste za operacije koje su povezane sa klasom kao cjelinom 
i ne zavise od specifičnih podataka instance. Koriste se i za fabričke metode koje 
kreiraju instance klase.

<pre>
```python
class Knjige:
    broj_knjiga = 0  

    def __init__(self, naslov, autor):
        self.naslov = naslov
        self.autor = autor
        Knjige.broj_knjiga += 1

    @classmethod
    def prikaži_broj_knjiga(cls):
        return f"Broj knjiga je: {cls.broj_knjiga}"


knjiga1 = Knjige("Harry Potter", "J.K.rowling")
knjiga2 = Knjige("Tvrdjava", "Mesa Selimovic")


print(Knjige.prikaži_broj_knjiga())  

```
</pre>

<pre>
```python
    Output: Broj knjiga je: 2
```
</pre>

U Pythonu, ponašanje public i private varijabli u metodama instance i klase je u skladu 
s njihovim pravilima pristupa, koja su sljedeća:

1. Pubic varijabe:

>Javnim varijablama, koje nemaju prefiks, 
može se pristupiti i mijenjati ih direktno unutar metoda instance i metoda klase.

```
</pre>

<pre>
```python
class Klasa:
    def __init__(self):
        self.public_var = "Ja sma public variabla"

    def instance_metoda(self):
        return self.public_var

    @classmethod
    def metoda_klase(cls):
        return cls().public_var


obj = Klasa()

print(obj.instance_metoda())  
print(Klasa.metoda_klase())  

```
</pre>

<pre>
```python
    Output: Ja sam public variabla
            Ja sam public variabla
```
</pre>

2. Private varijable:

>Privatne varijable, koje imaju prefiks dvostruke donje crte (npr. __private_var), 
prolaze kroz mijenjanje imena u Pythonu kako bi bile manje dostupne izvan klase.

>Privatnim varijablama se i dalje može pristupiti i mijenjati ih unutar metoda instance, 
ali morate koristiti iskrivljeno ime.

>Metode klase također mogu pristupiti privatnim varijablama koristeći iskrivljeno ime, 
sve dok imaju pristup instanci klase.

<pre>
```python
class Klasa:
    def __init__(self):
        self.__private_var = "Ja sam privatna variabla"

    def instance_metoda(self):
        return self.__private_var

    @classmethod
    def metoda_klase(cls):
        return cls().__private_var  


obj = Klasa()

print(obj.instance_metoda())  
print(Klasa.metoda_klase()) 
```
</pre>

<pre>
```python
    Output: Ja sam privatna variabla
            Ja sam privatna variabla
```
</pre>

U gornjem primjeru, privatna varijabla __private_var dostupna je i iz metode instance i 
iz metode klase, ali u slučaju metode klase koristimo iskrivljeno ime cls().__private_var 
da joj pristupimo.

Važno je napomenuti da iako možete tehnički pristupiti privatnim varijablama izvan klase 
koristeći iskrivljeno ime, to je protiv principa enkapsulacije i općenito se ne preporučuje. 
Privatne varijable su namijenjene da budu privatne s razlogom, a direktan pristup izvan 
klase treba izbjegavati kad god je to moguće kako bi se održala čista i robusna struktura 
koda. Umjesto toga, trebali biste osigurati javne metode (getter i setter metode) za pristup 
ili modificiranje privatnih podataka kada je to potrebno.

