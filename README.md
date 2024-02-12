# Dokumentacija za Web development kurseve

### Uputstvo za lokalno pokretanje dokumentacije
1. Klonirati repozitorijum
```bash
git clone https://github.com/BHFFMMST/web-development.git
```

2. Pozicionirati se u direktorijum `web-development`
```bash
cd Web-development
```

3. Kreirati virtualno okruzenje i aktivirati ga
```bash
python -m venv env-docs

source env-docs/Scripts/activate
```

4. Instalirati potrebne pakete
```bash
pip install -r requirements.txt
```

5. Pokrenuti dokumentaciju
```bash
mkdocs serve
```

Dokumentacija se pokrece na adresi [localhost:8000](localhost:8000)