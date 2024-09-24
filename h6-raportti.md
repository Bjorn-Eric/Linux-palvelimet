# Harjoitus 6

### a) Omat kotisivut

Näpyttelin paikallisella tietokoneellani kolme hyvin yksinkertaista html sivua, jotka linkitin toisiinsa ja kävin validoimassa https://validator.w3.org/ sivuston avulla: 

1. [index.html (linkki tiedostoon)](./screenshots/h6/html/index.html)
    <img src="./screenshots/h6/screenshots/1.png" alt="screenshot">
    <img src="./screenshots/h6/screenshots/4.png" alt="screenshot">
2.  [page2.html (linkki tiedostoon)](./screenshots/h6/html/index.html)
    <img src="./screenshots/h6/screenshots/2.png" alt="screenshot">
    <img src="./screenshots/h6/screenshots/5.png" alt="screenshot">
3.  [page3.html (linkki tiedostoon)](./screenshots/h6/html/index.html)
    <img src="./screenshots/h6/screenshots/3.png" alt="screenshot"> 
    <img src="./screenshots/h6/screenshots/6.png" alt="screenshot"> 

Tämän jälkeen kopioin sivut paikalliselta koneelta palvelimelle `scp`komentoa käyttäen. Yritin kyseistä komentoa käyttäen siirtää tiedostoja omalle palvelimelle, mutta törmästin seuraavaan ongelmaan:
    <img src="./screenshots/h6/screenshots/8.png" alt="screenshot"> 

Googlailin hetken ja ilmeni, että minulla oli kommentoituna seuraava kenttä ssh konfiguraatio tiedostosta, jonka ansiosta `scp`oli blokattu:
    
<img src="./screenshots/h6/screenshots/9.png" alt="screenshot"> 

Käynnistin tämän asetuksen säätämisen jälkeen palvelimen uudestaan ja kokeilin aikaisempaa `scp`komentoa uusiksi, mutta kävi edelleen sama virhe. Lopulta tajusin, että virhe olikin vain käyttäjässä ja oma domain ei ollut `bjorn-eric.com`, vaan `bjorn-eric.me`. Kokeilin uudestaan oikealla domainilla ja tällä kertaa tiedostojen lataaminen onnistui. Tarkastin vielä palvelimelta, että kyseiset tiedostot olivat tallella.
<img src="./screenshots/h6/screenshots/10.png" alt="screenshot"> 
<img src="./screenshots/h6/screenshots/11.png" alt="screenshot"> 



### b) Nimen konfigurointi

En valitettavasti ymmärtänyt tehtävänantoa. Oliko tarkoitus luoda uusi alidomaini osoittamaan omalle paiaklliselle koneelle vai osoittamaan palvelimelleni?

Hankin oman domainini https://bjorn-eric.com sivustolta https://joker.com. Domainille on konfiguroitu tällä hetkellä kaksi recordia. Yksi A recordi, joka osoittaa palvelimelle ja yksi CNAME recordi, joka uudelleen ohjaa `bjorn-eric.me` osoitteeseen:
<img src="./screenshots/h6/screenshots/7.png" alt="screenshot">

Loin kuiteknin uuden A-recodin ja ohjasin myös siihen uudestaan myös CNAME-recordin:

1. A-record:
    <img src="./screenshots/h6/screenshots/12.png" alt="screenshot">
2. CNAME-record:
    <img src="./screenshots/h6/screenshots/13.png" alt="screenshot">
3. Lopputulos:
    <img src="./screenshots/h6/screenshots/14.png" alt="screenshot">

Testasin vielä, että CNAME osoittaa oikeaseen osoitteeseen https://dnschecker.org sivuston avulla ja kaikki näytti kuin piti: 
    <img src="./screenshots/h6/screenshots/15.png" alt="screenshot">
    <img src="./screenshots/h6/screenshots/16.png" alt="screenshot">
    
    
### c) SSH avainparin luonti ja käyttöönotto

Palvelimeltani löytyi jo tehtävääni tehdessä julkinen ssh avain, mutta päätin tehdä uuden avainparin `ssh-keuygen` komennon avulla.

1. Ensiksi ajoin komennon `ssh-keygen -t rsa -b 4096 -C "testi_avain" -f ~/.ssh/testi_avain`. Kyseine komento luo uuden `rsa` tyyppisen ssh avainparin, joka on `4096`tavua pitkä ja sille annetaan nimeksi `testi_avain` ja se luodaan tiedostoon `testi_avain`. Kun ajaa kyseisen komennon, niin komento pyytää vielä antamaan salasanan, jota käytettäisiin kyseisen avaimen yhtydessä, mutta itse jätin kentät tyhjiksi, joten salasanaa ei määritelty kyseiselle avaimelle:
    <img src="./screenshots/h6/screenshots/18.png" alt="screenshot">
    (Listan lopusta löytyy `testi_avain` ja `testi_avain.pub`)
    <img src="./screenshots/h6/screenshots/17.png" alt="screenshot">

2. Tämän jälkeen siirsin julkisen avaimen (`testi_avain.pub`) palvelimelleni `ssh-copy-id` komentoa käyttäen, joka automaattisesti siirtää avaimen palvelimelle:
    <img src="./screenshots/h6/screenshots/19.png" alt="screenshot">

3. Tämän jälkeen vielä testasi ottaa yhteyttä palvelimelle ssh yhteyden yli uudella avaimella. Kaikki toimi niinkuin pitikin ja sain yhteyden palvelimelle: 
    <img src="./screenshots/h6/screenshots/20.png" alt="screenshot">
    
    
### d)

### Lähteet
https://terokarvinen.com/linux-palvelimet/#h5-nimekas 
https://dnschecker.org/