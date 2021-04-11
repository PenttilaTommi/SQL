## 1. tehtävä: Tutustu tietokantaan

Mitenhän tämän kiiluisi toimia? Hakemalla niin, että täytän ainoastaan etunimi sarakkeen tulee tulokseksi kolme Tommia kolmesta eri kunnasta 1900 luvun vaihten tienoilla. vaikuttaa epäuskottavalta. Toisaalta hakemalla Mattia tuloksia tulee satoja, mutta aakostetut kunnat loppuvat J kirjaimeen.  Maijalla muuten samoin mutta siellä on myös K kirjaimella alkavat kunnat.

## 2. Tehtävä: Käyttämäsi tietokannat

Olen antanut sähköpostini varmasti kymmeniin palveluihin. Melko usein vasten tahtoani mutta nykyään se on edellytyksenä useissa palveluissa. Tämän takia olen aikoja sitten luonut "AlterEgo" sähköpostiosoitteen jota käytän jos on pakko antaa osoite johonkin vähemmän viralliisn palveluihin tai palveluihin jotka oletettavasti alkavat suorastaan spämmäämään sähköpostilla. NÄissä voi myös käyttää tekaistuja nimiä tai olemattomia puhelinnumeroita.

## 3. Tehtävä: Piirrä kaavio
![Piirros](IMG_20210408_183343.jpg.)

## 4. Tehtävä: Hae kaikki
Tee nyt kysely, jolla saat listattua kaikki Kurssisuoritus-taulussa olevat rivit.

näytä taulut
select * from Kurssisuoritus



 Oikein meni!


Suoritetun kyselyn tulos
opiskelija	kurssi	päivämäärä	arvosana
999999	Ohjelmoinnin perusteet	2014-08-01	5
999999	Ohjelmoinnin jatkokurssi	2014-08-01	5
999999	Tietokantojen perusteet	2014-10-20	3
999998	Ohjelmoinnin perusteet	2013-08-01	4

## 5. Tehtävä: Hae kurssien nimet
Tee nyt kysely, jolla saat listattua Kurssisuoritus-taulussa olevien kurssien nimet.

näytä taulut
select kurssi from kurssisuoritus



 Oikein meni!


Suoritetun kyselyn tulos
kurssi
Ohjelmoinnin perusteet
Ohjelmoinnin jatkokurssi
Tietokantojen perusteet
Ohjelmoinnin perusteet

## 6. Tehtävä: Uniikit rivit
Tee nyt kysely, jolla saat listattua Kurssisuoritus-taulussa olevat uniikit kurssit.

näytä taulut
select DISTINCT kurssi from kurssisuoritus



 Oikein meni!


Suoritetun kyselyn tulos
kurssi
Ohjelmoinnin perusteet
Ohjelmoinnin jatkokurssi
Tietokantojen perusteet

## 7. Tehtävä: Hae nimellä
Tee nyt kysely, jolla saat listattua Opiskelija-taulusta kaikki ne opiskelijat, joiden nimi on 'Anna'.

näytä taulut
select * from opiskelija where nimi ='anna'



 Oikein meni!


Suoritetun kyselyn tulos
Tyhjä vastaus

## 8. Tehtävä: Hae ehdolla

8. Tehtävä: Hae ehdolla
Tee nyt kysely, jolla saat listattua Kurssisuoritus-taulusta kaikki Pihla-nimisen opiskelijan suoritukset. Voit olettaa, että Opiskelija-taulun sisältö on täsmälleen se, kuin mikä se tähän asti on ollut. Vinkki: millä Pihlan tunnistaa kummassakin taulussa?

näytä taulut
select * from kurssisuoritus where opiskelija = 999999



 Oikein meni!


Suoritetun kyselyn tulos
opiskelija	kurssi	päivämäärä	arvosana
999999	Ohjelmoinnin perusteet	2014-08-01	5
999999	Ohjelmoinnin jatkokurssi	2014-08-01	5
999999	Tietokantojen perusteet	2014-10-20	3

## 9. Tehtävä: LIKE

### Oletin että DISTNCT poisteisi turhat rivit mutta ei enkä keksi miten ne häipyy???

Tee nyt kysely, jolla saat listattua kaikki Opiskelija-taulussa olevat pääaineet, joissa esiintyy sana "tiede".

Huom! Tee kysely siten, että näet vain uniikit vastaukset. Kyselyn vastauksessa pitäisi olla vain 2 riviä. Kun saat kyselyn toimimaan, kokeile mitä tapahtuu jos muutat 'LIKE'-operaation muotoon 'NOT LIKE'.

piilota taulut
Taulut
Opiskelija (opiskelijanumero integer, nimi text, syntymävuosi integer, pääaine text)
Kurssisuoritus (opiskelija integer, kurssi text, päivämäärä date, arvosana integer)
SELECT DISTINCT * FROM Opiskelija WHERE pääaine LIKE '%tiede%'




Suoritetun kyselyn tulos
opiskelijanumero	nimi	syntymävuosi	pääaine
999999	Pihla	1997	Tietojenkäsittelytiede
999998	Joni	1993	Tietojenkäsittelytiede
999996	Krista	1990	Tietojenkäsittelytiede
999994	Gandhi	1869	Oikeustiede

'NOT LIKE' kyselyllä ilmestyy pelkät matematiikat.


SELECT DISTINCT * FROM Opiskelija WHERE pääaine NOT LIKE '%tiede%'




Suoritetun kyselyn tulos
opiskelijanumero	nimi	syntymävuosi	pääaine
999997	Anna	1991	Matematiikka
999995	Matti	1970	Matematiikka

## 10. Tehtävä: Yhdistelyharjoittelua

### Miksi pitäisi olla 4 riviä?? 
Tee nyt kysely, jolla saat listattua kaikki Kurssit ja niihin liittyvät kurssisuoritukset. Valitse näytettäviksi sarakkeiksi vain kurssin nimi ja kurssisuorituksen päivämäärä ja arvosana.

Kyselyn tuloksessa pitäisi olla 4 riviä ja 3 saraketta.

näytä taulut
SELECT DISTINCT nimi, päivämäärä, arvosana FROM kurssi, kurssisuoritus




Suoritetun kyselyn tulos
nimi	päivämäärä	arvosana
Ohjelmoinnin perusteet	2014-08-01	5
Ohjelmoinnin perusteet	2014-10-20	3
Ohjelmoinnin perusteet	2013-08-01	4
Ohjelmoinnin jatkokurssi	2014-08-01	5
Ohjelmoinnin jatkokurssi	2014-10-20	3
Ohjelmoinnin jatkokurssi	2013-08-01	4
Tietokantojen perusteet	2014-08-01	5
Tietokantojen perusteet	2014-10-20	3
Tietokantojen perusteet	2013-08-01	4
