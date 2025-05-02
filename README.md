Energia* on Karelia-ammattikorkeakoulun Älykkäät energiayhteisöt -hankkeen tuottama lämmityksen ohjausjärjestelmä.
Hanke on Euroopan unionin osarahoittama (https://www.karelia.fi/projektit/alykkaat-energiayhteisot/).


 Sisältö
- Node-RED -flowt lämmityksen, virheiden ja hintatiedon hallintaan
- Dashboard (UI) käyttöliittymä hintojen ja päätösten visualisointiin
- Virheiden keräys ja tallennus CSV-tiedostoksi
- Valmiit tukikoodit ja asennusohjeet

Tervetuloa käyttämään Energia* järjestelmää. Tämä dokumentti kertoo, mitä tarvitaan ja miten saat kaiken toimimaan Node-RED:issä.

A. Node-RED Asennus
- Asenna Node.js virallisilta sivuilta: https://nodejs.org/
- Tarkista versiot: node -v ja npm -v
- Asenna Node-RED: sudo npm install -g --unsafe-perm node-red
- Käynnistä Node-RED komennolla: node-red
- Avaa selain: http://localhost:1880 (yleensä http://127.0.0.1:1880)

B. Komponenttien Asennus Node-RED:iin
1.	Avaa selain ja mene Node-RED:n hallintapaneeliin
2.	Klikkaa oikeasta yläkulmasta "Manage palette" (hammasratas).
3.	Valitse "Install"-välilehti.
4.	Etsi ja asenna seuraavat:
   - node-red-dashboard
   - node-red-node-moment
   - node-red-node-csv
6.	Lisää moment-timezone settings.js -tiedostoon globaaliksi muuttujaksi:
7.	functionGlobalContext: { moment: require('moment-timezone') }
8.	Käynnistä Node-RED uudelleen
9. Flow:t tuodaan Node-RED:iin import toiminnon kautta.

C. Muita huomioita:
- Solmujen koodissa on pyritty niin laajaan kommentointiin, että pystyt ymmärtämään mitä niissä tapahtuu.
- Selaimen virkistäminen (F5): Jos dashboardin elementit eivät näy oikein ensimmäisellä kerralla, tee selainikkunan päivitys.
- Tiedostojen kirjoitus: Varmista, että Node-RED-käyttäjällä on oikeudet kirjoittaa tiedostoja siihen hakemistoon, jonne CSV-tiedostot tallennetaan.
- API-avaimet: Jos haet tietoa esim. ENTSO-E:stä, varmista että oma API-avaimesi on asetettu oikein hakupyynnön URL:iin


Tämä projekti on julkaistu MIT License -lisenssillä.

Copyright © 2025
Ville Kuittinen / Karelia-ammattikorkeakoulu

Saa käyttää, muokata ja jakaa vapaasti. Ei takuita toimivuudesta.
Alkuperäinen lähde on mainittava.
