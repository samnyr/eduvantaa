#### Tehtävä 4
: SELECT * FROM Kurssisuoritus
#### Tehtävä 5
: SELECT kurssi FROM Kurssisuoritus
#### Tehtävä 6
: SELECT DISTINCT kurssi FROM Kurssisuoritus
#### Tehtävä 7
: SELECT * FROM Opiskelija WHERE nimi =  'Anna'
#### Tehtävä 8
: SELECT * FROM Kurssisuoritus WHERE opiskelija = '999999'
#### Tehtävä 9
: SELECT DISTINCT pääaine FROM Opiskelija WHERE pääaine LIKE '%tiede%'
#### Tehtävä 10
: SELECT nimi, päivämäärä, arvosana FROM Kurssisuoritus,  Kurssi WHERE Kurssisuoritus.kurssi = Kurssi.kurssitunnus
#### Tehtävä 11
: SELECT nimi, päivämäärä, arvosana FROM Opiskelija, Kurssisuoritus
#### Tehtävä 12:
SELECT Kurssi.nimi AS kurssi,  Tehtävä.nimi AS tehtävä FROM Kurssi, Tehtävä, Kurssitehtävä WHERE Kurssi.Kurssitunnus = Kurssitehtävä.kurssi AND Kurssitehtävä.tehtävä = Tehtävä.tunnus
#### Tehtävä 13:
SELECT Kurssi.nimi AS kurssi, Tehtävä.nimi AS tehtävä
 FROM Opiskelija, tehtävä, kurssi, Kurssitehtävä, Tehtäväsuoritus
WHERE Kurssi.kurssitunnus = Kurssitehtävä.kurssi
AND Tehtäväsuoritus.tehtävä = Kurssitehtävä.tunnus
AND Tehtäväsuoritus.opiskelija = Opiskelija.opiskelijanumero
AND Kurssitehtävä.tehtävä = Tehtävä.tunnus
AND Opiskelija.nimi = 'Anna'
#### Tehtävä 14: 
Koska ensimmäisessä etsitään kolmesta kohteesta ja toisessa viidestä.

#### Tehtävä 15:
SELECT nimi FROM Kurssi k
WHERE k.kurssitunnus
NOT IN (SELECT kurssi FROM kurssitehtävä)

SELECT nimi FROM Kurssi k
LEFT JOIN Kurssitehtävä t
ON k.kurssitunnus=t.kurssi
WHERE t.tunnus IS NULL




