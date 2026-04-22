---
layout: default
title: Tietosuojakäytäntö — Abba
---

# Tietosuojakäytäntö

**Viimeksi päivitetty: 22. huhtikuuta 2026**

## 1. Johdanto

Abba ("me", "meidän", "sovellus") on mobiilirukous- ja Hiljaisen Ajan (Quiet Time) kumppani, joka on luotu kristityille, jotka haluavat rukoilla syvällisemmin. Tämä Tietosuojakäytäntö kuvaa, kuinka Abba kerää, käyttää, tallentaa ja suojaa tietojasi, kun käytät iOS-sovellusta (Bundle ID: `com.ystech.abba`).

Abba toimii tällä hetkellä itsenäisenä kehittäjäprojektina. Kun sanomme "me" tässä käytännössä, tarkoitamme Abba-tiimiä. Jos Abbasta tulee tulevaisuudessa rekisteröity yritys, tätä käytäntöä päivitetään vastaavasti.

Tämä käytäntö pätee maailmanlaajuisesti. Noudatamme EU:n yleisen tietosuoja-asetuksen (GDPR), California Consumer Privacy Actin (CCPA) ja Korean henkilötietojen suojalain (PIPA) periaatteita soveltuvin osin.

## 2. Keräämämme tiedot

### 2.1 Tilitiedot
Abba on **oletusarvoisesti anonyymi**. Kun avaat sovelluksen ensimmäisen kerran, luomme anonyymin käyttäjätunnuksen (UUID), jotta rukouksesi ja asetuksesi voivat synkronoitua istuntojen välillä. Sinun ei tarvitse antaa nimeä, sähköpostiosoitetta tai puhelinnumeroa käyttääksesi Abbaa.

Voit halutessasi kirjautua sisään **Apple Sign-In** tai **Google Sign-In** -kautta varmuuskopioidaksesi tietosi. Siinä tapauksessa vastaanotamme sähköpostiosoitteesi ja yksilöllisen tunnisteen Applelta tai Googlelta. Voit käyttää Apple Sign-Inin "Piilota sähköpostini" -toimintoa, jos haluat.

### 2.2 Rukoussisältö (keskeiset tiedot)
Kun käytät Abbaa, keräämme:
- **Äänitallenteita** ääneen lausutuista rukouksistasi
- **Litteroinnit**, jotka on luotu näistä tallenteista
- **Mietiskelytekstit ja pohdinnat**, joita kirjoitat tai luot
- **Raamatunkohdat**, jotka merkitset suosikeiksi

Nämä ovat arkaluontoisimpia tietoja, joita Abba käsittelee, ja kohtelemme niitä huolellisesti. Äänesi tallennetaan omaan yksityiseen kansioosi turvallisella palvelimellamme. Vain sinä voit käyttää sitä. Emme kuuntele sitä, emme jaa sitä emmekä käytä sitä markkinointiin.

### 2.3 Tilaustiedot
Jos tilaat Abba Pron, kolmannen osapuolen palvelu nimeltä **RevenueCat** tallentaa tilauksesi tilan (aktiivinen, vanhentunut, kokeilu jne.) yhdessä anonyymin tunnisteen kanssa. **Emme** vastaanota luottokorttisi numeroa — se jää Applelle.

### 2.4 Tekniset tiedot
- Laitteen kieli (sovelluksen oletuskielen asettamiseen)
- Kaatumislokit henkilötiedot peitettyinä (Sentryn kautta)
- Push-ilmoitustoken (FCM, valinnainen — vain jos otat ilmoitukset käyttöön)
- Sovellusversio ja iOS-versio (virheenkorjaukseen)

## 3. Kuinka käytämme tietojasi

Käytämme tietojasi:
- **Tarjotaksemme AI-analyysin** rukouksistasi ja Hiljaisen Ajan pohdinnoista (Google Gemini)
- **Synkronoidaksemme tietosi** istuntojen ja laitteiden välillä
- **Hallitaksemme tilaustasi** ja käyttöoikeuksia
- **Korjataksemme bugeja ja parantaaksemme sovellusta** kaatumisraporttien kautta
- **Lähettääksemme valinnaisia push-ilmoituksia** (päivittäiset Hiljaisen Ajan muistutukset), jos suostut

**Emme**:
- Näytä minkäänlaista mainontaa
- Myy tietojasi kenellekään
- Jaa rukoussisältöäsi kolmansille osapuolille (paitsi alla kuvattu AI-käsittely)
- Käytä sisältöäsi AI-mallien kouluttamiseen

## 4. Kolmannen osapuolen palvelut

Abba luottaa pieneen määrään luotettavia palveluita toimiakseen.

| Palvelu | Tarkoitus | Lähetetyt tiedot | Alue |
|---|---|---|---|
| **Supabase** | Tietokanta ja todennus | Anonyymi tunniste, rukoukset, metatiedot | USA / EU |
| **Google Gemini API** | Rukousten AI-analyysi | Vain rukousteksti | Google Cloud |
| **RevenueCat** | Tilaustenhallinta | Anonyymi tunniste, ostokuitit | USA |
| **Sentry** | Kaatumisraportit (PII peitettyinä) | Virhejäljet ilman sähköposteja, pitkiä litterointeja, JWT poistettu | USA / EU |
| **Firebase Cloud Messaging** | Push-ilmoitukset (valinnainen) | FCM-token | Google Cloud |
| **Apple Sign-In / Google Sign-In** | Valinnainen tilin linkitys | Sähköposti, toimittajan tunniste | Apple / Google |

**Google Gemini:** Googlen julkaiseman maksullisen API-käytön käytännön mukaan Geminiin lähetettyä rukoussisältöä **ei käytetä Googlen AI-mallien kouluttamiseen**. Käsittely on väliaikaista.

**Sentryn PII-peitto:** Käytämme peittosääntöjä ennen kaatumisraporttien lähettämistä — sähköpostit, yli 50 merkkiä pitkät korealaiset litteroinnit, JWT:t ja muut tunnisteet poistetaan.

## 5. Tietojen säilytys ja turvallisuus

- Kaikki siirrettävä tieto on salattu HTTPS:n (TLS 1.2+) kautta.
- Levossa olevat tiedot on suojattu tietokantapalveluntarjoajamme salauksella.
- **Rivitason suojaus (RLS)** Supabasessa varmistaa, että pääset käsiksi vain omiin tietoihisi.
- Äänitiedostot tallennetaan käyttäjäkohtaisiin kansioihin, joiden käyttöä ohjaa todennustokenisi.
- Pääsytokenit tallennetaan iOS Secure Enclaveen (`flutter_secure_storage`), ei koskaan tavallisiin asetuksiin.

Säilytämme tietojasi niin kauan kuin tilisi on aktiivinen. Jos poistat tilisi, poistamme tietosi **30 päivän kuluessa**, lukuun ottamatta tilanteita, joissa olemme lain mukaan velvollisia säilyttämään tietoja (kuten tilausten verotietoja, jotka Apple/RevenueCat säilyttävät omien käytäntöjensä mukaan).

## 6. Oikeutesi

Sinulla on seuraavat oikeudet henkilötietoihisi:

- **Pääsy** — pyytää kopio meillä olevista tiedoistasi
- **Oikaisu** — pyytää meitä korjaamaan virheellisiä tietoja
- **Poisto** — pyytää meitä poistamaan tilisi ja tietosi (saatavilla sovelluksessa: Asetukset → Tili → Poista tili, tai sähköpostitse)
- **Siirrettävyys** — pyytää tietojesi vientiä koneellisesti luettavassa muodossa
- **Vastustusoikeus** — vastustaa tiettyä käsittelyä
- **Peruuttaa suostumus** — voit milloin tahansa peruuttaa suostumuksesi push-ilmoituksille, AI-käsittelylle tai tilin linkitykselle

GDPR:n (EU) ja CCPA:n (Kalifornia) asukkaille nämä oikeudet on taattu lailla. Käyttääksesi mitä tahansa oikeutta, lähetä sähköpostia osoitteeseen **rrallvv@gmail.com**. Vastaamme 30 päivän kuluessa.

## 7. Lasten yksityisyys

Abballa on 4+-luokitus App Storessa. Emme tietoisesti kerää tietoja alle 13-vuotiailta lapsilta (COPPA) tai alle 16-vuotiailta (GDPR, joissakin EU-maissa) ilman todennettavaa vanhemman suostumusta. Jos epäilet, että lapsi on antanut henkilötietoja, ota meihin yhteyttä, niin poistamme ne välittömästi.

## 8. Kansainväliset tiedonsiirrot

Infrastruktuurimme sijaitsee Yhdysvalloissa ja Euroopan unionissa. Käyttämällä Abbaa suostut tietojesi siirtoon ja käsittelyyn näillä alueilla. Käytämme tarvittaessa vakiosopimuslausekkeita (SCC).

## 9. Hallituksen ja lainvalvonnan pyynnöt

Paljastamme käyttäjätietoja vain, kun laki sitä vaatii (pätevä haastemääräys, tuomioistuimen määräys tai vastaava). Emme vielä julkaise avoimuusraporttia, mutta sitoudumme ilmoittamaan asianomaisille käyttäjille, kun laki sen sallii.

## 10. Muutokset tähän käytäntöön

Saatamme päivittää tätä Tietosuojakäytäntöä Abban kehittyessä. Kun teemme olennaisia muutoksia, ilmoitamme sinulle sovelluksessa ja päivitämme ylhäällä olevan "Viimeksi päivitetty" -päivämäärän. Abban jatkuva käyttö muutosten jälkeen tarkoittaa, että hyväksyt päivitetyn käytännön.

## 11. Ota yhteyttä

Kysymyksiä, pyyntöjä tai valituksia?

- **Sähköposti:** rrallvv@gmail.com
- **Vastausaika:** 30 päivän kuluessa (yleensä aiemmin)

Sinulla on myös oikeus tehdä valitus paikalliselle tietosuojaviranomaiselle (esim. Tietosuojavaltuutetulle Suomessa, EU-jäsenvaltion DPA:lle, Kalifornian yleiselle syyttäjälle tai Korean PIPC:lle).

---

⚠️ **Käännösilmoitus**: Tämä on käännös, joka on tarjottu mukavuussyistä. Ristiriitatilanteessa [englanninkielinen versio](../privacy.html) on etusijalla.
