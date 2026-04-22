---
layout: default
title: Privatlivspolitik — Abba
---

# Privatlivspolitik

**Senest opdateret: 22. april 2026**

## 1. Introduktion

Abba ("vi", "vores", "appen") er en mobil bøns- og Stilletid-ledsager (Quiet Time) skabt til kristne, der ønsker at bede dybere. Denne Privatlivspolitik beskriver, hvordan Abba indsamler, bruger, opbevarer og beskytter dine oplysninger, når du bruger iOS-appen (Bundle ID: `com.ystech.abba`).

Abba drives i øjeblikket som et uafhængigt udviklerprojekt. Når vi siger "vi" i denne politik, mener vi Abba-teamet. Hvis Abba i fremtiden bliver et registreret selskab, vil denne politik blive opdateret tilsvarende.

Denne politik gælder verden over. Vi følger principperne i EU's Generelle Forordning om Databeskyttelse (GDPR), California Consumer Privacy Act (CCPA) og den koreanske Personal Information Protection Act (PIPA), hvor det er relevant.

## 2. Oplysninger vi indsamler

### 2.1 Kontooplysninger
Abba er **anonym som standard**. Når du åbner appen første gang, opretter vi et anonymt bruger-ID (UUID), så dine bønner og indstillinger kan synkroniseres på tværs af sessioner. Du behøver ikke angive navn, e-mail eller telefonnummer for at bruge Abba.

Du kan valgfrit logge ind med **Apple Sign-In** eller **Google Sign-In** for at sikkerhedskopiere dine data. I så fald modtager vi din e-mailadresse og en unik identifikator fra Apple eller Google. Du kan bruge "Skjul min e-mail" med Apple Sign-In, hvis du foretrækker det.

### 2.2 Bønneindhold (kernedata)
Når du bruger Abba, indsamler vi:
- **Lydoptagelser** af dine talte bønner
- **Udskrifter** genereret fra disse optagelser
- **Meditationstekst og refleksioner**, som du skriver eller genererer
- **Bibelske afsnit**, som du bogmærker

Dette er de mest følsomme data, Abba håndterer, og vi behandler dem med omhu. Din lyd opbevares i din egen private mappe på vores sikre lager. Kun du kan få adgang til den. Vi lytter ikke til den, deler den ikke og bruger den ikke til markedsføring.

### 2.3 Abonnementsoplysninger
Hvis du abonnerer på Abba Pro, registrerer en tredjepartstjeneste ved navn **RevenueCat** din abonnementsstatus (aktiv, udløbet, prøveperiode osv.) sammen med det anonyme ID. Vi modtager **ikke** dit kreditkortnummer — det bliver hos Apple.

### 2.4 Tekniske oplysninger
- Enhedens sprog (for at indstille dit standard-appsprog)
- Nedbrudslogs med maskerede personoplysninger (via Sentry)
- Push-notifikationstoken (FCM, valgfri — kun hvis du aktiverer notifikationer)
- App-version og iOS-version (til fejlfinding)

## 3. Sådan bruger vi dine oplysninger

Vi bruger dine oplysninger til:
- **At levere AI-analyse** af dine bønner og Stilletid-refleksioner (Google Gemini)
- **At synkronisere dine data** på tværs af sessioner og enheder
- **At administrere dit abonnement** og rettigheder
- **At rette fejl og forbedre appen** gennem nedbrudsrapporter
- **At sende valgfrie push-notifikationer** (daglige Stilletid-påmindelser), hvis du giver samtykke

Vi **gør ikke**:
- Viser reklamer af nogen art
- Sælger dine data til nogen
- Deler dit bønneindhold med tredjeparter (undtagen AI-behandlingen beskrevet nedenfor)
- Bruger dit indhold til at træne AI-modeller

## 4. Tredjepartstjenester

Abba er afhængig af et lille antal betroede tjenester for at fungere.

| Tjeneste | Formål | Sendte data | Region |
|---|---|---|---|
| **Supabase** | Database og godkendelse | Anonym ID, bønner, metadata | USA / EU |
| **Google Gemini API** | AI-analyse af bønner | Kun bønnetekst | Google Cloud |
| **RevenueCat** | Abonnementsadministration | Anonym ID, købskvitteringer | USA |
| **Sentry** | Nedbrudsrapporter (PII-maskeret) | Fejlspor uden e-mails, lange udskrifter, JWT fjernet | USA / EU |
| **Firebase Cloud Messaging** | Push-notifikationer (valgfri) | FCM-token | Google Cloud |
| **Apple Sign-In / Google Sign-In** | Valgfri kontokobling | E-mail, udbyder-ID | Apple / Google |

**Google Gemini:** I henhold til Googles offentliggjorte politik for betalt API-brug bruges bønneindhold, der sendes til Gemini, **ikke til at træne Googles AI-modeller**. Behandlingen er forbigående.

**Sentry PII-maskering:** Vi anvender maskeringsregler, før nedbrudsrapporter sendes — e-mails, koreanske udskrifter længere end 50 tegn, JWT'er og andre identifikatorer fjernes.

## 5. Datalagring og sikkerhed

- Alle data under overførsel er krypteret via HTTPS (TLS 1.2+).
- Data i hvile er beskyttet af vores databaseudbyders kryptering.
- **Row-Level Security (RLS)** i Supabase sikrer, at du kun kan få adgang til dine egne data.
- Lydfiler opbevares i mapper pr. bruger med adgang kontrolleret af dit godkendelsestoken.
- Adgangstokens opbevares i iOS Secure Enclave (`flutter_secure_storage`), aldrig i almindelige præferencer.

Vi opbevarer dine data, så længe din konto er aktiv. Hvis du sletter din konto, fjerner vi dine data inden for **30 dage**, undtagen hvor vi er lovmæssigt forpligtet til at opbevare registreringer (såsom skatteregistreringer for abonnementskøb, som Apple/RevenueCat opbevarer under deres egne politikker).

## 6. Dine rettigheder

Du har følgende rettigheder vedrørende dine personoplysninger:

- **Adgang** — anmode om en kopi af de data, vi har om dig
- **Rettelse** — bede os om at rette unøjagtige oplysninger
- **Sletning** — bede os om at slette din konto og data (tilgængelig i appen: Indstillinger → Konto → Slet konto, eller via e-mail)
- **Overførbarhed** — anmode om en eksport af dine data i et maskinlæsbart format
- **Indsigelse** — gøre indsigelse mod visse behandlinger
- **Trække samtykke tilbage** — du kan til enhver tid tilbagekalde samtykke til push-notifikationer, AI-behandling eller kontokobling

For GDPR- (EU) og CCPA-residenter (Californien) er disse rettigheder garanteret ved lov. For at udøve en rettighed, send en e-mail til **rrallvv@gmail.com**. Vi svarer inden for 30 dage.

## 7. Børns privatliv

Abba er vurderet 4+ i App Store. Vi indsamler ikke bevidst oplysninger fra børn under 13 år (COPPA) eller under 16 år (GDPR, i nogle EU-lande) uden verificerbart forældresamtykke. Hvis du mener, at et barn har givet personoplysninger, bedes du kontakte os, og vi vil slette dem omgående.

## 8. Internationale dataoverførsler

Vores infrastruktur hostes i USA og Den Europæiske Union. Ved at bruge Abba giver du samtykke til, at dine data overføres til og behandles i disse regioner. Vi støtter os på Standardkontraktbestemmelser (SCC'er), hvor det kræves.

## 9. Regerings- og juridiske anmodninger

Vi videregiver kun brugerdata, når det er lovmæssigt påkrævet (gyldig stævning, retskendelse eller tilsvarende). Vi offentliggør endnu ikke en gennemsigtighedsrapport, men vi forpligter os til at underrette berørte brugere, når loven tillader det.

## 10. Ændringer af denne politik

Vi kan opdatere denne Privatlivspolitik, efterhånden som Abba udvikler sig. Ved væsentlige ændringer vil vi underrette dig i appen og opdatere datoen "Senest opdateret" øverst. Fortsat brug af Abba efter ændringer betyder, at du accepterer den opdaterede politik.

## 11. Kontakt os

Spørgsmål, anmodninger eller klager?

- **E-mail:** rrallvv@gmail.com
- **Svartid:** inden for 30 dage (normalt hurtigere)

Du har også ret til at indgive en klage til din lokale databeskyttelsesmyndighed (f.eks. Datatilsynet i Danmark, DPA'en i dit EU-medlemsland, Californiens Attorney General eller Koreas PIPC).

---

⚠️ **Oversættelsesmeddelelse**: Dette er en oversættelse leveret for nemheds skyld. I tilfælde af uoverensstemmelser har [den engelske version](../privacy.html) forrang.
