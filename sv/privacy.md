---
layout: default
title: Integritetspolicy — Abba
---

# Integritetspolicy

**Senast uppdaterad: 22 april 2026**

## 1. Introduktion

Abba ("vi", "vår", "appen") är en mobil bön- och Stilla Tid-följeslagare (Quiet Time) skapad för kristna som vill be djupare. Denna Integritetspolicy beskriver hur Abba samlar in, använder, lagrar och skyddar din information när du använder iOS-appen (Bundle ID: `com.ystech.abba`).

Abba drivs för närvarande som ett oberoende utvecklarprojekt. När vi säger "vi" i denna policy menar vi Abba-teamet. Om Abba i framtiden blir ett registrerat företag kommer denna policy att uppdateras i enlighet därmed.

Denna policy gäller globalt. Vi följer principerna i EU:s allmänna dataskyddsförordning (GDPR), California Consumer Privacy Act (CCPA) och den koreanska Personal Information Protection Act (PIPA), där så är tillämpligt.

## 2. Information vi samlar in

### 2.1 Kontoinformation
Abba är **anonym som standard**. När du öppnar appen första gången skapar vi ett anonymt användar-ID (UUID) så att dina böner och inställningar kan synkroniseras mellan sessioner. Du behöver inte ange namn, e-post eller telefonnummer för att använda Abba.

Du kan valfritt logga in med **Apple Sign-In** eller **Google Sign-In** för att säkerhetskopiera dina data. I så fall får vi din e-postadress och en unik identifierare från Apple eller Google. Du kan använda "Dölj min e-postadress" med Apple Sign-In om du föredrar det.

### 2.2 Böneinnehåll (kärndata)
När du använder Abba samlar vi in:
- **Ljudinspelningar** av dina uttalade böner
- **Transkriberingar** genererade från dessa inspelningar
- **Meditationstext och reflektioner** som du skriver eller genererar
- **Bibelavsnitt** som du bokmärker

Detta är de mest känsliga data som Abba hanterar, och vi behandlar dem med omsorg. Ditt ljud lagras i din egen privata mapp på vår säkra lagring. Endast du kan komma åt det. Vi lyssnar inte på det, delar det inte och använder det inte för marknadsföring.

### 2.3 Prenumerationsinformation
Om du prenumererar på Abba Pro registrerar en tredjepartstjänst som heter **RevenueCat** din prenumerationsstatus (aktiv, utgången, prov, etc.) tillsammans med det anonyma ID:t. Vi tar **inte** emot ditt kreditkortsnummer — det stannar hos Apple.

### 2.4 Teknisk information
- Enhetens språk (för att ställa in ditt standardappspråk)
- Kraschloggar med maskerade personuppgifter (via Sentry)
- Push-meddelandetoken (FCM, valfritt — endast om du aktiverar aviseringar)
- App-version och iOS-version (för felsökning)

## 3. Hur vi använder din information

Vi använder din information för att:
- **Tillhandahålla AI-analys** av dina böner och Stilla Tid-reflektioner (Google Gemini)
- **Synkronisera dina data** över sessioner och enheter
- **Hantera din prenumeration** och rättigheter
- **Åtgärda buggar och förbättra appen** genom kraschrapporter
- **Skicka valfria push-aviseringar** (dagliga Stilla Tid-påminnelser) om du samtycker

Vi **gör inte**:
- Visar annonser av något slag
- Säljer dina data till någon
- Delar ditt böneinnehåll med tredje part (utom AI-bearbetningen som beskrivs nedan)
- Använder ditt innehåll för att träna AI-modeller

## 4. Tredjepartstjänster

Abba förlitar sig på ett litet antal betrodda tjänster för att fungera.

| Tjänst | Syfte | Skickad data | Region |
|---|---|---|---|
| **Supabase** | Databas och autentisering | Anonymt ID, böner, metadata | USA / EU |
| **Google Gemini API** | AI-analys av böner | Endast bönetext | Google Cloud |
| **RevenueCat** | Prenumerationshantering | Anonymt ID, köpkvitton | USA |
| **Sentry** | Kraschrapporter (PII-maskerade) | Felspår utan e-post, långa transkriberingar, JWT borttagna | USA / EU |
| **Firebase Cloud Messaging** | Push-aviseringar (valfritt) | FCM-token | Google Cloud |
| **Apple Sign-In / Google Sign-In** | Valfri kontokoppling | E-post, leverantörs-ID | Apple / Google |

**Google Gemini:** Enligt Googles publicerade policy för betald API-användning används böneinnehåll som skickas till Gemini **inte för att träna Googles AI-modeller**. Bearbetningen är tillfällig.

**Sentry PII-maskering:** Vi tillämpar maskeringsregler innan kraschrapporter skickas — e-post, koreanska transkriberingar längre än 50 tecken, JWT och andra identifierare tas bort.

## 5. Datalagring och säkerhet

- All data under överföring är krypterad via HTTPS (TLS 1.2+).
- Data i vila skyddas av vår databasleverantörs kryptering.
- **Row-Level Security (RLS)** i Supabase säkerställer att du endast kan komma åt dina egna data.
- Ljudfiler lagras i mappar per användare med åtkomst som kontrolleras av din autentiseringstoken.
- Åtkomsttokens lagras i iOS Secure Enclave (`flutter_secure_storage`), aldrig i vanliga inställningar.

Vi behåller dina data så länge ditt konto är aktivt. Om du raderar ditt konto tar vi bort dina data inom **30 dagar**, förutom där vi är juridiskt skyldiga att behålla uppgifter (såsom skatteuppgifter för prenumerationsköp, som Apple/RevenueCat behåller enligt sina egna policyer).

## 6. Dina rättigheter

Du har följande rättigheter över dina personuppgifter:

- **Tillgång** — begära en kopia av de data vi har om dig
- **Rättelse** — be oss rätta felaktig information
- **Radering** — be oss radera ditt konto och data (tillgängligt i appen: Inställningar → Konto → Radera konto, eller via e-post)
- **Överförbarhet** — begära en export av dina data i maskinläsbart format
- **Invändning** — invända mot viss behandling
- **Återkalla samtycke** — du kan när som helst återkalla samtycke för push-aviseringar, AI-bearbetning eller kontokoppling

För GDPR- (EU) och CCPA-invånare (Kalifornien) är dessa rättigheter garanterade enligt lag. För att utöva en rättighet, skicka ett e-postmeddelande till **rrallvv@gmail.com**. Vi svarar inom 30 dagar.

## 7. Barns integritet

Abba är klassad 4+ i App Store. Vi samlar inte medvetet in information från barn under 13 år (COPPA) eller under 16 år (GDPR, i vissa EU-länder) utan verifierbart föräldrasamtycke. Om du tror att ett barn har lämnat personuppgifter, vänligen kontakta oss och vi tar bort dem omedelbart.

## 8. Internationella dataöverföringar

Vår infrastruktur är värd i USA och Europeiska unionen. Genom att använda Abba samtycker du till att dina data överförs till och bearbetas i dessa regioner. Vi förlitar oss på standardavtalsklausuler (SCC) där det krävs.

## 9. Regerings- och juridiska förfrågningar

Vi avslöjar endast användardata när det krävs enligt lag (giltig stämning, domstolsbeslut eller motsvarande). Vi publicerar ännu ingen transparensrapport, men vi förbinder oss att meddela berörda användare när lagen tillåter det.

## 10. Ändringar i denna policy

Vi kan uppdatera denna Integritetspolicy i takt med att Abba utvecklas. Vid väsentliga ändringar kommer vi att meddela dig i appen och uppdatera datumet "Senast uppdaterad" högst upp. Fortsatt användning av Abba efter ändringar innebär att du accepterar den uppdaterade policyn.

## 11. Kontakta oss

Frågor, förfrågningar eller klagomål?

- **E-post:** rrallvv@gmail.com
- **Svarstid:** inom 30 dagar (vanligtvis tidigare)

Du har också rätt att lämna in ett klagomål till din lokala dataskyddsmyndighet (t.ex. IMY i Sverige, DPA i din EU-medlemsstat, Californiens Attorney General eller Koreas PIPC).

---

⚠️ **Översättningsmeddelande**: Detta är en översättning som tillhandahålls för bekvämlighet. Vid avvikelser gäller den [engelska versionen](../privacy.html).
