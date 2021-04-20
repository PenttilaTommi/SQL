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

ee nyt kysely, jolla saat listattua kaikki Opiskelija-taulussa olevat pääaineet, joissa esiintyy sana "tiede".

Huom! Tee kysely siten, että näet vain uniikit vastaukset. Kyselyn vastauksessa pitäisi olla vain 2 riviä. Kun saat kyselyn toimimaan, kokeile mitä tapahtuu jos muutat 'LIKE'-operaation muotoon 'NOT LIKE'.

näytä taulut
SELECT DISTINCT pääaine FROM Opiskelija WHERE pääaine LIKE '%tiede%'




Suoritetun kyselyn tulos
pääaine
Tietojenkäsittelytiede
Oikeustiede


NOT LIKE kyselyllä tulee vastauksesksipelkkä matematiikka koska sanassa ei esiinny tiedettä.


## 10. Tehtävä: Yhdistelyharjoittelua

Tee nyt kysely, jolla saat listattua kaikki Kurssit ja niihin liittyvät kurssisuoritukset. Valitse näytettäviksi sarakkeiksi vain kurssin nimi ja kurssisuorituksen päivämäärä ja arvosana.

Kyselyn tuloksessa pitäisi olla 4 riviä ja 3 saraketta.


SELECT nimi, päivämäärä, arvosana FROM Kurssi, Kurssisuoritus WHERE Kurssi.kurssitunnus = Kurssisuoritus.kurssi




Suoritetun kyselyn tulos
nimi	päivämäärä	arvosana
Ohjelmoinnin perusteet	2013-08-01	4
Ohjelmoinnin perusteet	2014-08-01	5
Ohjelmoinnin jatkokurssi	2014-08-01	5
Tietokantojen perusteet	2014-10-20	3

## 11. Tehtävä: Haku useasta taulusta
Tee nyt kysely, joka tulostaa jokaisen opiskelijan nimen, kurssisuorituksen päivämäärän, ja kurssisuorituksen arvosanan.

näytä taulut
SELECT nimi, päivämäärä, arvosana FROM Opiskelija, Kurssisuoritus




Suoritetun kyselyn tulos
nimi	päivämäärä	arvosana
Pihla	2014-08-01	5
Pihla	2014-08-01	5
Pihla	2014-10-20	3
Pihla	2013-08-01	4
Joni	2014-08-01	5
Joni	2014-08-01	5
Joni	2014-10-20	3
Joni	2013-08-01	4
Anna	2014-08-01	5
Anna	2014-08-01	5
Anna	2014-10-20	3
Anna	2013-08-01	4
Krista	2014-08-01	5
Krista	2014-08-01	5
Krista	2014-10-20	3
Krista	2013-08-01	4
Matti	2014-08-01	5
Matti	2014-08-01	5
Matti	2014-10-20	3
Matti	2013-08-01	4
Gandhi	2014-08-01	5
Gandhi	2014-08-01	5
Gandhi	2014-10-20	3
Gandhi	2013-08-01	4

## 12. Tehtävä: Tulosten otsikointi
Tee nyt kysely, joka tulostaa jokaiseen kurssiin liittyvän tehtävän. Tulostuksen otsikoiden nimien tulee olla 'kurssi' ja 'tehtävä'.

näytä taulut
SELECT Kurssi.nimi  AS kurssi, Tehtävä.nimi AS tehtävä 
FROM Kurssi, Tehtävä




Suoritetun kyselyn tulos
kurssi	tehtävä
Ohjelmoinnin perusteet	Fotari
Ohjelmoinnin perusteet	Onko tässä rekursio?
Ohjelmoinnin perusteet	Keksi tehtävä
Ohjelmoinnin perusteet	Koetus
Ohjelmoinnin jatkokurssi	Fotari
Ohjelmoinnin jatkokurssi	Onko tässä rekursio?
Ohjelmoinnin jatkokurssi	Keksi tehtävä
Ohjelmoinnin jatkokurssi	Koetus
Tietokantojen perusteet	Fotari
Tietokantojen perusteet	Onko tässä rekursio?
Tietokantojen perusteet	Keksi tehtävä
Tietokantojen perusteet	Koetus

## 13. Tehtävä: Hakujen jäsentely
Tee nyt kysely, joka tulostaa kaikki tehtävät, jotka opiskelija 'Anna' on suorittanut. Tee tulostuksesta sellainen, että yksi sarake sisältää kurssin nimen, ja toinen sarake tehtävän nimen.

näytä taulut

SELECT Tehtävä.nimi AS tehtävä, Kurssi.nimi AS kurssi FROM Tehtävä, Kurssi, Kurssitehtävä, Tehtäväsuoritus, Opiskelija
WHERE Tehtävä.tunnus = Kurssitehtävä.tehtävä
AND Kurssitehtävä.kurssi = Kurssi.kurssitunnus
AND Kurssitehtävä.tunnus = Tehtäväsuoritus.tehtävä
AND Opiskelija.opiskelijanumero = Tehtäväsuoritus.opiskelija
AND Opiskelija.nimi = 'Anna'




Suoritetun kyselyn tulos
tehtävä	kurssi
Fotari	Ohjelmoinnin perusteet
Keksi tehtävä	Tietokantojen perusteet

## 14. tehtävä: pohdintaa taulujen yhdistämisestä

Mä en kyllä täysin ymmärrä kysymystä, koska näissähän haetaan lähtökohtaisesti eri asioita. ensin tehtävää ja sen jälkeen opiskelijoita. Tehtävistä tule kolme tulosta ja opiskelijoista viisi. Ylimääräiset rivit tulee opiskelija taulusta, koska tehtäviä suorittavia opiskelijoita on viisi.

## 15. tehtävä: Alikyselyt
Tee nyt kysely, joka listaa kaikki kurssit, joilla ei ole yhtään tehtävää.

SELECT nimi FROM Kurssi
WHERE kurssi.kurssitunnus
NOT IN (SELECT nimi FROM Tehtävä)




Suoritetun kyselyn tulos
nimi
Ohjelmoinnin perusteet
Ohjelmoinnin jatkokurssi
Tietokantojen perusteet
Tietokantojen perusteet, osa2

## 16. Tehtävä

Tee nyt kysely, jolla lasket kurssisuoritus-taulussa olevat kurssisuoritukset kurssin koodin perusteella. Käytä tulostuksessa sarekkeiden nimiä "kurssikoodi" ja "lukumäärä".

SELECT kurssi AS kurssikoodi, COUNT(*) AS lukumäärä
FROM Kurssisuoritus GROUP BY kurssi



 Oikein meni!


Suoritetun kyselyn tulos
kurssikoodi	lukumäärä
581325	2
581328	1
582103	1


## 17. Tehtävä: Yhteenvetokysely

Tee nyt kysely, jossa lasket kurssisuoritus-taulussa olevien kurssien suoritukset -- taas koodin perusteella. Tällä kertaa tulostuksessa tulee kuitenkn tulostaa kurssikoodin sijaan kurssin nimi. Käytä sarakkeiden niminä "kurssi" ja "lukumäärä". (Huomaa, että edellisessä osassa katsotaan kurssitehtäviä, tässä kurssisuorituksia!)

SELECT Kurssi.nimi  AS kurssi, COUNT(*) AS lukumäärä 
FROM Kurssisuoritus, Kurssi 
WHERE Kurssi.kurssitunnus = Kurssisuoritus.kurssi
GROUP BY kurssi



 Oikein meni!


Suoritetun kyselyn tulos
kurssi	lukumäärä
Ohjelmoinnin perusteet	2
Tietokantojen perusteet	1
Ohjelmoinnin jatkokurssi	1

## 18. Tehtävä: LEFT JOIN

Tee nyt LEFT JOIN -operaatiota käyttäen kysely, jolla listaat kurssikohtaiset suorituslukumäärät siten, että myös ne kurssit, joilla ei ole yhtäkään suoritusta otetaan huomioon. Käytä sarakkeiden niminä nimiä "kurssi" ja "lukumäärä".

SELECT k.nimi AS kurssi, COUNT (ks.kurssi) as lukumäärä FROM kurssi k LEFT JOIN Kurssisuoritus ks 
ON k.kurssitunnus = ks.kurssi GROUP BY k.nimi



 Oikein meni!


Suoritetun kyselyn tulos
kurssi	lukumäärä
Ohjelmoinnin jatkokurssi	1
Ohjelmoinnin perusteet	2
Tietokantojen perusteet	1
Tietokantojen perusteet, osa2	0


## 19. Tehtävä: Taulun luominen
Luo tietokantaan taulu Kurssi, jolla on sarakkeet kurssitunnus, nimi ja kuvaus.

näytä taulut
CREATE TABLE Kurssi(kurssitunnus, nimi, kuvaus)



## 20. Tehtävä: Rivin luominen
Lisää nyt tauluun Kurssi kurssi nimeltä "SQL-kielen perusteet", jonka kurssitunnus on "12345" ja kuvaus "SELECT 'Hei maailma';".

INSERT INTO Kurssi (kurssitunnus, nimi, kuvaus)
    VALUES ('12345', 'SQL-kielen perusteet', "SELECT 'Hei maailma'")




Tarkista vielä, että taulun luominen onnistui, ja että uusi kurssi löytyy tietokantataulusta.

SELECT * FROM Kurssi




Suoritetun kyselyn tulos
kurssitunnus	nimi	kuvaus
12345	SQL-kielen perusteet	SELECT 'Hei maailma'


## 21. Tehtävä: Attribuutteja
Luo ensin tarkasteltava tietokantataulu.

CREATE TABLE Tommintaulu
(
työpaikka varchar(100),
ikä interger(2),
harrastukset varchar(200),
syntymävuosi date(4)
)




Suoritetun kyselyn tulos
Tyhjä vastaus

näytä taulut
Kun tietokantataulu on luotu, saat tarkasteltua sen sisältöä PRAGMA-komennolla.

PRAGMA TABLE_INFO(Tommintaulu)




Suoritetun kyselyn tulos
cid	name	type	notnull	dflt_value	pk
0	työpaikka	varchar(100)	0		0
1	ikä	interger(2)	0		0
2	harrastukset	varchar(200)	0		0
3	syntymävuosi	date(4)	0		0

## 22. TEHTÄVÄ: PRAGMA
Luo taulu Kurssi, jolla on sarakkeet kurssitunnus, nimi ja kuvaus. Kurssitunnuksen tulee olla kokonaisluku, nimen merkkijono, ja kuvauksen merkkijono.

CREATE TABLE Kurssi
(
kurssitunnus integer,
nimi varchar(200),
kuvaus varchar(500)
)




näytä taulut
Varmista vielä PRAGMA-komennolla, että sarakkeiden tyypit ovat halutut.

PRAGMA TABLE_INFO(Kurssi)




Suoritetun kyselyn tulos
cid	name	type	notnull	dflt_value	pk
0	kurssitunnus	integer	0		0
1	nimi	varchar(200)	0		0
2	kuvaus	varchar(500)	0		0


## 23. Tehtävä: Pääavain
Listaa nyt taulussa olevat opiskelijat. Mitä huomaat jos opiskelijoita lisätään tietokantatauluun enemmän?  ### ne saavat järjestysnumeron automaattisesti opiskelijanumeroksi.

SELECT * FROM Opiskelija




Suoritetun kyselyn tulos
opiskelijanumero	nimi	syntymävuosi	pääaine
1	Ada Lovelace		

Koska tietokantatauluun on määritelty avain, joka on uniikki, ei taulun sarakkeessa opiskelijanumero voi olla kahta samaa arvoa. Kokeile tätä painamalla alla olevaa nappia ensin kerran -- jolloin opiskelija lisätään -- ja sitten vielä toisen kerran. Mitä virheviesti kertoo? 

### Kerto että samalla opiskelijanumerolla ei voi lisätä uutta. Eli opiskelijanumeroon jo käytössä.

INSERT INTO Opiskelija (opiskelijanumero, nimi)
    VALUES (999, 'Beezow Doo-Doo Zopittybop-Bop-Bop')


 Virhe:Error: UNIQUE constraint failed: Opiskelija.opiskelijanumero
