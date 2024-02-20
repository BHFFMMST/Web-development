
# Kako dodati CSS

Kada pretraživač pročita style sheet, on će formatirati HTML dokument u skladu sa informacijama u style sheetu.
##
Tri načina za umetanje CSS-a
##
Postoje tri načina umetanja:

     -Eksterni CSS
     -Interni CSS
     -Inline CSS
##
Eksterni CSS
##
Pomoću eksternog CSS-a možete promijeniti izgled cijele web stranice promjenom samo jedne datoteke!

Svaka HTML stranica mora sadržavati referencu na eksternu datoteku sa style sheetom unutar elementa <link>, unutar odjeljka zaglavlja.

![App Screenshot](https://github.com/BHFFMMST/Web-development/blob/main/docs/content/styling/Screenshot_22.png?raw=true)

Eksterni style sheet se može napisati u bilo kojem uređivaču teksta i mora biti sačuvan sa ekstenzijom .css.

Eksterna .css datoteka ne bi trebala sadržavati nikakve HTML oznake.

Evo kako izgleda datoteka "mystyle.css":

![App Screenshot](https://github.com/BHFFMMST/Web-development/blob/main/docs/content/styling/Screenshot_23.png?raw=true)
##
Interni CSS
##
Interni style sheet može se koristiti ako jedna HTML stranica ima jedinstven stil.

Interni stil je definiran unutar <style> elementa, unutar odjeljka 'head'.

![App Screenshot](https://github.com/BHFFMMST/Web-development/blob/main/docs/content/styling/Screenshot_24.png?raw=true)
##
Inline CSS
##
Inline stil može se koristiti za primjenu jedinstvenog stila za jedan element.

Da biste koristili inline stilove, dodajte atribut 'style' na odgovarajući element. Atribut 'style' može sadržavati bilo koje CSS osobine.

![App Screenshot](https://github.com/BHFFMMST/Web-development/blob/main/docs/content/styling/Screenshot_25.png?raw=true)

