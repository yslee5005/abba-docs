---
layout: default
title: Datenschutzerklärung — Abba
---

# Datenschutzerklärung

**Letzte Aktualisierung: 22. April 2026**

## 1. Einleitung

Abba („wir", „unser", „die App") ist eine mobile Gebets- und Stille-Zeit-Begleiter-App für Christen, die tiefer beten möchten. Diese Datenschutzerklärung beschreibt, wie Abba Ihre Informationen erhebt, verwendet, speichert und schützt, wenn Sie die iOS-App nutzen (Bundle-ID: `com.ystech.abba`).

Abba wird derzeit als unabhängiges Entwicklerprojekt betrieben. Wenn wir in dieser Richtlinie von „wir" sprechen, meinen wir das Abba-Team. Sollte Abba in Zukunft ein eingetragenes Unternehmen werden, wird diese Richtlinie entsprechend aktualisiert.

Diese Richtlinie gilt weltweit. Wir halten uns an die Grundsätze der EU-Datenschutz-Grundverordnung (DSGVO), des California Consumer Privacy Act (CCPA) und des koreanischen Datenschutzgesetzes (PIPA), soweit anwendbar.

## 2. Welche Informationen wir erheben

### 2.1 Kontoinformationen
Abba ist **anonym-first**. Wenn Sie die App zum ersten Mal öffnen, erstellen wir eine anonyme Benutzer-ID (UUID), damit Ihre Gebete und Einstellungen über Sitzungen hinweg synchronisiert werden können. Sie müssen keinen Namen, keine E-Mail-Adresse und keine Telefonnummer angeben, um Abba zu nutzen.

Sie können sich optional mit **Apple Sign-In** oder **Google Sign-In** anmelden, um Ihre Daten zu sichern. In diesem Fall erhalten wir Ihre E-Mail-Adresse und eine eindeutige Kennung von Apple oder Google. Mit Apple Sign-In können Sie auf Wunsch „Meine E-Mail verbergen" verwenden.

### 2.2 Gebetsinhalte (Kerndaten)
Bei der Nutzung von Abba erheben wir:
- **Audioaufnahmen** Ihrer gesprochenen Gebete
- **Transkripte**, die aus diesen Aufnahmen erstellt werden
- **Meditationstexte und Reflexionen**, die Sie schreiben oder generieren
- **Bibelstellen**, die Sie als Lesezeichen speichern

Dies sind die sensibelsten Daten, die Abba verarbeitet, und wir behandeln sie mit Sorgfalt. Ihre Audiodateien werden in Ihrem eigenen privaten Ordner auf unserem sicheren Speicher abgelegt. Nur Sie haben Zugriff darauf. Wir hören sie nicht ab, geben sie nicht weiter und nutzen sie nicht für Marketingzwecke.

### 2.3 Abonnement-Informationen
Wenn Sie Abba Pro abonnieren, zeichnet ein Drittanbieter namens **RevenueCat** Ihren Abonnementstatus (aktiv, abgelaufen, Testphase usw.) zusammen mit der anonymen ID auf. Wir erhalten Ihre Kreditkartennummer **nicht** — diese bleibt bei Apple.

### 2.4 Technische Informationen
- Gerätesprache (zur Festlegung Ihrer Standard-App-Sprache)
- Absturzprotokolle mit maskierten personenbezogenen Daten (über Sentry)
- Push-Benachrichtigungs-Token (FCM, optional — nur wenn Sie Benachrichtigungen aktivieren)
- App-Version und iOS-Version (zur Fehlersuche)

## 3. Wie wir Ihre Informationen verwenden

Wir verwenden Ihre Informationen, um:
- **KI-Analysen** Ihrer Gebete und Stille-Zeit-Reflexionen bereitzustellen (Google Gemini)
- **Ihre Daten zu synchronisieren** über Sitzungen und Geräte hinweg
- **Ihr Abonnement zu verwalten** und Berechtigungen zu prüfen
- **Fehler zu beheben und die App zu verbessern** durch Absturzberichte
- **Optionale Push-Benachrichtigungen** zu senden (tägliche Stille-Zeit-Erinnerungen), wenn Sie zustimmen

Wir tun **nicht**:
- Werbung jeglicher Art anzeigen
- Ihre Daten an Dritte verkaufen
- Ihre Gebetsinhalte an Dritte weitergeben (außer der unten beschriebenen KI-Verarbeitung)
- Ihre Inhalte zum Training von KI-Modellen verwenden

## 4. Dienste von Drittanbietern

Abba stützt sich auf eine kleine Anzahl vertrauenswürdiger Dienste, um zu funktionieren.

| Dienst | Zweck | Gesendete Daten | Region |
|---|---|---|---|
| **Supabase** | Datenbank & Authentifizierung | Anonyme ID, Gebete, Metadaten | USA / EU |
| **Google Gemini API** | KI-Analyse der Gebete | Nur Gebetstext | Google Cloud |
| **RevenueCat** | Abonnementverwaltung | Anonyme ID, Kaufbelege | USA |
| **Sentry** | Absturzberichte (PII-maskiert) | Fehlerprotokolle ohne E-Mails, lange Transkripte, JWTs | USA / EU |
| **Firebase Cloud Messaging** | Push-Benachrichtigungen (optional) | FCM-Token | Google Cloud |
| **Apple Sign-In / Google Sign-In** | Optionale Kontoverknüpfung | E-Mail, Anbieter-ID | Apple / Google |

**Google Gemini:** Gemäß Googles veröffentlichter Richtlinie für kostenpflichtige API-Nutzung werden an Gemini gesendete Gebetsinhalte **nicht zum Training von Googles KI-Modellen verwendet**. Die Verarbeitung erfolgt vorübergehend.

**Sentry-PII-Maskierung:** Wir wenden Maskierungsregeln an, bevor Absturzberichte gesendet werden — E-Mails, koreanische Transkripte mit mehr als 50 Zeichen, JWTs und andere Kennungen werden entfernt.

## 5. Datenspeicherung und Sicherheit

- Alle übertragenen Daten werden über HTTPS (TLS 1.2+) verschlüsselt.
- Ruhende Daten sind durch die Verschlüsselung unseres Datenbankanbieters geschützt.
- **Row-Level Security (RLS)** in Supabase stellt sicher, dass Sie nur auf Ihre eigenen Daten zugreifen können.
- Audiodateien werden in benutzerspezifischen Ordnern gespeichert, deren Zugriff durch Ihr Authentifizierungstoken kontrolliert wird.
- Zugriffstokens werden in der iOS Secure Enclave (`flutter_secure_storage`) gespeichert, niemals in einfachen Einstellungen.

Wir bewahren Ihre Daten auf, solange Ihr Konto aktiv ist. Wenn Sie Ihr Konto löschen, entfernen wir Ihre Daten innerhalb von **30 Tagen**, außer wenn wir gesetzlich verpflichtet sind, Aufzeichnungen aufzubewahren (z. B. Steuerunterlagen für Abonnementkäufe, die Apple/RevenueCat gemäß ihren eigenen Richtlinien aufbewahren).

## 6. Ihre Rechte

Sie haben die folgenden Rechte bezüglich Ihrer personenbezogenen Daten:

- **Auskunft** — eine Kopie der von uns gespeicherten Daten anfordern
- **Berichtigung** — uns bitten, unrichtige Informationen zu korrigieren
- **Löschung** — uns bitten, Ihr Konto und Ihre Daten zu löschen (in der App verfügbar: Einstellungen → Konto → Konto löschen, oder per E-Mail)
- **Übertragbarkeit** — einen Export Ihrer Daten in einem maschinenlesbaren Format anfordern
- **Widerspruch** — bestimmter Verarbeitung widersprechen
- **Widerruf der Einwilligung** — Sie können Ihre Einwilligung für Push-Benachrichtigungen, KI-Verarbeitung oder Kontoverknüpfung jederzeit widerrufen

Für DSGVO- (EU) und CCPA-Bürger (Kalifornien) sind diese Rechte gesetzlich garantiert. Um ein Recht auszuüben, senden Sie eine E-Mail an **rrallvv@gmail.com**. Wir antworten innerhalb von 30 Tagen.

## 7. Datenschutz für Kinder

Abba ist im App Store mit 4+ bewertet. Wir erheben wissentlich keine Informationen von Kindern unter 13 Jahren (COPPA) oder unter 16 Jahren (DSGVO, in einigen EU-Ländern) ohne nachprüfbare elterliche Zustimmung. Wenn Sie glauben, dass ein Kind personenbezogene Daten bereitgestellt hat, kontaktieren Sie uns bitte, und wir werden diese umgehend löschen.

## 8. Internationale Datenübermittlungen

Unsere Infrastruktur wird in den Vereinigten Staaten und der Europäischen Union gehostet. Durch die Nutzung von Abba stimmen Sie der Übertragung und Verarbeitung Ihrer Daten in diesen Regionen zu. Wir stützen uns, wo erforderlich, auf Standardvertragsklauseln (SCCs).

## 9. Behörden- und Rechtsanfragen

Wir geben Nutzerdaten nur dann preis, wenn wir gesetzlich dazu verpflichtet sind (gültige Vorladung, gerichtliche Anordnung oder Äquivalent). Wir veröffentlichen noch keinen Transparenzbericht, verpflichten uns jedoch, betroffene Nutzer zu benachrichtigen, sofern dies gesetzlich zulässig ist.

## 10. Änderungen dieser Richtlinie

Wir können diese Datenschutzerklärung aktualisieren, wenn sich Abba weiterentwickelt. Bei wesentlichen Änderungen werden wir Sie in der App benachrichtigen und das Datum „Letzte Aktualisierung" oben aktualisieren. Die fortgesetzte Nutzung von Abba nach Änderungen bedeutet, dass Sie die aktualisierte Richtlinie akzeptieren.

## 11. Kontakt

Fragen, Anfragen oder Beschwerden?

- **E-Mail:** rrallvv@gmail.com
- **Antwortzeit:** innerhalb von 30 Tagen (meist früher)

Sie haben auch das Recht, eine Beschwerde bei Ihrer lokalen Datenschutzbehörde einzureichen (z. B. Ihrer DPA des EU-Mitgliedstaats, dem kalifornischen Generalstaatsanwalt oder der koreanischen PIPC).

---

⚠️ **Übersetzungshinweis**: Dies ist eine Übersetzung, die zu Informationszwecken bereitgestellt wird. Bei Abweichungen ist die [englische Fassung](../privacy.html) maßgeblich.
