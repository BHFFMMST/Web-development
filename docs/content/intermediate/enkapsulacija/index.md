# Enkapsulacija

Enkapsulacija je proces sakrivanja podataka i metoda unutar objekta kako bi se sprijčilo njihovo nekontrolisano korišćenje. Enkapsulacijom se može postići bolja raspodjela funkcionalnosti među klasama. Svaka klasa raspolaže samo podacima koji su joj prirodno dodijeljeni što onemogućava miješanje objekata jedne klase u funkcionalnosti objekata druge klase.

**Primjer:** 
Neka su date klase `Krug` i `Crtez`‚ pri čemu se na crtežu nacrtana dva kruga, prirodno je da `Krug` sadrži podatke koji ga opisuju (koordinate centra i poluprečnik), a neka `Crtez` sadrži, kao atribute,  dva kruga. 

Objekat klase `Crtez` ne treba da ima direktan pristup podacima koji opisuju krug, već je potrebno da im pristupa ili manipuliše njima isključivo pozivanjem metoda nad objektima klase `Krug`, poput metode `transliraj` kojom se krug pomjera za dati vektor pomjeraja.   

```python
class Krug:
    def __init__(self, cx, cy, r):
        self.cx = cx
        self.cy = cy
        self.r = r

    def transliraj(self, dx, dy):
        self.cx += dx
        self.cy += dy

    def __str__(self):
        return "Krug sa centrom u tački ({},{}) i poluprečnikom {}".format(self.cx, self.cy, self.r)

class Crtez:
    def __init__(self, krug1, krug2):
        self.krug1 = krug1
        self.krug2 = krug2

    def transliraj_sve(self, dx, dy):
        self.krug1.transliraj(dx, dy)
        self.krug2.transliraj(dx, dy)

    def prikazi(self):
        print(self.krug1)
        print(self.krug2)
```

Enkapsulacija nam sugeriše da se program (tj. problem) i njegovo stanje mogu podijeliti na manje dijelove ali da ujedno ti dijelovi budu dovoljno nezavisni, te da se mogu ponovo upotrebljavati, o ovome treba voditi računa prilikom pisanja programa.
