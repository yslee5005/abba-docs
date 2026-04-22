---
layout: default
title: Informativa sulla Privacy — Abba
---

# Informativa sulla Privacy

**Ultimo aggiornamento: 22 aprile 2026**

## 1. Introduzione

Abba («noi», «nostro», «l'app») è un compagno mobile di preghiera e Tempo di Silenzio (Quiet Time) creato per i cristiani che desiderano pregare più profondamente. Questa Informativa sulla Privacy descrive come Abba raccoglie, utilizza, conserva e protegge le tue informazioni quando utilizzi l'app iOS (Bundle ID: `com.ystech.abba`).

Abba è attualmente gestito come progetto di sviluppatore indipendente. Quando facciamo riferimento a «noi» in questa informativa, intendiamo il team di Abba. Se Abba dovesse diventare un'azienda registrata in futuro, questa informativa verrà aggiornata di conseguenza.

Questa informativa si applica a livello mondiale. Seguiamo i principi del Regolamento Generale sulla Protezione dei Dati dell'UE (GDPR), del California Consumer Privacy Act (CCPA) e della Legge coreana sulla Protezione delle Informazioni Personali (PIPA), ove applicabile.

## 2. Informazioni che raccogliamo

### 2.1 Informazioni sull'account
Abba è **anonimo per impostazione predefinita**. Quando apri l'app per la prima volta, creiamo un ID utente anonimo (UUID) in modo che le tue preghiere e impostazioni possano essere sincronizzate tra le sessioni. Non è necessario fornire un nome, un'email o un numero di telefono per utilizzare Abba.

Puoi facoltativamente accedere con **Apple Sign-In** o **Google Sign-In** per eseguire il backup dei tuoi dati. In tal caso, riceviamo il tuo indirizzo email e un identificatore univoco da Apple o Google. Se preferisci, puoi utilizzare «Nascondi la mia email» con Apple Sign-In.

### 2.2 Contenuto delle preghiere (dati principali)
Quando utilizzi Abba, raccogliamo:
- **Registrazioni audio** delle tue preghiere pronunciate
- **Trascrizioni** generate da queste registrazioni
- **Testi di meditazione e riflessioni** che scrivi o generi
- **Passi biblici** che salvi tra i preferiti

Questi sono i dati più sensibili gestiti da Abba e li trattiamo con cura. Il tuo audio è conservato in una tua cartella privata sul nostro storage sicuro. Solo tu puoi accedervi. Non lo ascoltiamo, non lo condividiamo e non lo utilizziamo per scopi di marketing.

### 2.3 Informazioni sull'abbonamento
Se ti abboni ad Abba Pro, un servizio di terze parti chiamato **RevenueCat** registra lo stato del tuo abbonamento (attivo, scaduto, prova, ecc.) insieme all'ID anonimo. **Non** riceviamo il numero della tua carta di credito — rimane con Apple.

### 2.4 Informazioni tecniche
- Lingua del dispositivo (per impostare la lingua predefinita dell'app)
- Log di crash con dati personali mascherati (tramite Sentry)
- Token di notifica push (FCM, opzionale — solo se abiliti le notifiche)
- Versione dell'app e versione iOS (per il debug)

## 3. Come utilizziamo le tue informazioni

Utilizziamo le tue informazioni per:
- **Fornire analisi AI** delle tue preghiere e riflessioni di Tempo di Silenzio (Google Gemini)
- **Sincronizzare i tuoi dati** tra sessioni e dispositivi
- **Gestire il tuo abbonamento** e i relativi diritti
- **Correggere bug e migliorare l'app** tramite i report di crash
- **Inviare notifiche push opzionali** (promemoria giornalieri di Tempo di Silenzio) se dai il consenso

**Non**:
- Mostriamo pubblicità di alcun tipo
- Vendiamo i tuoi dati a nessuno
- Condividiamo il contenuto delle tue preghiere con terzi (eccetto l'elaborazione AI descritta di seguito)
- Usiamo il tuo contenuto per addestrare modelli AI

## 4. Servizi di terze parti

Abba si basa su un piccolo numero di servizi fidati per funzionare.

| Servizio | Scopo | Dati inviati | Regione |
|---|---|---|---|
| **Supabase** | Database e autenticazione | ID anonimo, preghiere, metadati | USA / UE |
| **Google Gemini API** | Analisi AI delle preghiere | Solo testo della preghiera | Google Cloud |
| **RevenueCat** | Gestione abbonamenti | ID anonimo, ricevute di acquisto | USA |
| **Sentry** | Report di crash (PII mascherati) | Tracce di errore senza email, trascrizioni lunghe, JWT rimossi | USA / UE |
| **Firebase Cloud Messaging** | Notifiche push (opzionale) | Token FCM | Google Cloud |
| **Apple Sign-In / Google Sign-In** | Collegamento account opzionale | Email, ID fornitore | Apple / Google |

**Google Gemini:** Secondo la politica pubblicata da Google per l'uso API a pagamento, il contenuto delle preghiere inviato a Gemini **non viene utilizzato per addestrare i modelli AI di Google**. L'elaborazione è transitoria.

**Mascheramento PII Sentry:** Applichiamo regole di mascheramento prima di inviare i report di crash — email, trascrizioni coreane più lunghe di 50 caratteri, JWT e altri identificatori vengono rimossi.

## 5. Conservazione e sicurezza dei dati

- Tutti i dati in transito sono cifrati tramite HTTPS (TLS 1.2+).
- I dati a riposo sono protetti dalla cifratura del nostro provider di database.
- La **Row-Level Security (RLS)** in Supabase garantisce che tu possa accedere solo ai tuoi dati.
- I file audio sono conservati in cartelle per utente con accesso controllato dal tuo token di autenticazione.
- I token di accesso sono conservati nel Secure Enclave di iOS (`flutter_secure_storage`), mai in preferenze in chiaro.

Conserviamo i tuoi dati finché il tuo account è attivo. Se elimini il tuo account, rimuoviamo i tuoi dati entro **30 giorni**, tranne quando siamo legalmente obbligati a conservare i registri (come i registri fiscali per gli acquisti di abbonamento, che Apple/RevenueCat conservano secondo le loro politiche).

## 6. I tuoi diritti

Hai i seguenti diritti sui tuoi dati personali:

- **Accesso** — richiedere una copia dei dati che abbiamo su di te
- **Rettifica** — chiederci di correggere informazioni inesatte
- **Cancellazione** — chiederci di eliminare il tuo account e dati (disponibile nell'app: Impostazioni → Account → Elimina account, o via email)
- **Portabilità** — richiedere l'esportazione dei tuoi dati in formato leggibile da macchina
- **Opposizione** — opporti a determinati trattamenti
- **Revoca del consenso** — puoi revocare il consenso per notifiche push, elaborazione AI o collegamento account in qualsiasi momento

Per i residenti GDPR (UE) e CCPA (California), questi diritti sono garantiti per legge. Per esercitare un diritto, invia un'email a **rrallvv@gmail.com**. Rispondiamo entro 30 giorni.

## 7. Privacy dei minori

Abba è classificato 4+ nell'App Store. Non raccogliamo consapevolmente informazioni da bambini sotto i 13 anni (COPPA) o sotto i 16 anni (GDPR, in alcuni paesi UE) senza il consenso verificabile dei genitori. Se ritieni che un minore abbia fornito informazioni personali, contattaci e le elimineremo immediatamente.

## 8. Trasferimenti internazionali di dati

La nostra infrastruttura è ospitata negli Stati Uniti e nell'Unione Europea. Usando Abba, acconsenti al trasferimento e all'elaborazione dei tuoi dati in queste regioni. Ci basiamo sulle Clausole Contrattuali Standard (CCS) ove richiesto.

## 9. Richieste governative e legali

Divulghiamo i dati degli utenti solo quando richiesto dalla legge (citazione valida, ordine del tribunale o equivalente). Non pubblichiamo ancora un rapporto di trasparenza, ma ci impegniamo a notificare gli utenti interessati quando la legge lo consente.

## 10. Modifiche a questa informativa

Possiamo aggiornare questa Informativa sulla Privacy man mano che Abba evolve. Quando apportiamo modifiche sostanziali, ti avviseremo nell'app e aggiorneremo la data di «Ultimo aggiornamento» in alto. L'uso continuato di Abba dopo le modifiche significa che accetti l'informativa aggiornata.

## 11. Contattaci

Domande, richieste o reclami?

- **Email:** rrallvv@gmail.com
- **Tempo di risposta:** entro 30 giorni (di solito prima)

Hai anche il diritto di presentare un reclamo alla tua autorità locale di protezione dei dati (ad es., il Garante Privacy italiano, la DPA del tuo stato membro UE, il Procuratore Generale della California o il PIPC coreano).

---

⚠️ **Avviso di traduzione**: Questa è una traduzione fornita per comodità. In caso di discrepanza, prevarrà la [versione inglese](../privacy.html).
