
# CSS Box Model

Svi HTML elementi se mogu smatrati kao jedan 'box'.

U CSS-u se termin "box model" koristi kada se govori o dizajnu i izgledu.

Model CSS okvira je u suštini kutija koja obavija svaki HTML element. Sastoji se od: sadržaja, paddinga, ivica i margina. Slika ispod ilustruje box model:

![App Screenshot](https://github.com/BHFFMMST/Web-development/blob/main/docs/assets/images/styling/Screenshot_64.png?raw=true)

Objašnjenje različitih dijelova:

- Content - Sadržaj okvira u kojem se pojavljuju tekst i slike
- Padding - Briše područje oko sadržaja. Podloga je prozirna
- Border - Granica koja se kreće oko paddinga i sadržaja
- Margin - Briše područje izvan margine. Margina je transparentna
Box model nam omogućava da dodamo ivicu oko elemenata i da definiramo razmak između elemenata.

![App Screenshot](https://github.com/BHFFMMST/Web-development/blob/main/docs/assets/images/styling/Screenshot_65.png?raw=true)

# Širina i visina elementa
Da biste pravilno postavili širinu i visinu elementa u svim pretraživačima, morate znati kako radi box model.

*Kada postavite svojstva širine i visine elementa pomoću CSS-a, samo postavljate širinu i visinu područja sadržaja. Da biste izračunali ukupnu širinu i visinu elementa, morate uključiti i padding i bordere.

![App Screenshot](https://github.com/BHFFMMST/Web-development/blob/main/docs/assets/images/styling/Screenshot_66.png?raw=true)

Primjer izračunavanja:

Ukupna širina elementa se izračunava na sljedeći način:

Ukupna širina elementa = width + left padding + right padding + left border + right border

Ukupna visina elementa se izračunava na sljedeći način:

Ukupna visina elementa = height + top padding + bottom padding + top border + bottom border

