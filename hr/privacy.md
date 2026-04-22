---
layout: default
title: Pravila o privatnosti — Abba
---

# Pravila o privatnosti

**Posljednje ažuriranje: 22. travnja 2026.**

## 1. Uvod

Abba („mi", „naš", „aplikacija") je mobilni pratitelj molitve i Tihog vremena (Quiet Time) izrađen za kršćane koji žele dublje moliti. Ova Pravila o privatnosti opisuju kako Abba prikuplja, koristi, pohranjuje i štiti vaše podatke kada koristite iOS aplikaciju (Bundle ID: `com.ystech.abba`).

Abba se trenutno vodi kao samostalni programerski projekt. Kada u ovim pravilima kažemo „mi", mislimo na Abba tim. Ako Abba u budućnosti postane registrirana tvrtka, ova pravila bit će ažurirana u skladu s tim.

Ova pravila vrijede u cijelom svijetu. Slijedimo načela Opće uredbe EU o zaštiti podataka (GDPR), California Consumer Privacy Act (CCPA) i korejskog Zakona o zaštiti osobnih podataka (PIPA), gdje je primjenjivo.

## 2. Podaci koje prikupljamo

### 2.1 Podaci o računu
Abba je **prema zadanim postavkama anonimna**. Kada prvi put otvorite aplikaciju, kreiramo anonimni ID korisnika (UUID) kako bi se vaše molitve i postavke mogle sinkronizirati između sesija. Ne morate navesti ime, e-poštu ili telefonski broj za korištenje Abbe.

Možete se po izboru prijaviti putem **Apple Sign-In** ili **Google Sign-In** za sigurnosnu kopiju podataka. U tom slučaju primamo vašu e-mail adresu i jedinstveni identifikator od Applea ili Googlea. Možete koristiti „Sakrij moju e-poštu" s Apple Sign-In ako želite.

### 2.2 Sadržaj molitvi (osnovni podaci)
Kada koristite Abbu, prikupljamo:
- **Audio snimke** vaših izgovorenih molitvi
- **Prijepise** generirane iz tih snimki
- **Tekstove meditacije i razmišljanja** koje pišete ili generirate
- **Biblijske ulomke** koje označite

Ovo su najosjetljiviji podaci kojima Abba rukuje i s njima postupamo s pažnjom. Vaš audio se pohranjuje u vlastitu privatnu mapu na našem sigurnom pohranjivanju. Pristup imate samo vi. Ne slušamo ih, ne dijelimo ih i ne koristimo ih za marketing.

### 2.3 Podaci o pretplati
Ako se pretplatite na Abba Pro, usluga treće strane pod nazivom **RevenueCat** bilježi status vaše pretplate (aktivna, istekla, probno razdoblje, itd.) zajedno s anonimnim ID-om. **Ne** primamo broj vaše kreditne kartice — on ostaje kod Applea.

### 2.4 Tehnički podaci
- Jezik uređaja (za postavljanje zadanog jezika aplikacije)
- Zapisnici o padovima s maskiranim osobnim podacima (putem Sentryja)
- Token push obavijesti (FCM, neobavezan — samo ako omogućite obavijesti)
- Verzija aplikacije i verzija iOS-a (za otklanjanje pogrešaka)

## 3. Kako koristimo vaše podatke

Vaše podatke koristimo za:
- **Pružanje AI analize** vaših molitvi i razmišljanja Tihog vremena (Google Gemini)
- **Sinkronizaciju vaših podataka** između sesija i uređaja
- **Upravljanje vašom pretplatom** i ovlaštenjima
- **Ispravljanje grešaka i poboljšanje aplikacije** putem izvještaja o padovima
- **Slanje neobaveznih push obavijesti** (dnevne podsjetnike za Tiho vrijeme) ako pristanete

**Ne**:
- Prikazujemo oglase bilo koje vrste
- Prodajemo vaše podatke bilo kome
- Dijelimo sadržaj vaših molitvi s trećim stranama (osim AI obrade opisane u nastavku)
- Koristimo vaš sadržaj za treniranje AI modela

## 4. Usluge trećih strana

Abba se oslanja na mali broj pouzdanih usluga za svoj rad.

| Usluga | Svrha | Poslani podaci | Regija |
|---|---|---|---|
| **Supabase** | Baza podataka i autentifikacija | Anonimni ID, molitve, metapodaci | SAD / EU |
| **Google Gemini API** | AI analiza molitvi | Samo tekst molitve | Google Cloud |
| **RevenueCat** | Upravljanje pretplatama | Anonimni ID, računi o kupnji | SAD |
| **Sentry** | Izvještaji o padovima (PII maskiran) | Tragovi grešaka bez e-poruka, dugih prijepisa, JWT uklonjeni | SAD / EU |
| **Firebase Cloud Messaging** | Push obavijesti (neobavezno) | FCM token | Google Cloud |
| **Apple Sign-In / Google Sign-In** | Neobavezno povezivanje računa | E-pošta, ID davatelja | Apple / Google |

**Google Gemini:** Prema objavljenoj Googleovoj politici za plaćenu upotrebu API-ja, sadržaj molitvi poslan u Gemini **ne koristi se za treniranje Googleovih AI modela**. Obrada je prolazna.

**Sentry maskiranje PII:** Primjenjujemo pravila maskiranja prije slanja izvještaja o padovima — e-pošta, korejski prijepisi dulji od 50 znakova, JWT i drugi identifikatori uklanjaju se.

## 5. Pohrana i sigurnost podataka

- Svi podaci u prijenosu šifrirani su putem HTTPS-a (TLS 1.2+).
- Podaci u mirovanju zaštićeni su enkripcijom našeg pružatelja baze podataka.
- **Row-Level Security (RLS)** u Supabaseu osigurava da možete pristupiti samo vlastitim podacima.
- Audio datoteke pohranjuju se u mape po korisniku s pristupom kontroliranim vašim autentifikacijskim tokenom.
- Tokeni pristupa pohranjuju se u iOS Secure Enclave (`flutter_secure_storage`), nikad u običnim postavkama.

Vaše podatke zadržavamo dok je vaš račun aktivan. Ako izbrišete svoj račun, uklanjamo vaše podatke unutar **30 dana**, osim u slučajevima kada smo pravno obvezni voditi evidenciju (kao što su porezni zapisi za kupnju pretplate, koje Apple/RevenueCat čuvaju prema vlastitim pravilima).

## 6. Vaša prava

Imate sljedeća prava u vezi s vašim osobnim podacima:

- **Pristup** — zatražiti kopiju podataka koje držimo o vama
- **Ispravak** — tražiti nas da ispravimo netočne podatke
- **Brisanje** — tražiti nas da izbrišemo vaš račun i podatke (dostupno u aplikaciji: Postavke → Račun → Izbriši račun, ili putem e-pošte)
- **Prenosivost** — zatražiti izvoz podataka u strojno čitljivom formatu
- **Prigovor** — uložiti prigovor protiv određene obrade
- **Povlačenje pristanka** — možete u svakom trenutku opozvati pristanak za push obavijesti, AI obradu ili povezivanje računa

Za stanovnike GDPR-a (EU) i CCPA-a (Kalifornija) ova su prava zajamčena zakonom. Za ostvarivanje bilo kojeg prava pošaljite e-poštu na **rrallvv@gmail.com**. Odgovaramo unutar 30 dana.

## 7. Privatnost djece

Abba ima ocjenu 4+ u App Storeu. Svjesno ne prikupljamo podatke od djece mlađe od 13 godina (COPPA) ili mlađe od 16 godina (GDPR, u nekim zemljama EU) bez provjerljivog roditeljskog pristanka. Ako vjerujete da je dijete dalo osobne podatke, kontaktirajte nas i odmah ćemo ih izbrisati.

## 8. Međunarodni prijenosi podataka

Naša infrastruktura smještena je u Sjedinjenim Državama i Europskoj uniji. Korištenjem Abbe pristajete na prijenos i obradu vaših podataka u tim regijama. Gdje je to potrebno, oslanjamo se na Standardne ugovorne klauzule (SCC).

## 9. Vladini i pravni zahtjevi

Podatke korisnika otkrivamo samo kada to zakon zahtijeva (važeći sudski poziv, sudski nalog ili ekvivalent). Još ne objavljujemo izvještaj o transparentnosti, ali se obvezujemo obavijestiti pogođene korisnike kada to zakon dopušta.

## 10. Izmjene ovih pravila

Ova Pravila o privatnosti možemo ažurirati kako se Abba razvija. Kod značajnih promjena obavijestit ćemo vas u aplikaciji i ažurirati datum „Posljednje ažuriranje" na vrhu. Nastavak korištenja Abbe nakon promjena znači da prihvaćate ažurirana pravila.

## 11. Kontaktirajte nas

Pitanja, zahtjevi ili pritužbe?

- **E-pošta:** rrallvv@gmail.com
- **Vrijeme odgovora:** unutar 30 dana (obično ranije)

Također imate pravo podnijeti pritužbu lokalnom tijelu za zaštitu podataka (npr. AZOP u Hrvatskoj, DPA vaše države članice EU, Općem državnom odvjetniku Kalifornije ili korejskom PIPC-u).

---

⚠️ **Obavijest o prijevodu**: Ovo je prijevod osiguran radi praktičnosti. U slučaju bilo kakvog odstupanja, mjerodavna je [engleska verzija](../privacy.html).
