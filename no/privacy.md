---
layout: default
title: Personvernerklæring — Abba
---

# Personvernerklæring

**Sist oppdatert: 22. april 2026**

## 1. Introduksjon

Abba ("vi", "vår", "appen") er en mobil bønne- og Stille Tid-følgesvenn (Quiet Time) laget for kristne som ønsker å be dypere. Denne Personvernerklæringen beskriver hvordan Abba samler inn, bruker, lagrer og beskytter informasjonen din når du bruker iOS-appen (Bundle ID: `com.ystech.abba`).

Abba drives for øyeblikket som et uavhengig utviklerprosjekt. Når vi sier "vi" i denne erklæringen, mener vi Abba-teamet. Hvis Abba blir et registrert selskap i fremtiden, vil denne erklæringen bli oppdatert deretter.

Denne erklæringen gjelder globalt. Vi følger prinsippene i EUs generelle personvernforordning (GDPR), California Consumer Privacy Act (CCPA) og den koreanske Personal Information Protection Act (PIPA), der det er aktuelt.

## 2. Informasjon vi samler inn

### 2.1 Kontoinformasjon
Abba er **anonym som standard**. Når du åpner appen for første gang, oppretter vi en anonym bruker-ID (UUID) slik at bønnene og innstillingene dine kan synkroniseres på tvers av økter. Du trenger ikke å oppgi navn, e-post eller telefonnummer for å bruke Abba.

Du kan valgfritt logge inn med **Apple Sign-In** eller **Google Sign-In** for å sikkerhetskopiere dataene dine. I så fall mottar vi e-postadressen din og en unik identifikator fra Apple eller Google. Du kan bruke "Skjul e-postadressen min" med Apple Sign-In hvis du foretrekker det.

### 2.2 Bønneinnhold (kjernedata)
Når du bruker Abba, samler vi inn:
- **Lydopptak** av dine uttalte bønner
- **Transkripsjoner** generert fra disse opptakene
- **Meditasjonstekst og refleksjoner** som du skriver eller genererer
- **Bibelavsnitt** som du bokmerker

Dette er de mest sensitive dataene Abba håndterer, og vi behandler dem med omhu. Lyden din lagres i din egen private mappe på vår sikre lagring. Bare du kan få tilgang til den. Vi lytter ikke til den, deler den ikke og bruker den ikke til markedsføring.

### 2.3 Abonnementsinformasjon
Hvis du abonnerer på Abba Pro, registrerer en tredjepartstjeneste kalt **RevenueCat** abonnementsstatusen din (aktiv, utløpt, prøveperiode, osv.) sammen med den anonyme ID-en. Vi mottar **ikke** kredittkortnummeret ditt — det forblir hos Apple.

### 2.4 Teknisk informasjon
- Enhetens språk (for å angi standard appspråk)
- Krasjlogger med maskerte personopplysninger (via Sentry)
- Push-varslingstoken (FCM, valgfritt — kun hvis du aktiverer varsler)
- App-versjon og iOS-versjon (for feilsøking)

## 3. Hvordan vi bruker informasjonen din

Vi bruker informasjonen din til å:
- **Gi AI-analyse** av bønnene dine og Stille Tid-refleksjoner (Google Gemini)
- **Synkronisere dataene dine** på tvers av økter og enheter
- **Administrere abonnementet ditt** og rettigheter
- **Rette feil og forbedre appen** gjennom krasjrapporter
- **Sende valgfrie push-varsler** (daglige Stille Tid-påminnelser) hvis du samtykker

Vi **gjør ikke**:
- Viser reklame av noe slag
- Selger dataene dine til noen
- Deler bønneinnholdet ditt med tredjeparter (bortsett fra AI-behandlingen beskrevet nedenfor)
- Bruker innholdet ditt til å trene AI-modeller

## 4. Tredjepartstjenester

Abba er avhengig av et lite antall pålitelige tjenester for å fungere.

| Tjeneste | Formål | Sendte data | Region |
|---|---|---|---|
| **Supabase** | Database og autentisering | Anonym ID, bønner, metadata | USA / EU |
| **Google Gemini API** | AI-analyse av bønner | Kun bønnetekst | Google Cloud |
| **RevenueCat** | Abonnementshåndtering | Anonym ID, kjøpskvitteringer | USA |
| **Sentry** | Krasjrapporter (PII-maskert) | Feilspor uten e-poster, lange transkripsjoner, JWT fjernet | USA / EU |
| **Firebase Cloud Messaging** | Push-varsler (valgfritt) | FCM-token | Google Cloud |
| **Apple Sign-In / Google Sign-In** | Valgfri kontokobling | E-post, leverandør-ID | Apple / Google |

**Google Gemini:** I henhold til Googles publiserte retningslinjer for betalt API-bruk brukes bønneinnhold som sendes til Gemini **ikke til å trene Googles AI-modeller**. Behandlingen er forbigående.

**Sentry PII-maskering:** Vi bruker maskeringsregler før krasjrapporter sendes — e-poster, koreanske transkripsjoner lengre enn 50 tegn, JWT og andre identifikatorer fjernes.

## 5. Datalagring og sikkerhet

- All data under overføring er kryptert via HTTPS (TLS 1.2+).
- Data i hvile er beskyttet av vår databaseleverandørs kryptering.
- **Row-Level Security (RLS)** i Supabase sikrer at du kun får tilgang til dine egne data.
- Lydfiler lagres i mapper per bruker med tilgang kontrollert av autentiseringstokenet ditt.
- Tilgangstokener lagres i iOS Secure Enclave (`flutter_secure_storage`), aldri i vanlige innstillinger.

Vi oppbevarer dataene dine så lenge kontoen din er aktiv. Hvis du sletter kontoen, fjerner vi dataene dine innen **30 dager**, bortsett fra der vi er lovpålagt å oppbevare opptegnelser (for eksempel skattedokumenter for abonnementskjøp, som Apple/RevenueCat oppbevarer i henhold til sine egne retningslinjer).

## 6. Dine rettigheter

Du har følgende rettigheter over personopplysningene dine:

- **Tilgang** — be om en kopi av dataene vi har om deg
- **Retting** — be oss om å rette unøyaktig informasjon
- **Sletting** — be oss om å slette kontoen og dataene dine (tilgjengelig i appen: Innstillinger → Konto → Slett konto, eller via e-post)
- **Portabilitet** — be om eksport av dataene dine i maskinlesbart format
- **Innsigelse** — motsette seg visse behandlinger
- **Trekke tilbake samtykke** — du kan når som helst trekke tilbake samtykke for push-varsler, AI-behandling eller kontokobling

For GDPR- (EU) og CCPA-innbyggere (California) er disse rettighetene garantert ved lov. For å utøve en rettighet, send en e-post til **rrallvv@gmail.com**. Vi svarer innen 30 dager.

## 7. Barns personvern

Abba har 4+-rangering i App Store. Vi samler ikke bevisst inn informasjon fra barn under 13 år (COPPA) eller under 16 år (GDPR, i noen EU-land) uten verifiserbar foreldresamtykke. Hvis du tror at et barn har gitt personopplysninger, vennligst kontakt oss, og vi vil slette dem umiddelbart.

## 8. Internasjonale dataoverføringer

Vår infrastruktur er hostet i USA og EU. Ved å bruke Abba samtykker du til at dataene dine overføres til og behandles i disse regionene. Vi bruker standard kontraktsklausuler (SCC) der det kreves.

## 9. Myndighets- og rettslige forespørsler

Vi avslører kun brukerdata når det er lovpålagt (gyldig stevning, rettskjennelse eller tilsvarende). Vi publiserer ennå ikke en åpenhetsrapport, men vi forplikter oss til å varsle berørte brukere når loven tillater det.

## 10. Endringer i denne erklæringen

Vi kan oppdatere denne Personvernerklæringen etter hvert som Abba utvikler seg. Ved vesentlige endringer vil vi varsle deg i appen og oppdatere datoen "Sist oppdatert" øverst. Fortsatt bruk av Abba etter endringer betyr at du godtar den oppdaterte erklæringen.

## 11. Kontakt oss

Spørsmål, forespørsler eller klager?

- **E-post:** rrallvv@gmail.com
- **Svartid:** innen 30 dager (vanligvis tidligere)

Du har også rett til å sende inn en klage til din lokale databeskyttelsesmyndighet (f.eks. Datatilsynet i Norge, DPA i din EU-medlemsstat, Californias Attorney General eller Koreas PIPC).

---

⚠️ **Oversettelsesmerknad**: Dette er en oversettelse som er levert for bekvemmelighet. Ved avvik gjelder den [engelske versjonen](../privacy.html).
