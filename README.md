#  IoT Kasvin seurantajärjestelmä (Arduino MKR WiFi 1010)

Tämä projekti on **Arduino-pohjainen IoT-järjestelmä**, joka mittaa kasvin **maan kosteutta** ja **valon määrää** ja lähettää mittaustiedot palvelimelle WiFi-yhteyden kautta JSON-muodossa. Palvelin palauttaa vastauksena kasteluun liittyvää ohjaustietoa, jota voidaan hyödyntää jatkokehityksessä (esim. automaattinen kastelu).

Projekti on suunniteltu erityisesti **Arduino MKR WiFi 1010** -alustalle ja hyödyntää **MKR IoT Carrier** -lisäosaa.

---

## 🚀 Ominaisuudet

-  WiFi-yhteys (WiFiNINA)
-  Maankosteuden mittaus (analoginen anturi)
-  Valon määrän mittaus
-  Mittaustietojen lähetys palvelimelle JSON-muodossa
-  HTTP Basic Authentication (Base64)
-  Säännöllinen tiedonsiirto (30 sekunnin välein)
-  Palvelimen JSON-vastauksen käsittely

---

##  Käytetyt teknologiat ja kirjastot

- Arduino MKR WiFi 1010
- MKR IoT Carrier
- C++ (Arduino)
- WiFiNINA
- ArduinoHttpClient
- ArduinoJson
- Base64

---

##  Järjestelmän toiminta

1. Laite yhdistää WiFi-verkkoon
2. Mittaa:
   - Valon määrän (A0)
   - Maankosteuden (A6)
3. Lähettää mittaustiedot HTTP POST -pyyntönä palvelimelle
4. Palvelin palauttaa:
   - Kasteluun liittyvää tietoa
   - Aikaan liittyvää ohjausdataa
5. Laite tulostaa vastauksen sarjaporttiin

---
