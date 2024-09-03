# Raportti "Komentaja Pingviini"
Tässä raportissa käydään läpi hieman Linuxin perus komentoja ja erilaisia komentoriville asennettavia ohjelmia.

### Micron asentaminen
1. Ensiksi päivitin apt lähteet komennolla: "sudo apt update"
    <img src="./screenshots/1.png" alt="screenshot">
2. Tämän jälkeen asensin kaikki päivitykset: "sudo apt full-upgrade -y"
    <img src="./screenshots/2.png" alt="screenshot">
3. Tämän jälkeen asensin micro ohjelman komennolla "sudo apt install micro" ja painoin enter
    <img src="./screenshots/3.png" alt="screenshot">
4. Tämän jälkeen perustin testausta varten uuden tiedoston nimeltään "test.txt" ja lisäsin sinne tekstiä
    <img src="./screenshots/4.png" alt="screenshot">
    <img src="./screenshots/5.png" alt="screenshot">
5. Tämän jälkeen törmäsin ongelmaan, koska en osannut sulkea ohjelmaa. Lopulta löysin kuitenkin ratkaisun ohjelmiston "help" osiosta.
    <img src="./screenshots/6.png" alt="screenshot">
6. Help osion sain auki ctrl + g ja siellä on ohjeet miten saa micron komentorivin auki (ctrl + e). Päätin kokeilla komentoriville "quit" komentoa, joka sulki ohjelman.
    <img src="./screenshots/7.png" alt="screenshot">

## Kolmen komentoriviohjelman esittely
Tässä kappaleessa esittelen kolmea yksinkertaista ohjelmaa, jotka löysin "apt search" komennon avulla.

### HTOP
Htop on kehittyneempi versio "top" komennosta. Htop komennon avulla pystyt näkemään kaikki järjestelmän prosessit, niiden taustatiedot ja pystyt myös yleisellä tasolla 
hallitsemaan niitä. Htop komento on hyvä, koska se myös näyttää reaaliajassa paljonko resursseja jokin prosessi käyttää ja paljonko järjestelmällä on kuormitusta.

1. Asensin htop ohjelman komennolla "sudo apt install htop -y"
    <img src="./screenshots/12.png" alt="screenshot">
2. Ohjelma asentui ilman mitään ongelmia.
    <img src="./screenshots/13.png" alt="screenshot">
3. Ohejlmasta löytyy myös parametrit, jolla voit suodattaa prosesseja käyttäjäkohtaisesti tai nimen perusteella.
    <img src="./screenshots/15.png" alt="screenshot">
    <img src="./screenshots/14.png" alt="screenshot">


### SL
Sl on pila ohjelma, joka yrittää matkia ls komentoa. Pila esiinty siinä, kun käyttäjä kirjoittaa vahingossa ls komennon väärin ja ruudulle pamahtaa ohi kulkeva juna, jota ei voi sulkea millään, ei edes ctrl + c yhdistelmällä.

1. Asensin sl ohjelman komennolla "sudo apt install sl -y"
    <img src="./screenshots/11.png" alt="screenshot">
2. Testasin ohjelmaa ja se toimi moitteettomasti.
    <img src="./screenshots/10.png" alt="screenshot">


### duf
Duf on hieman käyttäjäystävällisempi versio komennosta df. Duf on hyvin yksinkertainen työkalu, joka näyttää paljonko muistia on käytössä/vapaana järjestelmässä.

1. Asensin duf ohjelman komennolla "sudo apt install duf -y"
    <img src="./screenshots/16.png" alt="screenshot">
2. Testasin ohjelmaa ajamalla komennon "duf" ja kaikki näytti toimivan.
    <img src="./screenshots/17.png" alt="screenshot">


## FHS.

1. "/" on juuri kansio
2. /home/ on kansio


## Grep komento
Grep on komento, jonka avulla voi suodattaa 

## Pipe esittely
Pipe on komentorivillä käytetty keino, jonka ansiosta voit syöttää jonkin komennon tuloksen toiselle komennolle, eli toisin sanoen ketjuttaa komentoja. Helppo esimerkki tästä on vaikkapa 
 

## Rauta (lshw)
1. Ensiksi asensin ohjelman komennolla "sudo apt install lshw -y"
2. Tämän jälkeen testasin ohjelmaa ajamalla komennon "sudo lshw -short -sanitize"
3. Komento listasi minulle kaikki tiedot fyysisestä laitteesta.

Tulkitsin komentoa