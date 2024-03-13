
# CSS selektori

CSS selektor vrši odabir HTML elemenata koje želite stilizirati.

CSS selektori se koriste za "pronalaženje" (ili odabir) HTML elemenata koje želite stilizirati.

CSS selektore možemo podijeliti u pet kategorija:

    - Jednostavni selektori (odaberete elemente na osnovu imena, ID-a, klase)
    - Selektori kombinatora (odaberete elemente na osnovu specifičnog odnosa između njih)
    - Selektori pseudoklasa (odabir elemenata na osnovu određenog stanja)
    - Selektori pseudoelemenata (odaberete i stilizirate dio elementa)
    - Selektori atributa (odaberete elemente na osnovu atributa ili vrijednosti atributa)

Selektor elemenata bira HTML elemente na osnovu naziva elementa.

![App Screenshot](https://github.com/BHFFMMST/Web-development/blob/main/docs/assets/images/styling/Screenshot_13.png?raw=true)
##
CSS id selektor
##

Selektor id koristi atribut id HTML elementa za odabir određenog elementa.

ID elementa je jedinstven unutar stranice, tako da se id selektor koristi za odabir jednog jedinstvenog elementa.

Da biste odabrali element sa određenim ID-om, upišite znak hash (#), nakon čega slijedi id elemenat.

![App Screenshot](https://github.com/BHFFMMST/Web-development/blob/main/docs/assets/images/styling/Screenshot_14.png?raw=true)

##
CSS class selektor
##

Selektor klase bira HTML elemente sa specifičnim atributom klase.

Da biste odabrali elemente sa određenom klasom, napišete znak tačke (.), nakon čega slijedi naziv klase.

![App Screenshot](https://github.com/BHFFMMST/Web-development/blob/main/docs/assets/images/styling/Screenshot_15.png?raw=true)

Također možete odrediti da klasa treba da utiče samo na određene HTML elemente.

![App Screenshot](https://github.com/BHFFMMST/Web-development/blob/main/docs/assets/images/styling/Screenshot_16.png?raw=true)

HTML elementi se također mogu odnositi na više od jedne klase.

![App Screenshot](https://github.com/BHFFMMST/Web-development/blob/main/docs/assets/images/styling/Screenshot_17.png?raw=true)
##

CSS univerzalni selektor

##
Univerzalni selektor (*) odabire sve HTML elemente na stranici.

![App Screenshot](https://github.com/BHFFMMST/Web-development/blob/main/docs/assets/images/styling/Screenshot_18.png?raw=true)
##
CSS grupisanje selektora
##
Selektor grupisanja bira sve HTML elemente sa istim definicijama stila.

Pogledajte sljedeći CSS kod (elementi h1, h2 i p imaju iste definicije stila):
![App Screenshot](https://github.com/BHFFMMST/Web-development/blob/main/docs/assets/images/styling/Screenshot_19.png?raw=true)

Da bi se kod minimizirao, grupisanje je odlična opcija.

Da biste grupisali selektore, odvojite svaki selektor zarezom.

![App Screenshot](https://github.com/BHFFMMST/Web-development/blob/main/docs/assets/images/styling/Screenshot_20.png?raw=true)
##
SUMIRANJE:
##
![App Screenshot](https://github.com/BHFFMMST/Web-development/blob/main/docs/assets/images/styling/Screenshot_21.png?raw=true)