---
layout: default
title: Politica de Confidențialitate — Abba
---

# Politica de Confidențialitate

**Ultima actualizare: 22 aprilie 2026**

## 1. Introducere

Abba („noi", „al nostru", „aplicația") este un însoțitor mobil de rugăciune și Timp Liniștit (Quiet Time) creat pentru creștinii care doresc să se roage mai profund. Această Politică de Confidențialitate descrie modul în care Abba colectează, utilizează, stochează și protejează informațiile dvs. atunci când utilizați aplicația iOS (Bundle ID: `com.ystech.abba`).

Abba este operată în prezent ca un proiect independent de dezvoltator. Când ne referim la „noi" în această politică, ne referim la echipa Abba. Dacă Abba devine o companie înregistrată în viitor, această politică va fi actualizată în consecință.

Această politică se aplică la nivel mondial. Urmăm principiile Regulamentului General privind Protecția Datelor al UE (GDPR), California Consumer Privacy Act (CCPA) și legii coreene privind protecția informațiilor personale (PIPA), acolo unde este aplicabil.

## 2. Informațiile pe care le colectăm

### 2.1 Informații despre cont
Abba este **anonimă în mod implicit**. Când deschideți aplicația pentru prima dată, creăm un ID de utilizator anonim (UUID), astfel încât rugăciunile și setările dvs. să se poată sincroniza între sesiuni. Nu trebuie să furnizați un nume, e-mail sau număr de telefon pentru a utiliza Abba.

Puteți opțional să vă conectați cu **Apple Sign-In** sau **Google Sign-In** pentru a face backup datelor dvs. În acest caz, primim adresa dvs. de e-mail și un identificator unic de la Apple sau Google. Puteți utiliza „Ascunde adresa mea de e-mail" cu Apple Sign-In dacă preferați.

### 2.2 Conținutul rugăciunii (date de bază)
Când utilizați Abba, colectăm:
- **Înregistrări audio** ale rugăciunilor dvs. rostite
- **Transcrieri** generate din aceste înregistrări
- **Texte de meditație și reflecții** pe care le scrieți sau generați
- **Pasaje biblice** pe care le marcați ca favorite

Acestea sunt cele mai sensibile date pe care le gestionează Abba și le tratăm cu grijă. Audio-ul dvs. este stocat în propriul folder privat pe stocarea noastră sigură. Numai dvs. puteți accesa. Nu îl ascultăm, nu îl partajăm și nu îl folosim pentru marketing.

### 2.3 Informații despre abonament
Dacă vă abonați la Abba Pro, un serviciu terț numit **RevenueCat** înregistrează starea abonamentului dvs. (activ, expirat, încercare etc.) împreună cu ID-ul anonim. **Nu** primim numărul cardului dvs. de credit — acesta rămâne la Apple.

### 2.4 Informații tehnice
- Limba dispozitivului (pentru a seta limba implicită a aplicației)
- Jurnale de erori cu date personale mascate (prin Sentry)
- Token pentru notificări push (FCM, opțional — numai dacă activați notificările)
- Versiunea aplicației și versiunea iOS (pentru depanare)

## 3. Cum folosim informațiile dvs.

Folosim informațiile dvs. pentru:
- **Furnizarea analizei AI** a rugăciunilor și reflecțiilor dvs. de Timp Liniștit (Google Gemini)
- **Sincronizarea datelor dvs.** între sesiuni și dispozitive
- **Gestionarea abonamentului dvs.** și a drepturilor
- **Remedierea erorilor și îmbunătățirea aplicației** prin rapoarte de eroare
- **Trimiterea notificărilor push opționale** (memento-uri zilnice pentru Timp Liniștit) dacă sunteți de acord

**Nu**:
- Afișăm reclame de niciun fel
- Vindem datele dvs. nimănui
- Partajăm conținutul rugăciunilor cu terți (cu excepția procesării AI descrise mai jos)
- Folosim conținutul dvs. pentru a antrena modele AI

## 4. Servicii ale terților

Abba se bazează pe un număr mic de servicii de încredere pentru a funcționa.

| Serviciu | Scop | Date trimise | Regiune |
|---|---|---|---|
| **Supabase** | Bază de date și autentificare | ID anonim, rugăciuni, metadate | SUA / UE |
| **Google Gemini API** | Analiza AI a rugăciunilor | Numai text rugăciune | Google Cloud |
| **RevenueCat** | Gestionarea abonamentelor | ID anonim, chitanțe de cumpărare | SUA |
| **Sentry** | Rapoarte de eroare (PII mascat) | Urme de eroare fără e-mailuri, transcrieri lungi, JWT eliminate | SUA / UE |
| **Firebase Cloud Messaging** | Notificări push (opțional) | Token FCM | Google Cloud |
| **Apple Sign-In / Google Sign-In** | Conectare cont opțională | E-mail, ID furnizor | Apple / Google |

**Google Gemini:** Conform politicii publicate de Google pentru utilizarea plătită a API-ului, conținutul rugăciunilor trimis către Gemini **nu este folosit pentru antrenarea modelelor AI Google**. Procesarea este temporară.

**Mascarea PII Sentry:** Aplicăm reguli de mascare înainte de trimiterea rapoartelor de eroare — e-mailurile, transcrierile coreene mai lungi de 50 de caractere, JWT-urile și alți identificatori sunt eliminați.

## 5. Stocarea și securitatea datelor

- Toate datele în tranzit sunt criptate prin HTTPS (TLS 1.2+).
- Datele în repaus sunt protejate de criptarea furnizorului nostru de baze de date.
- **Row-Level Security (RLS)** în Supabase asigură că puteți accesa doar propriile date.
- Fișierele audio sunt stocate în foldere pe utilizator, cu acces controlat de tokenul dvs. de autentificare.
- Token-urile de acces sunt stocate în iOS Secure Enclave (`flutter_secure_storage`), niciodată în preferințe simple.

Păstrăm datele dvs. atâta timp cât contul dvs. este activ. Dacă vă ștergeți contul, eliminăm datele dvs. în termen de **30 de zile**, cu excepția cazurilor în care suntem obligați legal să păstrăm înregistrări (cum ar fi înregistrările fiscale pentru achizițiile de abonamente, pe care Apple/RevenueCat le păstrează conform propriilor politici).

## 6. Drepturile dvs.

Aveți următoarele drepturi asupra datelor dvs. personale:

- **Acces** — să solicitați o copie a datelor pe care le deținem despre dvs.
- **Rectificare** — să ne cereți să corectăm informații inexacte
- **Ștergere** — să ne cereți să vă ștergem contul și datele (disponibil în aplicație: Setări → Cont → Ștergere cont, sau prin e-mail)
- **Portabilitate** — să solicitați un export al datelor dvs. într-un format care poate fi citit de mașină
- **Opoziție** — să vă opuneți anumitor procesări
- **Retragerea consimțământului** — puteți revoca consimțământul pentru notificări push, procesare AI sau conectare cont în orice moment

Pentru rezidenții GDPR (UE) și CCPA (California), aceste drepturi sunt garantate prin lege. Pentru a exercita orice drept, trimiteți un e-mail la **rrallvv@gmail.com**. Răspundem în termen de 30 de zile.

## 7. Confidențialitatea copiilor

Abba are evaluarea 4+ în App Store. Nu colectăm cu bună știință informații de la copii sub 13 ani (COPPA) sau sub 16 ani (GDPR, în unele țări UE) fără consimțământul parental verificabil. Dacă credeți că un copil a furnizat informații personale, contactați-ne și le vom șterge imediat.

## 8. Transferuri internaționale de date

Infrastructura noastră este găzduită în Statele Unite și Uniunea Europeană. Prin utilizarea Abba, consimțiți la transferul și procesarea datelor dvs. în aceste regiuni. Ne bazăm pe clauzele contractuale standard (SCC) acolo unde este necesar.

## 9. Solicitări guvernamentale și legale

Divulgăm datele utilizatorilor doar atunci când este cerut prin lege (citație validă, ordin judecătoresc sau echivalent). Nu publicăm încă un raport de transparență, dar ne angajăm să notificăm utilizatorii afectați atunci când legea permite.

## 10. Modificări ale acestei politici

Putem actualiza această Politică de Confidențialitate pe măsură ce Abba evoluează. Când facem modificări semnificative, vă vom notifica în aplicație și vom actualiza data „Ultima actualizare" din partea de sus. Utilizarea continuă a Abba după modificări înseamnă că acceptați politica actualizată.

## 11. Contactați-ne

Întrebări, solicitări sau reclamații?

- **E-mail:** rrallvv@gmail.com
- **Timp de răspuns:** în termen de 30 de zile (de obicei mai devreme)

Aveți, de asemenea, dreptul de a depune o plângere la autoritatea locală de protecție a datelor (de exemplu, ANSPDCP în România, DPA al statului membru UE, Procurorul General din California sau PIPC din Coreea).

---

⚠️ **Notă de traducere**: Aceasta este o traducere oferită pentru comoditate. În caz de discrepanță, prevalează [versiunea în limba engleză](../privacy.html).
