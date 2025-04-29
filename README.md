Energia* on Karelia-ammattikorkeakoulun Älykkäät energiayhteisöt -hankkeen tuottama lämmityksen ohjausjärjestelmä.


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

C. Muita huomioita:
- Solmujen koodissa on pyritty niin laajaan kommentointiin, että pystyt ymmärtämään mitä niissä tapahtuu.
- Selaimen virkistäminen (F5): Jos dashboardin elementit eivät näy oikein ensimmäisellä kerralla, tee selainikkunan päivitys.
- Tiedostojen kirjoitus: Varmista, että Node-RED-käyttäjällä on oikeudet kirjoittaa tiedostoja siihen hakemistoon, jonne CSV-tiedostot tallennetaan.
- API-avaimet: Jos haet tietoa esim. ENTSO-E:stä, varmista että oma API-avaimesi on asetettu oikein hakupyynnön URL:iin

D. Vianmääritys
- Node-RED ei käynnisty: tarkista Node.js-asennus ja settings.js.
- Shelly-laitteet eivät yhdistä: tarkista IP:t ja verkko.
- Aikaleimat väärin: varmista moment-asennus ja aikavyöhyke.


© 2025 Ville Kuittinen/Karelia-ammattikorkeakoulu - MIT License - https://opensource.org/licenses/MIT
