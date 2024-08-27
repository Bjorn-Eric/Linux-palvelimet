# Raportti Debianin Asentamisesta

Tässä raportissa käydään läpi, miten asennetaan debian 12.6.0 virtual box ympäristöön. Tiivistän myös pari opettajan laatimaa artikkelia omin sanoin.


## Raportin kirjoittaminen

- Raportin pitää olla niin selkeä, että sen avulla voidaan saavuttaa sama lopputulos aina. Raportissa pitää siis kertoa tarkkaan missä ympäristössä ollaan tekemässä ja mitä ollaan tarkalleen tekemässä

- Raportoinnissa pitää myös olla mahdollisimman tästmällinen. Raportissa pitää selvitä mahdollisimman yksityiskohtaisesti mitä kirjoittaja on tehnyt, missäkin tilanteessa, esim. mitä nappia on painanut, mitä komentoja on käyttänyt yms. Raportti on myös suositeltavaa aina kirjoittaa imperfekti, eli menneessä aikamuodossa.

- Raportti pitäisi myös olla mahdollisimman selkeä ja helppolukuinen. Kirjoittajan on suotavaa aina tarkistaa kaikki kirjoitusvirheet. Myös hyvä yleinen rakenne ja väliotsikot ovat suositeltuja.


## Mitä on ilmainen ohjelmisto

- Ilmainen ohjelmisto on käytännössä (vie loppuun)

## Ympäristö

- Tietokone: Mac Book Pro 2019 - Ventura 13.4.1 - Intel I9 - 16 GB RAM
- Debian: 12.6.0
- VirtualBox: 7.0.20
<img width="243" alt="Screenshot 2023-10-27 at 22 00 32" src="https://github.com/user-attachments/assets/b96934b3-eb77-43db-9500-400b5c960cdf">


## Askeleet Debianin asentamiseksi

1. Ensiksi kävin lataamassa VirtualBox ohjelmiston koneelleni, osoitteesta: https://www.virtualbox.org/wiki/Downloads.
2. Asensin ohjelmiston koneelleni wizardin avulla.
3. Kävin lataamassa Debian tiedoston osoitteesta: https://www.debian.org ja sieltä valitsemalla "Download".
4. Ladattuani Debian asennus tiedoston, avasin virtual boxin:
<img width="986" alt="Screenshot 2024-08-26 at 23 42 20" src="https://github.com/user-attachments/assets/18a91dd1-d24b-4758-82f0-28897605a6ac">
5. Klikkasin virtual box ohjelmasta painiketta "New".
6. Loin uuden virtuaali koneen:
<img width="980" alt="Screenshot 2024-08-26 at 23 44 41" src="https://github.com/user-attachments/assets/6091f834-b245-4c5e-90f1-8852ca1e7530">
<img width="999" alt="Screenshot 2024-08-26 at 23 45 53" src="https://github.com/user-attachments/assets/77285c23-a597-4d42-a73a-868e5abb86f3">
<img width="1004" alt="Screenshot 2024-08-26 at 23 46 34" src="https://github.com/user-attachments/assets/78d201f9-0098-4a07-8bb5-796c287af03e">
<img width="1003" alt="Screenshot 2024-08-26 at 23 47 10" src="https://github.com/user-attachments/assets/13bebb79-75d5-41a9-beae-504a9f1e714f">
<img width="1073" alt="Screenshot 2024-08-26 at 23 47 23" src="https://github.com/user-attachments/assets/4c7db920-d891-4380-b428-457d5dc6aee4">
7. Käynnistettyäni asennus prosessin, tietokoneen oma käyttöjärjestelmä pyysi minua antamaan lupaa "Accessibility Access" Virtual Box ohjelmistolle.
<img width="580" alt="Screenshot 2024-08-26 at 23 47 57" src="https://github.com/user-attachments/assets/d15c6f08-c93f-4ad9-b88a-3b93f2a202f9">

8. Annoin luvan, jonka jälkeen käyttöjärjestelmä käynnisti Virtual Box ohjelman uudelleen.
9. Tämän jälkeen Debian asennus kesti noin 12 minuuttia.
<img width="1679" alt="Screenshot 2024-08-26 at 23 49 23" src="https://github.com/user-attachments/assets/60c2afd4-7d14-4a02-986e-5d977e264c9c">
10. Virtual Boxin näyttö oli kuitenkin hieman pienin, niin kävin säätämässä sitä Virtual Box "Display" asetuksista:
 <img width="734" alt="Screenshot 2024-08-26 at 23 50 23" src="https://github.com/user-attachments/assets/31e44ede-27a9-4a6f-af49-34d100ee37cf">
11. Asenuksen jälkeen Debian käynnistyi normaalisti ja näytölle ilmeni kirjautumis sivu:
<img width="1678" alt="Screenshot 2024-08-26 at 23 57 12" src="https://github.com/user-attachments/assets/e770b2c7-fbf7-4d78-b717-d01b6b650735">
12. Pystyin käyttämään Debiania normaalisti ilman mitään ongelmia:
<img width="1672" alt="Screenshot 2024-08-26 at 23 58 04" src="https://github.com/user-attachments/assets/2cf23206-3412-4713-8de5-52d79f816a68">
