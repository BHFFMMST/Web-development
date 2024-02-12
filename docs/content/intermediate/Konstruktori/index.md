Metoda **\__init__** je najvažnija metoda u klasi. Ona se poziva kada se kreira instanca(objekt) klase, koristeći ime 
klase kao funkciju.
Metoda **\__init__** je konstruktor.

>Konstruktor je jedinstvena funkcija koja se automatski poziva kada se kreira objekt klase.
 Glavna svrha konstruktora je da inicijalizira ili dodijeli vrijednosti članovima 
 podataka te klase. Ne može vratiti nijednu vrijednost osim ništa.

Tipovi konstruktora:
>- **default konstruktor** - jednostavan konstruktor koji ne prihvata nikakve argumente. Njegova
 definicija ima samo jedan argument koji je referenca na instancu koja se konstruiše.
>- **parametrizovani konstruktor** -
uzima svoj prvi argument kao referencu na instancu koja se konstruiše poznatu kao self,
 a ostale argumente daje programer.

 <pre>
```python
class Macka:
  #default konstruktor  
  def __init__(self):
    self.macka = "Macke su super zivotinje"

    def print_Macka(self):
        print(self.macka)
  
obj = Macka()
obj.print_Macka()

```
</pre>

<pre>
```python
Output: Macke su super zivotinje
```
</pre>

<pre>
```python
class Sabiranje:
    prvi = 0
    drugi = 0
    suma = 0
    def __init__(self, p, d):
        self.prvi = p
        self.drugi = s

    def odgovor(self):
        print("Prvi broj = " + str(self.prvi))
        print("Drugi broj = " + str(self.drugi))
        print("Suma dva broja = " + str(self.suma))
    
    def racun(self):
        self.suma = self.prvi + self.drugi

obj = Sabiranje(5, 3)
obj = racun()
obj = odgovor()
```
</pre>

<pre>
```python
Output: Prvi broj = 5
        Drugi broj = 3
        Suma dva broja = 8
```
</pre>

Sve metode moraju imati **self** kao prvi parametar, iako nije eksplicitno proslijeđen, 
Python dodaje argument self na listu umjesto vas; ne morate ga uključiti kada pozivate
 metode. Unutar definicije metode, self se odnosi na instancu koja poziva metodu.

Prednosti korištenja konstruktora
>-**Inicijalizacija objekata**: Konstruktori se koriste
 za inicijalizaciju objekata klase. Oni vam omogućavaju da
  postavite zadane vrijednosti za atribute ili svojstva, a također 
omogućavaju da inicijalizirate objekt s prilagođenim podacima.

>-**Jednostavan za implementaciju**: Konstruktori se lako implementiraju u Python-u i
 mogu se definirati korištenjem metode __init__()

>-**Bolja čitljivost**: Konstruktori poboljšavaju čitljivost koda tako što jasno stavljaju  
do znanja koje vrijednosti se inicijaliziraju i kako se inicijaliziraju.

>-**Enkapsulacija**: Konstruktori se mogu koristiti za provođenje enkapsulacije, osiguravajući 
da su atributi objekta ispravno inicijalizirani i na kontroliran način.

##Getteri i setteri

Glavna svrha korištenja **gettera i settera** u objektno orijentiranim programima je osigurati 
enkapsulaciju podataka. Privatne varijable u Pythonu zapravo nisu skrivena polja kao u 
drugim objektno orijentisanim jezicima. Getteri i Setteri u pythonu se često koriste kada:
> - Koristimo gettere i settere da bismo dodali logiku validacije oko dobijanja i postavljanja vrednosti
> - Da bi se izbjegao direktan pristup polju klase, tj. privatnim varijablama ne može se pristupiti direktno
 ili modificirati od strane eksternog korisnika.

 <pre>
```python
class Student:
    def __init__(self, ocjena = 0):
         self._ocjena = age
      
    # getter
    def get_ocjena(self):
        return self._ocjena
      
    # setter 
    def set_ocjena(self, x):
        self._ocjena = x
  
mujo = Student()
  

mujo.set_ocjena(8)
  

print(mujo.get_ocjena())
  
print(mujo._ocjena)
```
</pre>

<pre>
```python
Output: 8
        8

```
</pre>
U gore navedene funkcije get_ocjena() i set_ocjena() ponašaju se kao normalne funkcije i 
ne igraju nikakav utjecaj kao getteri i setteri, da bi se postigla takva 
funkcionalnost Python ima posebnu funkciju **property()**.

U Pythonu property() je ugrađena funkcija koja kreira i vraća objekt svojstva. 
Objekt svojstva ima tri metode, getter(), setter() i delete(). property() funkcija
 u Pythonu ima četiri argumenta property(fget, fset, fdel, doc), fget je funkcija za 
 dohvaćanje vrijednosti atributa. fset je funkcija za postavljanje vrijednosti atributa.
 fdel je funkcija za brisanje vrijednosti atributa. doc kreira docstring za atribut.
  Objekat svojstva ima tri metode, getter(), setter() i delete() za navođenje fget, 
  fset i fdel pojedinačno. Na primjer

  <pre>
```python


class Student:
	def __init__(self):
		self._ocjena = 0
	
	
	def get_ocjena(self):
        print("getter metoda je pozvana")
		return self._ocjena
	
	
	def set_ocjena(self, a):
        print("setter metoda je pozvana")
		self._ocjena = a

	
	def del_ocjena(self):
		del self._ocjena
	
	ocjena = property(get_ocjena, set_ocjena, del_ocjena)

haso = Student()

haso.ocjena = 9

print(haso.ocjena)


```
</pre>

<pre>
```python
Output: setter metoda je pozvana
        getter metoda je pozvana
        9
```
</pre>

U prethodnoj metodi koristili smo funkciju property() da bismo postigli ponašanje gettera 
i settera. Međutim, getteri i setteri se također
 koriste za provjeru valjanosti dobivanja i postavljanja vrijednosti atributa. Postoji još 
 jedan način implementacije funkcije svojstva, tj. korištenjem dekoratora. Python @property
  je jedan od ugrađenih dekoratora. Glavna svrha svakog dekoratora je da promijeni metode 
  ili atribute vaše klase na takav način da korisnik vaše klase nema potrebe da pravi bilo
   kakvu promjenu u svom kodu. Na primjer

<pre>
```python
class Student:
	def __init__(self):
		self._ocjena = 0
	
	@property
	def ocjena(self):
		print("getter metoda je pozvana")
		return self._ocjena
	
	
	@age.setter
	def ocjena(self, a):
		if(a < 6):
			raise ValueError("Ocjena nije prolazna")
		print("setter metoda je pozvana")
		self._ocjena = a

suljo = Student()

suljo.ocjena = 7

print(suljo.ocjena)

```
</pre>

<pre>
```python
Output: setter metoda je pozvana
        getter metoda je pozvana
        7
```
</pre>

U gornjem kodu je jasno kako koristiti @property dekorator za kreiranje gettera i 
settera. Red 15-16 djeluje kao kod za provjeru valjanosti koji podiže
 ValueError ako pokušamo inicijalizirati ocjenu sa vrijednošću manjom od 6. Na ovaj način bilo
  koja vrsta provjere valjanosti može se primijeniti u getter ili setter funkcijama.