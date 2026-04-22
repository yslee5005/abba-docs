---
layout: default
title: Privacybeleid — Abba
---

# Privacybeleid

**Laatst bijgewerkt: 22 april 2026**

## 1. Inleiding

Abba ("wij", "onze", "de app") is een mobiele gebed- en Stille Tijd-metgezel, gemaakt voor christenen die dieper willen bidden. Dit Privacybeleid beschrijft hoe Abba uw informatie verzamelt, gebruikt, opslaat en beschermt wanneer u de iOS-app gebruikt (Bundle ID: `com.ystech.abba`).

Abba wordt momenteel geëxploiteerd als een onafhankelijk ontwikkelaarsproject. Als we in dit beleid "wij" zeggen, bedoelen we het Abba-team. Als Abba in de toekomst een geregistreerd bedrijf wordt, zal dit beleid dienovereenkomstig worden bijgewerkt.

Dit beleid geldt wereldwijd. We volgen de principes van de EU Algemene Verordening Gegevensbescherming (AVG/GDPR), de California Consumer Privacy Act (CCPA) en de Koreaanse Personal Information Protection Act (PIPA), waar van toepassing.

## 2. Informatie die wij verzamelen

### 2.1 Accountgegevens
Abba is **anoniem-eerst**. Wanneer u de app voor de eerste keer opent, maken we een anonieme gebruikers-ID (UUID) aan zodat uw gebeden en instellingen over sessies heen kunnen synchroniseren. U hoeft geen naam, e-mailadres of telefoonnummer op te geven om Abba te gebruiken.

U kunt optioneel inloggen met **Apple Sign-In** of **Google Sign-In** om uw gegevens te back-uppen. In dat geval ontvangen we uw e-mailadres en een unieke identifier van Apple of Google. U kunt "Mijn e-mail verbergen" gebruiken met Apple Sign-In als u dat verkiest.

### 2.2 Gebedsinhoud (kerngegevens)
Wanneer u Abba gebruikt, verzamelen wij:
- **Audio-opnamen** van uw gesproken gebeden
- **Transcripties** gegenereerd uit die opnamen
- **Meditatieteksten en reflecties** die u schrijft of genereert
- **Bijbelgedeelten** die u markeert

Dit zijn de meest gevoelige gegevens die Abba verwerkt, en we behandelen ze zorgvuldig. Uw audio wordt opgeslagen in uw eigen privémap op onze beveiligde opslag. Alleen u heeft er toegang toe. Wij luisteren er niet naar, delen het niet, en gebruiken het niet voor marketing.

### 2.3 Abonnementsinformatie
Als u zich abonneert op Abba Pro, registreert een externe dienst genaamd **RevenueCat** uw abonnementsstatus (actief, verlopen, proef, enz.) samen met de anonieme ID. Wij ontvangen uw creditcardnummer **niet** — dat blijft bij Apple.

### 2.4 Technische informatie
- Apparaattaal (om uw standaard app-taal in te stellen)
- Crashlogs met gemaskeerde persoonsgegevens (via Sentry)
- Push-notificatietoken (FCM, optioneel — alleen als u notificaties inschakelt)
- App-versie en iOS-versie (voor debugging)

## 3. Hoe wij uw informatie gebruiken

Wij gebruiken uw informatie om:
- **AI-analyse te bieden** van uw gebeden en Stille Tijd-reflecties (Google Gemini)
- **Uw gegevens te synchroniseren** tussen sessies en apparaten
- **Uw abonnement te beheren** en rechten te verifiëren
- **Bugs te verhelpen en de app te verbeteren** via crashrapporten
- **Optionele pushnotificaties te sturen** (dagelijkse Stille Tijd-herinneringen) als u ermee instemt

Wij doen **niet**:
- Advertenties van welke aard dan ook tonen
- Uw gegevens aan wie dan ook verkopen
- Uw gebedsinhoud delen met derden (behalve de AI-verwerking hieronder beschreven)
- Uw inhoud gebruiken om AI-modellen te trainen

## 4. Diensten van derden

Abba is afhankelijk van een klein aantal vertrouwde diensten om te functioneren.

| Dienst | Doel | Verzonden gegevens | Regio |
|---|---|---|---|
| **Supabase** | Database & authenticatie | Anonieme ID, gebeden, metadata | VS / EU |
| **Google Gemini API** | AI-analyse van gebeden | Alleen gebedstekst | Google Cloud |
| **RevenueCat** | Abonnementsbeheer | Anonieme ID, aankoopbewijzen | VS |
| **Sentry** | Crashrapporten (PII-gemaskeerd) | Foutsporen zonder e-mails, lange transcripties, JWT's verwijderd | VS / EU |
| **Firebase Cloud Messaging** | Pushnotificaties (optioneel) | FCM-token | Google Cloud |
| **Apple Sign-In / Google Sign-In** | Optionele accountkoppeling | E-mail, provider-ID | Apple / Google |

**Google Gemini:** Volgens Google's gepubliceerde beleid voor betaald API-gebruik wordt gebedsinhoud die naar Gemini wordt verzonden **niet gebruikt om Google's AI-modellen te trainen**. Verwerking is tijdelijk.

**Sentry PII-maskering:** We passen maskeringsregels toe vóór het verzenden van crashrapporten — e-mails, Koreaanse transcripties van meer dan 50 tekens, JWT's en andere identifiers worden verwijderd.

## 5. Gegevensopslag en beveiliging

- Alle gegevens in transit zijn versleuteld via HTTPS (TLS 1.2+).
- Gegevens in rust zijn beschermd door de encryptie van onze databaseprovider.
- **Row-Level Security (RLS)** in Supabase zorgt ervoor dat u alleen toegang heeft tot uw eigen gegevens.
- Audiobestanden worden opgeslagen in mappen per gebruiker, met toegang gecontroleerd door uw authenticatietoken.
- Toegangstokens worden opgeslagen in iOS Secure Enclave (`flutter_secure_storage`), nooit in platte voorkeuren.

Wij bewaren uw gegevens zolang uw account actief is. Als u uw account verwijdert, verwijderen we uw gegevens binnen **30 dagen**, behalve waar we wettelijk verplicht zijn gegevens te bewaren (zoals belastinggegevens voor abonnementsaankopen, die Apple/RevenueCat bewaren volgens hun eigen beleid).

## 6. Uw rechten

U heeft de volgende rechten met betrekking tot uw persoonsgegevens:

- **Inzage** — een kopie van de gegevens die wij over u bewaren opvragen
- **Rectificatie** — ons verzoeken onjuiste informatie te corrigeren
- **Verwijdering** — ons verzoeken uw account en gegevens te verwijderen (beschikbaar in de app: Instellingen → Account → Account verwijderen, of per e-mail)
- **Overdraagbaarheid** — een export van uw gegevens in machinaal leesbaar formaat opvragen
- **Bezwaar** — bezwaar maken tegen bepaalde verwerking
- **Toestemming intrekken** — u kunt toestemming voor pushnotificaties, AI-verwerking of accountkoppeling op elk moment intrekken

Voor inwoners onder de AVG (EU) en CCPA (Californië) zijn deze rechten wettelijk gegarandeerd. Om een recht uit te oefenen, stuur een e-mail naar **rrallvv@gmail.com**. Wij reageren binnen 30 dagen.

## 7. Privacy van kinderen

Abba heeft een 4+-rating in de App Store. Wij verzamelen niet bewust informatie van kinderen onder de 13 jaar (COPPA) of onder de 16 jaar (AVG, in sommige EU-landen) zonder verifieerbare ouderlijke toestemming. Als u denkt dat een kind persoonsgegevens heeft verstrekt, neem dan contact met ons op en wij zullen deze onmiddellijk verwijderen.

## 8. Internationale gegevensoverdrachten

Onze infrastructuur wordt gehost in de Verenigde Staten en de Europese Unie. Door Abba te gebruiken, stemt u in met de overdracht en verwerking van uw gegevens in deze regio's. Wij steunen waar nodig op Standaardcontractbepalingen (SCC's).

## 9. Overheids- en juridische verzoeken

Wij verstrekken gebruikersgegevens alleen wanneer wettelijk verplicht (geldige dagvaarding, gerechtelijk bevel of gelijkwaardig). Wij publiceren nog geen transparantierapport, maar verplichten ons ertoe getroffen gebruikers op de hoogte te stellen wanneer dit wettelijk is toegestaan.

## 10. Wijzigingen in dit beleid

Wij kunnen dit Privacybeleid bijwerken naarmate Abba evolueert. Bij substantiële wijzigingen zullen we u in de app op de hoogte stellen en de datum "Laatst bijgewerkt" bovenaan actualiseren. Voortgezet gebruik van Abba na wijzigingen betekent dat u het bijgewerkte beleid aanvaardt.

## 11. Contact

Vragen, verzoeken of klachten?

- **E-mail:** rrallvv@gmail.com
- **Reactietijd:** binnen 30 dagen (meestal eerder)

U heeft ook het recht om een klacht in te dienen bij uw lokale gegevensbeschermingsautoriteit (bijv. de Autoriteit Persoonsgegevens in Nederland, de DPA van uw EU-lidstaat, de California Attorney General of Korea's PIPC).

---

⚠️ **Vertaalmelding**: Dit is een vertaling die voor uw gemak wordt verstrekt. In geval van tegenstrijdigheid is de [Engelse versie](../privacy.html) doorslaggevend.
