
# CSS Padding 

CSS svojstvo padding se koristi za generisanje prostora oko sadržaja elemenata, unutar definiranog okvira.

Sa CSS-om, imamo potpunu kontrolu nad paddingom. Postoje svojstva za postavljanje paddinga za svaku stranu elementa (gore, desno, dolje i lijevo). 

# Padding - pojedinačne strane

CSS ima svojstva za određivanje paddinga za svaku stranu elementa:

- padding-top
- padding-right
- padding-bottom
- padding-left
Sva svojstva paddinga mogu imati sljedeće vrijednosti:

- length - određuje padding u px, pt, cm, itd.
- % - specificira padding u % širine elementa koji sadrži
- inherit - specificira da padding treba biti naslijeđen od parent elementa

Tip: Negativne vrijednosti nisu dozvoljene.

![App Screenshot](https://github.com/BHFFMMST/Web-development/blob/main/docs/assets/images/styling/Screenshot_56.png?raw=true)

# Padding i širina elemenata

Svojstvo širine CSS-a specificira širinu područja sadržaja elementa. Područje sadržaja je dio unutar paddinga, ivice i margine elementa (model okvira).

Dakle, ako element ima navedenu širinu, padding dodan tom elementu će se dodati ukupnoj širini elementa. Ovo je često nepoželjan rezultat.

![App Screenshot](https://github.com/BHFFMMST/Web-development/blob/main/docs/assets/images/styling/Screenshot_57.png?raw=true)

Da biste zadržali širinu na 300px, bez obzira na količinu paddinga, možete koristiti svojstvo box-sizing. Ovo omogućava da element zadrži svoju stvarnu širinu; ako povećate padding, dostupni prostor sadržaja će se smanjiti.

![App Screenshot](https://github.com/BHFFMMST/Web-development/blob/main/docs/assets/images/styling/Screenshot_58.png?raw=true)