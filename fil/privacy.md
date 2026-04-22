---
layout: default
title: Patakaran sa Privacy — Abba
---

# Patakaran sa Privacy

**Huling Na-update: Abril 22, 2026**

## 1. Panimula

Ang Abba ("kami", "aming app", "ang app") ay isang mobile na kasama sa panalangin at Quiet Time na ginawa para sa mga Kristiyano na nais manalangin nang mas malalim. Inilalarawan ng Patakaran sa Privacy na ito kung paano kinokolekta, ginagamit, iniimbak, at pinoprotektahan ng Abba ang iyong impormasyon kapag ginamit mo ang iOS app (Bundle ID: `com.ystech.abba`).

Ang Abba ay kasalukuyang pinapatakbo bilang independent developer project. Kapag tinutukoy namin ang "kami" sa patakarang ito, ang ibig naming sabihin ay ang Abba team. Kung magiging rehistradong kumpanya ang Abba sa hinaharap, ang patakarang ito ay ia-update nang naaayon.

Ang patakarang ito ay nalalapat sa buong mundo. Sinusunod namin ang mga prinsipyo ng EU General Data Protection Regulation (GDPR), California Consumer Privacy Act (CCPA), at Korean Personal Information Protection Act (PIPA) kung naaangkop. Para sa mga gumagamit sa Pilipinas, isinasaalang-alang namin ang diwa ng Data Privacy Act of 2012 (RA 10173).

## 2. Impormasyong Kinokolekta Namin

### 2.1 Impormasyon ng Account
Ang Abba ay **anonymous-first**. Kapag binuksan mo ang app sa unang pagkakataon, gumagawa kami ng anonymous user ID (UUID) upang maisync ang iyong mga panalangin at setting sa mga session. Hindi mo kailangang magbigay ng pangalan, email, o numero ng telepono upang gamitin ang Abba.

Maaari mong opsyonal na mag-sign in gamit ang **Apple Sign-In** o **Google Sign-In** upang mag-backup ng iyong data. Sa kasong iyon, natatanggap namin ang iyong email address at isang natatanging identifier mula sa Apple o Google. Maaari mong gamitin ang "Hide My Email" sa Apple Sign-In kung gusto mo.

### 2.2 Nilalaman ng Panalangin (Core Data)
Kapag ginamit mo ang Abba, kinokolekta namin ang:
- **Mga audio recording** ng iyong binibigkas na mga panalangin
- **Mga transcript** na nabuo mula sa mga recording na iyon
- **Mga teksto at pagninilay** na isinulat o nabuo mo
- **Mga talata sa Banal na Kasulatan** na na-bookmark mo

Ito ang pinakasensitibong data na hinahawakan ng Abba, at tinatrato namin ito nang maingat. Ang iyong audio ay iniimbak sa iyong sariling pribadong folder sa aming secure na storage. Ikaw lang ang may access. Hindi namin ito pinakikinggan, ibinabahagi, o ginagamit para sa marketing.

### 2.3 Impormasyon ng Subscription
Kung nag-subscribe ka sa Abba Pro, isang third-party service na tinatawag na **RevenueCat** ang nagtatala ng iyong subscription status (active, expired, trial, atbp.) kasama ang anonymous ID. **Hindi** namin natatanggap ang numero ng iyong credit card — nananatili iyon sa Apple.

### 2.4 Teknikal na Impormasyon
- Wika ng device (para itakda ang default na wika ng app)
- Mga crash log na may naka-mask na personal data (sa pamamagitan ng Sentry)
- Push notification token (FCM, opsyonal — kung pinagana mo ang mga notification)
- Bersyon ng app at bersyon ng iOS (para sa debugging)

## 3. Paano Namin Ginagamit ang Iyong Impormasyon

Ginagamit namin ang iyong impormasyon upang:
- **Magbigay ng AI analysis** ng iyong mga panalangin at Quiet Time na pagninilay (Google Gemini)
- **Mag-sync ng iyong data** sa mga session at device
- **Pamahalaan ang iyong subscription** at mga entitlement
- **Ayusin ang mga bug at pagbutihin ang app** sa pamamagitan ng mga crash report
- **Magpadala ng opsyonal na push notification** (pang-araw-araw na Quiet Time reminder) kung nag-opt in ka

**Hindi** kami:
- Nagpapakita ng anumang uri ng advertising
- Nagbebenta ng iyong data sa sinuman
- Nagbabahagi ng iyong prayer content sa mga third party (maliban sa AI processing na inilarawan sa ibaba)
- Gumagamit ng iyong content upang sanayin ang mga AI model

## 4. Mga Third-Party Service

Umaasa ang Abba sa maliit na bilang ng mga pinagkakatiwalaang serbisyo upang mag-operate.

| Serbisyo | Layunin | Datos na Ipinadala | Rehiyon |
|---|---|---|---|
| **Supabase** | Database at authentication | Anonymous ID, panalangin, metadata | US / EU |
| **Google Gemini API** | AI analysis ng panalangin | Teksto lang ng panalangin | Google Cloud |
| **RevenueCat** | Pamamahala ng subscription | Anonymous ID, mga resibo ng pagbili | US |
| **Sentry** | Pag-uulat ng crash (naka-mask ang PII) | Mga error trace na may inalis na email, mahabang transcript, JWT | US / EU |
| **Firebase Cloud Messaging** | Push notification (opsyonal) | FCM token | Google Cloud |
| **Apple Sign-In / Google Sign-In** | Opsyonal na account link | Email, provider ID | Apple / Google |

**Google Gemini:** Ayon sa inilathalang patakaran ng Google para sa paid API usage, ang prayer content na ipinadala sa Gemini ay **hindi ginagamit upang sanayin ang mga AI model ng Google**. Ang processing ay pansamantala.

**Sentry PII masking:** Naglalapat kami ng mga masking rule bago magpadala ng crash reports — ang mga email, mahabang transcript na higit sa 50 karakter, JWTs, at iba pang identifier ay inalis.

## 5. Pag-iimbak ng Data at Seguridad

- Lahat ng data na nasa transit ay naka-encrypt sa pamamagitan ng HTTPS (TLS 1.2+).
- Ang data na nasa rest ay pinoprotektahan ng encryption ng aming database provider.
- Tinitiyak ng **Row-Level Security (RLS)** sa Supabase na ikaw lang ang maaaring mag-access ng sarili mong data.
- Ang mga audio file ay iniimbak sa mga per-user folder na may access na kinokontrol ng iyong authentication token.
- Ang mga access token ay iniimbak sa iOS Secure Enclave (`flutter_secure_storage`), hindi kailanman sa plain preferences.

Pinananatili namin ang iyong data hangga't aktibo ang iyong account. Kung tatanggalin mo ang iyong account, aalisin namin ang iyong data sa loob ng **30 araw**, maliban sa kung saan kinakailangan naming itago ang mga rekord ayon sa batas (tulad ng mga tax record para sa subscription purchases, na pinananatili ng Apple/RevenueCat ayon sa kanilang sariling mga patakaran).

## 6. Ang Iyong mga Karapatan

Mayroon kang mga sumusunod na karapatan sa iyong personal na data:

- **Access** — humiling ng kopya ng data na hawak namin tungkol sa iyo
- **Correction** — hilingin sa amin na ayusin ang hindi tamang impormasyon
- **Deletion** — hilingin sa amin na tanggalin ang iyong account at data (magagamit sa app: Settings → Account → Delete Account, o sa pamamagitan ng email)
- **Portability** — humiling ng export ng iyong data sa machine-readable na format
- **Objection** — tumutol sa ilang processing
- **Withdraw consent** — maaari mong bawiin ang consent para sa mga push notification, AI processing, o account linking anumang oras

Para sa mga residente ng GDPR (EU) at CCPA (California), ang mga karapatang ito ay garantisado ng batas. Upang gamitin ang anumang karapatan, i-email ang **rrallvv@gmail.com**. Tumutugon kami sa loob ng 30 araw.

## 7. Privacy ng Mga Bata

Ang Abba ay rated 4+ sa App Store. Hindi namin sadyang kinokolekta ang impormasyon mula sa mga batang wala pang 13 (COPPA) o wala pang 16 (GDPR, sa ilang bansa sa EU) nang walang verifiable parental consent. Kung naniniwala kang nagbigay ng personal na impormasyon ang isang bata, mangyaring makipag-ugnayan sa amin at aalisin namin ito kaagad.

## 8. International Data Transfers

Ang aming imprastraktura ay naka-host sa United States at European Union. Sa paggamit ng Abba, pumapayag ka na ma-transfer at maproseso ang iyong data sa mga rehiyong ito. Umaasa kami sa Standard Contractual Clauses (SCCs) kung kinakailangan.

## 9. Mga Kahilingan ng Gobyerno at Legal

Ibinubunyag lang namin ang data ng user kapag legal na kinakailangan (valid subpoena, court order, o katumbas). Hindi pa kami naglalathala ng transparency report, ngunit nangangako kaming ipaalam sa mga apektadong user kapag legal na pinapayagan.

## 10. Mga Pagbabago sa Patakarang Ito

Maaari naming i-update ang Patakaran sa Privacy na ito habang umuunlad ang Abba. Kapag gumawa kami ng mahahalagang pagbabago, aabisuhan ka namin sa app at i-update ang petsang "Huling Na-update" sa itaas. Ang patuloy na paggamit ng Abba pagkatapos ng mga pagbabago ay nangangahulugang tinatanggap mo ang na-update na patakaran.

## 11. Makipag-ugnayan sa Amin

Mga tanong, kahilingan, o reklamo?

- **Email:** rrallvv@gmail.com
- **Oras ng pagtugon:** sa loob ng 30 araw (kadalasan mas maaga)

Mayroon ka ring karapatang maghain ng reklamo sa iyong lokal na data protection authority (hal., DPA ng iyong EU member state, California Attorney General, o PIPC ng Korea).

---
⚠️ **Paunawa sa Pagsasalin**: Ito ay pagsasaling ibinibigay para sa kaginhawaan.
Sa kaso ng anumang pagkakaiba, ang [bersyon sa Ingles](../privacy.html) ang mananaig.
