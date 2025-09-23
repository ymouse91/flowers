# Flowers

**Flowers** on selainpohjainen lautapelisovellus (PWA), jossa yhdistyvät korttipakan hallinta, alueiden rakentaminen ja perhosbonusten optimointi. Peli perustuu alkuperäiseen *Flowers*-lautapeliin, mutta tämä versio on räätälöity sekä **solo-peliksi** että useamman pelaajan kokeiluihin.

Sovellus toimii **iPadilla, iPhonella ja PC:llä** (Safari/Chrome). Sen voi asentaa kotinäyttöön PWA-sovelluksena ja pelata myös offline-tilassa.

---

## Ominaisuudet

- **PWA-tuki**: voidaan asentaa selaimesta (Add to Home Screen / Asenna sovellus).
- **Korttipakan hallinta**: 40 + 40 kortin pakat solo-variantissa.
- **Pisteytys**:
  - Kukka-alueiden koko
  - Perhosbonukset vierekkäisyydestä
  - Miinuspisteet vääränkokoisista alueista
- **Automaattinen laskenta**: ohjelma tunnistaa alueet, laskee pisteet ja bonukset.
- **Visuaaliset merkinnät**:
  - Korttien numerot näkyvät laudan päällä
  - Butterfly-ikonit oikein sijoitettuna
- **Debug-tila** (kehityskäyttöön): näyttää millaisia alueita tunnistetaan ja mitä poistetaan.

---

## Pelin kulku (solo)

1. Pelaajalla on käytössään **40 + 40 kortin pakka**.
2. Kortteja pelataan laudalle **olemassa olevien korttien viereen vaakaan tai pystyy**.
   - Kortteja voi nostaa pimeästä pakasta.
   - Näkyvän pakan korttin nosto aiheutaa seuraavan kortin poistumisen pakasta.
3. Tavoitteena on muodostaa mahdollisimman suuria kukka-alueita. 
4. Pelialueella säilytetään pisteidenlaskua varten pelin lopussa kuitenkin vain ne kortit, joiden numeroarvot muodostavan **täsmälleen** numeroa vastaavan alueen eli esim. 3 kolmosella merkittyä korttia tai 4 nelosella merkittyä korttia. Näin ollen numerolla 1 merkitty kortti ei saa koskea toista numerolla 1 merkittyä korttia.
5. **Perhoset** tuovat yhden lisäpisteen, jos ne asettuvat vierekkäin vastaavan värisen kortin kanssa.
6. Pelin lopussa ohjelma laskee pisteet ja arvioi tuloksen asteikolla (esim. Beginner → Expert).

---

## Asennus ja käyttö

1. Avaa sovellus selaimessa (esim. `https://<käyttäjän-github>.github.io/flowers/`).
2. Lisää kotinäyttöön:
   - iOS: *Jaa* → *Lisää kotinäytölle*
   - Chrome/Edge: *Asenna sovellus*
3. Sovellus toimii tämän jälkeen offline-tilassa.
4. Käynnistä peli ja seuraa ohjeita.

---

## Kehittäjille

- Projekti koostuu seuraavista tiedostoista:
  - `index.html` – käyttöliittymä
  - `app.js` – pelilogiikka ja pisteytys
  - `style.css` – ulkoasu ja asettelu
  - `manifest.json` – PWA-määritykset
  - `service-worker.js` – offline-tuki
- Kuvakkeet löytyvät `icons/`-hakemistosta.
- Kehityksessä käytetty: **HTML5, CSS3, JavaScript (vanilla)**

---

## Tulevat kehityskohteet

- Moninpelin laajennus
- Lisästrategiat perhosbonusten laskentaan
- Graafisten elementtien viimeistely
- Uusia pelivariaatioita (esim. kesävariantti erilliseksi tilaksi)

---

## Lisenssi

Tämä projekti on kehitetty henkilökohtaiseen käyttöön ja pelitestaukseen.  
© 2025 Jouko Riikonen
