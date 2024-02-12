# Apstraktne klase

Apstrakcija predstavlja proces izdvajanja zajedničkih karakteristika objekata i njihovo predstavljanje u obliku apstraktnih klasa. Apstraktna klasa predstavlja zajedničku nadklasu za sve konkretne klase koje imaju zajedničke karakteristike. Apstraktna klasa ne može imati instance, već se koristi za definisanje zajedničkih atributa i metoda koje će nasljeđivati konkretne klase.


**Primjer:**
Trebamo realizovati klasu `GeometrijskiObjekat` u ravni. Postoje različite vrste geometrijskih objekata, kao što su trougao, kvadrat, krug. Geometrijski objekti imaju metode poput obima i površine koje se definišu na različite načine za različite objekte. Potrebno je obavezati podklase da implementiraju ove metode.

```python
from abc import ABC, abstractmethod

class GeometrijskiObjekat(ABC):
    @abstractmethod
    def obim(self):
        pass
    
    @abstractmethod
    def povrsina(self):
        pass


class Krug(GeometrijskiObjekat):
    def __init__(self, r):
        self.r = r

    def obim(self):
        return 2 * self.r * 3.14

    def povrsina(self):
        return self.r * self.r * 3.14
    
    def __str__(self):
        return "Krug sa poluprečnikom {}".format(self.r)


class Kvadrat(GeometrijskiObjekat):
    def __init__(self, a):
        self.a = a

    def obim(self):
        return 4 * self.a

    def povrsina(self):
        return self.a * self.a

    def __str__(self):
        return "Kvadrat sa stranicom {}".format(self.a)
```

Apstraktne metode se definišu pomoću dekoratora `@abstractmethod`, a da bi se klasa označila kao apstraktna, potrebno je da nasljeđuje klasu `ABC` iz modula `abc` koji se uvozi na početku programa.
