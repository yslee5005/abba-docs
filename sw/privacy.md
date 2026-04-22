---
layout: default
title: Sera ya Faragha — Abba
---

# Sera ya Faragha

**Imesasishwa Mwisho: Aprili 22, 2026**

## 1. Utangulizi

Abba ("sisi", "programu yetu", "programu") ni programu ya simu ya mkononi inayoandamana katika maombi na Muda wa Kimya (Quiet Time) iliyoundwa kwa Wakristo wanaotaka kuomba kwa kina zaidi. Sera hii ya Faragha inaelezea jinsi Abba inavyokusanya, inavyotumia, inavyohifadhi, na inavyolinda taarifa zako unapotumia programu ya iOS (Bundle ID: `com.ystech.abba`).

Abba kwa sasa inaendeshwa kama mradi wa msanidi huru. Tunaposema "sisi" katika sera hii, tunamaanisha timu ya Abba. Iwapo Abba itakuwa kampuni iliyosajiliwa baadaye, sera hii itasasishwa ipasavyo.

Sera hii inatumika ulimwenguni kote. Tunafuata kanuni za Kanuni ya Ulinzi wa Data ya Jumla ya EU (GDPR), Sheria ya Faragha ya Mtumiaji ya California (CCPA), na Sheria ya Ulinzi wa Taarifa Binafsi ya Korea (PIPA) pale inapotumika.

## 2. Taarifa Tunazokusanya

### 2.1 Taarifa za Akaunti
Abba ni **ya kutokujulikana kwanza**. Unapofungua programu kwa mara ya kwanza, tunaunda kitambulisho cha mtumiaji kisichojulikana (UUID) ili maombi yako na mipangilio vifanywe ulinganifu kati ya vipindi. Hauhitaji kutoa jina, barua pepe, au nambari ya simu kutumia Abba.

Kwa hiari, unaweza kuingia kwa kutumia **Apple Sign-In** au **Google Sign-In** ili kuhifadhi nakala ya data yako. Katika kesi hiyo, tunapata anwani yako ya barua pepe na kitambulisho cha kipekee kutoka kwa Apple au Google. Unaweza kutumia "Ficha Barua Pepe Yangu" na Apple Sign-In ikiwa unapendelea.

### 2.2 Maudhui ya Maombi (Data Muhimu)
Unapotumia Abba, tunakusanya:
- **Rekodi za sauti** za maombi yako yaliyoongelewa
- **Nakala za maandishi** zilizozalishwa kutoka kwa rekodi hizo
- **Maandishi ya tafakari na mawazo** unayoandika au kuyazalisha
- **Vifungu vya Maandiko** unavyoweka alama

Hii ni data nyeti zaidi ambayo Abba inashughulikia, na tunaishughulikia kwa uangalifu. Sauti yako inahifadhiwa kwenye folda yako binafsi kwenye hifadhi yetu salama. Ni wewe pekee unaweza kuipata. Hatuisikilizi, hatuishiriki, na hatuitumii kwa uuzaji.

### 2.3 Taarifa za Usajili
Ikiwa utajisajili kwa Abba Pro, huduma ya tatu iitwayo **RevenueCat** inarekodi hali ya usajili wako (hai, imekwisha, jaribio, nk.) pamoja na kitambulisho kisichojulikana. **Hatupati** nambari ya kadi yako ya mkopo — inabaki na Apple.

### 2.4 Taarifa za Kiufundi
- Lugha ya kifaa (kuweka lugha chaguomsingi ya programu)
- Kumbukumbu za msuguano na data ya kibinafsi iliyofichwa (kupitia Sentry)
- Tokeni ya arifa za kusukuma (FCM, hiari — tu ikiwa utawezesha arifa)
- Toleo la programu na toleo la iOS (kwa utatuzi wa makosa)

## 3. Jinsi Tunavyotumia Taarifa Zako

Tunatumia taarifa zako kwa:
- **Kutoa uchambuzi wa AI** wa maombi yako na tafakari za Muda wa Kimya (Google Gemini)
- **Kusawazisha data yako** kati ya vipindi na vifaa
- **Kusimamia usajili wako** na haki
- **Kurekebisha hitilafu na kuboresha programu** kupitia ripoti za msuguano
- **Kutuma arifa za hiari za kusukuma** (vikumbusho vya kila siku vya Muda wa Kimya) ikiwa utachagua kujiunga

**Hatufanyi** mambo yafuatayo:
- Kuonyesha matangazo ya aina yoyote
- Kuuza data yako kwa mtu yeyote
- Kushiriki maudhui yako ya maombi na mtu mwingine (isipokuwa usindikaji wa AI ulioelezewa hapa chini)
- Kutumia maudhui yako kufundisha miundo ya AI

## 4. Huduma za Mtu wa Tatu

Abba inategemea idadi ndogo ya huduma zinazoaminika ili kufanya kazi.

| Huduma | Madhumuni | Data Iliyotumwa | Eneo |
|---|---|---|---|
| **Supabase** | Hifadhidata na uthibitishaji | Kitambulisho kisichojulikana, maombi, metadata | US / EU |
| **Google Gemini API** | Uchambuzi wa AI wa maombi | Maandishi ya maombi tu | Google Cloud |
| **RevenueCat** | Usimamizi wa usajili | Kitambulisho kisichojulikana, risiti za ununuzi | US |
| **Sentry** | Ripoti za msuguano (PII imefichwa) | Ufuatiliaji wa makosa na barua pepe, nakala ndefu, JWT zikiondolewa | US / EU |
| **Firebase Cloud Messaging** | Arifa za kusukuma (hiari) | Tokeni ya FCM | Google Cloud |
| **Apple Sign-In / Google Sign-In** | Kiungo cha akaunti cha hiari | Barua pepe, kitambulisho cha mtoa huduma | Apple / Google |

**Google Gemini:** Kulingana na sera iliyochapishwa ya Google kwa matumizi ya API inayolipwa, maudhui ya maombi yaliyotumwa kwa Gemini **hayatumiki kufundisha miundo ya AI ya Google**. Usindikaji ni wa muda mfupi.

**Ufichaji wa PII wa Sentry:** Tunatumia sheria za ufichaji kabla ya kutuma ripoti za msuguano — barua pepe, nakala zenye urefu zaidi ya herufi 50, JWT, na vitambulisho vingine vinaondolewa.

## 5. Kuhifadhi Data na Usalama

- Data yote inayosafiri imesimbwa kupitia HTTPS (TLS 1.2+).
- Data iliyopumzika inalindwa na usimbaji wa mtoa huduma wa hifadhidata yetu.
- **Usalama wa Kiwango cha Safu (RLS)** katika Supabase unahakikisha kuwa unaweza kupata data yako tu.
- Faili za sauti zinahifadhiwa katika folda za kila mtumiaji zikiwa na ufikiaji unaodhibitiwa na tokeni yako ya uthibitishaji.
- Tokeni za ufikiaji zinahifadhiwa katika iOS Secure Enclave (`flutter_secure_storage`), kamwe si katika mapendeleo ya kawaida.

Tunahifadhi data yako maadamu akaunti yako inafanya kazi. Ukifuta akaunti yako, tunaondoa data yako ndani ya **siku 30**, isipokuwa pale ambapo tunahitajika kisheria kutunza rekodi (kama vile rekodi za kodi za ununuzi wa usajili, ambazo Apple/RevenueCat zinazihifadhi chini ya sera zao).

## 6. Haki Zako

Una haki zifuatazo juu ya data yako binafsi:

- **Ufikiaji** — omba nakala ya data tuliyonayo juu yako
- **Marekebisho** — tuombe kurekebisha taarifa zisizo sahihi
- **Kufuta** — tuombe kufuta akaunti yako na data (inapatikana ndani ya programu: Mipangilio → Akaunti → Futa Akaunti, au kwa barua pepe)
- **Uhamishaji** — omba uhamishaji wa data yako katika umbizo linalosomeka na mashine
- **Kupinga** — pinga usindikaji fulani
- **Kuondoa idhini** — unaweza kuondoa idhini kwa arifa za kusukuma, usindikaji wa AI, au kuunganisha akaunti wakati wowote

Kwa wakaazi wa GDPR (EU) na CCPA (California), haki hizi zimehakikishwa na sheria. Kutumia haki yoyote, tuma barua pepe kwa **rrallvv@gmail.com**. Tunajibu ndani ya siku 30.

## 7. Faragha ya Watoto

Abba imetolewa ukadiriaji wa 4+ katika App Store. Hatukusanyi taarifa kwa makusudi kutoka kwa watoto walio chini ya miaka 13 (COPPA) au chini ya miaka 16 (GDPR, katika baadhi ya nchi za EU) bila idhini ya wazazi inayothibitishwa. Ikiwa unaamini mtoto ametoa taarifa binafsi, tafadhali wasiliana nasi na tutazifuta mara moja.

## 8. Uhamishaji wa Data wa Kimataifa

Miundombinu yetu inaandaliwa Marekani na Muungano wa Ulaya. Kwa kutumia Abba, unakubali data yako kuhamishwa na kusindikwa katika maeneo haya. Tunategemea Vifungu vya Mkataba vya Kawaida (SCCs) pale inapohitajika.

## 9. Maombi ya Serikali na Kisheria

Tunafichua data ya mtumiaji tu wakati sheria inapohitaji (wito halali, amri ya mahakama, au sawa na hiyo). Hatujachapisha ripoti ya uwazi bado, lakini tunajitolea kuarifu watumiaji walioathirika wakati sheria inaporuhusu.

## 10. Mabadiliko ya Sera Hii

Tunaweza kusasisha Sera hii ya Faragha kadri Abba inavyoendelea kukua. Tunapofanya mabadiliko makubwa, tutakuarifu ndani ya programu na kusasisha tarehe ya "Imesasishwa Mwisho" juu. Kuendelea kutumia Abba baada ya mabadiliko kunamaanisha unakubali sera iliyosasishwa.

## 11. Wasiliana Nasi

Maswali, maombi, au malalamiko?

- **Barua pepe:** rrallvv@gmail.com
- **Muda wa kujibu:** ndani ya siku 30 (kwa kawaida mapema zaidi)

Pia una haki ya kufungua malalamiko na mamlaka ya ulinzi wa data ya eneo lako (kwa mfano, DPA ya nchi mwanachama wa EU, Mwanasheria Mkuu wa California, au PIPC ya Korea).

---
⚠️ **Notisi ya Tafsiri**: Hii ni tafsiri iliyotolewa kwa urahisi.
Ikiwa kuna tofauti yoyote, [toleo la Kiingereza](../privacy.html) litakuwa na nguvu.
