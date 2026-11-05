# Aleksi15 Betaflight presets

Henkilökohtainen preset-lähde. Valmisteltu 5.11.2026 annetuista kopteridiffeistä.

## Käyttö

Julkaise tämä hakemisto omana julkisena GitHub-reponaan. Lisää repon URL ja julkaistu haara Betaflightin Presets > Preset Sources -kohtaan. Valitse oman firmwaren presetit, tarkista valinnat ja tallenna.

2026.6-kokonaisuus sisältää ratet, vanhan TinyTrainerin kytkimet, HDZero-OSD:n, neljän loogisen LEDin asetukset sekä akun ja coretempin hälytykset. Akun varoitus on 3,05 V/kenno, kriittinen raja 2,95 V/kenno ja coretemp 90 C. Akun arvot kirjoitetaan valittuun akkuprofiiliin. Rates-preset näkyy myös 4.5- ja 2025.12-versioille. Muut presetit on rajattu 2026.6-versioon.

Ratet ovat Betaflight-tyyppiä: RC Rate 0.98, Super Rate 0.58, Expo 0.01 kaikille akseleille. Ne kirjoitetaan valittuun rate-profiiliin. Kytkinpreset korvaa vanhat AUX-toiminnot ja tikkujen päätepisteet tämän handsetin arvoilla.

LED-väri voi seurata VTX-taajuutta tai olla jokin kuudesta käsin valittavasta kisaväristä. Betaflightin automaattiset värit eivät muodosta FAI:n määräämää kanavataulukkoa. FAI F9U 2026 v2 kohdan 1.6 fyysinen vaatimus on 32 RGB-LEDiä tai 280 mm diffusoitua nauhaa silloin kun järjestäjä vaatii kyseiset kisavalot. Neljä rinnakkaista neljän LEDin nauhaa on 16 fyysistä LEDiä.

## Rajat ja tarkistus

TTZ:n firmware on 2026.6.2. Pilotin asetukset ja automaattisen LED-tilan tallentuminen tarkistettiin CLI:stä uudelleenkäynnistyksen jälkeen. Kokonaispresetiä ei ole vielä koelennetty. Moottorit ja vastaanotin vaativat oman tarkistuksensa. Kiinteät värit ja LEDien fyysinen värijärjestys pitää tarkistaa oikeista valoista.

Ota täydellinen dump all ennen päivityksiä. Säilytä kopterikohtaiset asetukset ja vanhat firmwaret yksityisessä arkistossa. Tämä julkiseksi tarkoitettu repo sisältää vain pilotin asetuksia.

## Ylläpito

Muokkaa oikean firmwareversion tekstitiedostoa ja aja:

```sh
npm run index
npm run check
```

Indexer on Betaflightin firmware-presets-reposta, commit 50265ad54f82361aaa57489d1c2aae2e37c1e1b4. Sen GPL-3.0-lisenssi on mukana. Lisää uusi firmwareversio vasta CLI-yhteensopivuuden tarkistamisen jälkeen.

Lähteet: [Betaflight preset-lähteet](https://github.com/betaflight/firmware-presets#custom-sources), [FAI F9U 2026 v2](https://www.fai.org/sites/default/files/2026-06/CIAM-F9-Drones-2026-06-01.pdf).
