---
layout: default
title: Zásady ochrany osobných údajov — Abba
---

# Zásady ochrany osobných údajov

**Posledná aktualizácia: 22. apríla 2026**

## 1. Úvod

Abba („my", „naša aplikácia", „aplikácia") je mobilný spoločník pre modlitbu a Tichý čas (Quiet Time) určený pre kresťanov, ktorí sa chcú modliť hlbšie. Tieto Zásady ochrany osobných údajov opisujú, ako Abba zhromažďuje, používa, uchováva a chráni vaše informácie pri používaní aplikácie iOS (Bundle ID: `com.ystech.abba`).

Abba v súčasnosti funguje ako projekt nezávislého vývojára. Keď v týchto zásadách hovoríme „my", myslíme tým tím Abba. Ak sa Abba v budúcnosti stane registrovanou spoločnosťou, tieto zásady budú zodpovedajúcim spôsobom aktualizované.

Tieto zásady platia celosvetovo. Kde je to aplikovateľné, dodržiavame zásady Všeobecného nariadenia EÚ o ochrane údajov (GDPR), Kalifornského zákona o ochrane súkromia spotrebiteľov (CCPA) a Kórejského zákona o ochrane osobných údajov (PIPA).

## 2. Informácie, ktoré zhromažďujeme

### 2.1 Informácie o účte
Abba je **primárne anonymná**. Keď aplikáciu otvoríte prvýkrát, vytvoríme anonymné ID používateľa (UUID), aby sa vaše modlitby a nastavenia mohli synchronizovať medzi reláciami. Na používanie Abba nemusíte poskytovať meno, e-mail ani telefónne číslo.

Voliteľne sa môžete prihlásiť cez **Apple Sign-In** alebo **Google Sign-In**, aby ste si zálohovali dáta. V takom prípade od spoločnosti Apple alebo Google dostávame vašu e-mailovú adresu a jedinečný identifikátor. Ak chcete, môžete s Apple Sign-In použiť funkciu „Skryť môj e-mail".

### 2.2 Obsah modlitieb (základné údaje)
Keď používate Abba, zhromažďujeme:
- **Zvukové nahrávky** vašich vyslovených modlitieb
- **Prepisy** vygenerované z týchto nahrávok
- **Texty rozjímania a reflexií**, ktoré píšete alebo generujete
- **Pasáže Písma**, ktoré si označíte záložkou

Toto sú najcitlivejšie údaje, ktoré Abba spracúva, a zaobchádzame s nimi s opatrnosťou. Vaše zvukové nahrávky sa ukladajú do vášho vlastného súkromného priečinka na našom bezpečnom úložisku. Iba vy k nim máte prístup. Nepočúvame ich, nezdieľame ich ani ich nepoužívame na marketing.

### 2.3 Informácie o predplatnom
Ak sa prihlásite na odber Abba Pro, služba tretej strany **RevenueCat** zaznamená stav vášho predplatného (aktívne, uplynuté, skúšobné atď.) spolu s anonymným ID. **Nedostávame** číslo vašej kreditnej karty — to zostáva u spoločnosti Apple.

### 2.4 Technické informácie
- Jazyk zariadenia (na nastavenie predvoleného jazyka aplikácie)
- Záznamy o zlyhaniach s maskovanými osobnými údajmi (prostredníctvom Sentry)
- Token push notifikácií (FCM, voliteľné — iba ak povolíte notifikácie)
- Verzia aplikácie a verzia iOS (na ladenie)

## 3. Ako používame vaše informácie

Vaše informácie používame na:
- **Poskytovanie analýzy AI** vašich modlitieb a reflexií Tichého času (Google Gemini)
- **Synchronizáciu vašich údajov** medzi reláciami a zariadeniami
- **Spravovanie vášho predplatného** a oprávnení
- **Opravu chýb a zlepšenie aplikácie** prostredníctvom správ o zlyhaniach
- **Odosielanie voliteľných push notifikácií** (denné pripomienky Tichého času), ak si to zvolíte

**Nerobíme** toto:
- Nezobrazujeme žiadnu reklamu
- Nepredávame vaše dáta nikomu
- Nezdieľame obsah vašich modlitieb s tretími stranami (okrem spracovania AI opísaného nižšie)
- Nepoužívame váš obsah na trénovanie modelov AI

## 4. Služby tretích strán

Abba sa pri svojej prevádzke spolieha na malý počet dôveryhodných služieb.

| Služba | Účel | Odoslané údaje | Región |
|---|---|---|---|
| **Supabase** | Databáza a autentifikácia | Anonymné ID, modlitby, metadáta | USA / EÚ |
| **Google Gemini API** | AI analýza modlitieb | Iba text modlitby | Google Cloud |
| **RevenueCat** | Správa predplatného | Anonymné ID, potvrdenia o nákupe | USA |
| **Sentry** | Reporting zlyhaní (PII maskované) | Stopy chýb s odstránenými e-mailmi, dlhými prepismi, JWT | USA / EÚ |
| **Firebase Cloud Messaging** | Push notifikácie (voliteľné) | FCM token | Google Cloud |
| **Apple Sign-In / Google Sign-In** | Voliteľné prepojenie účtu | E-mail, ID poskytovateľa | Apple / Google |

**Google Gemini:** Podľa publikovaných zásad Google pre platené používanie API, obsah modlitieb odoslaný do Gemini **sa nepoužíva na trénovanie modelov AI spoločnosti Google**. Spracovanie je prechodné.

**Maskovanie PII v Sentry:** Pred odoslaním správ o zlyhaniach aplikujeme pravidlá maskovania — e-maily, prepisy dlhšie ako 50 znakov, JWT a iné identifikátory sú odstránené.

## 5. Ukladanie údajov a bezpečnosť

- Všetky prenášané údaje sú šifrované pomocou HTTPS (TLS 1.2+).
- Údaje v pokoji sú chránené šifrovaním nášho poskytovateľa databázy.
- **Bezpečnosť na úrovni riadku (RLS)** v Supabase zabezpečuje, že môžete pristupovať iba k vlastným údajom.
- Zvukové súbory sa ukladajú v priečinkoch pre jednotlivých používateľov s prístupom riadeným vaším autentifikačným tokenom.
- Prístupové tokeny sa ukladajú v iOS Secure Enclave (`flutter_secure_storage`), nikdy nie v bežných nastaveniach.

Vaše údaje uchovávame dovtedy, kým je váš účet aktívny. Ak si účet vymažete, vaše údaje odstránime do **30 dní**, okrem prípadov, keď sme zo zákona povinní uchovávať záznamy (napríklad daňové záznamy o nákupe predplatného, ktoré Apple/RevenueCat uchovávajú podľa vlastných zásad).

## 6. Vaše práva

Na svoje osobné údaje máte nasledujúce práva:

- **Prístup** — požiadať o kópiu údajov, ktoré o vás uchovávame
- **Oprava** — požiadať nás o opravu nepresných informácií
- **Vymazanie** — požiadať o vymazanie vášho účtu a údajov (dostupné v aplikácii: Nastavenia → Účet → Vymazať účet, alebo e-mailom)
- **Prenosnosť** — požiadať o export vašich údajov v strojovo čitateľnom formáte
- **Námietka** — namietať proti určitému spracovaniu
- **Odvolanie súhlasu** — súhlas s push notifikáciami, spracovaním AI alebo prepojením účtu môžete kedykoľvek odvolať

Pre obyvateľov GDPR (EÚ) a CCPA (Kalifornia) sú tieto práva zaručené zákonom. Ak chcete uplatniť akékoľvek právo, pošlite e-mail na **rrallvv@gmail.com**. Odpovedáme do 30 dní.

## 7. Súkromie detí

Abba je hodnotená 4+ v App Store. Vedome nezhromažďujeme informácie od detí mladších ako 13 rokov (COPPA) alebo 16 rokov (GDPR, v niektorých krajinách EÚ) bez overiteľného súhlasu rodiča. Ak sa domnievate, že dieťa poskytlo osobné informácie, prosím, kontaktujte nás a my ich okamžite vymažeme.

## 8. Medzinárodné prenosy údajov

Naša infraštruktúra je hosťovaná v Spojených štátoch a Európskej únii. Používaním Abba súhlasíte s prenosom a spracovaním vašich údajov v týchto regiónoch. Tam, kde je to potrebné, sa spoliehame na štandardné zmluvné doložky (SCC).

## 9. Štátne a právne žiadosti

Údaje používateľov zverejňujeme iba vtedy, keď to zákon vyžaduje (platné predvolanie, súdny príkaz alebo ekvivalent). Správu o transparentnosti ešte nezverejňujeme, ale zaväzujeme sa informovať dotknutých používateľov vtedy, keď to zákon umožňuje.

## 10. Zmeny týchto zásad

S rozvojom Abba môžeme tieto Zásady ochrany osobných údajov aktualizovať. Keď urobíme podstatné zmeny, upozorníme vás v aplikácii a aktualizujeme dátum „Posledná aktualizácia" v hornej časti. Pokračovanie v používaní Abba po zmenách znamená, že prijímate aktualizované zásady.

## 11. Kontaktujte nás

Otázky, žiadosti alebo sťažnosti?

- **E-mail:** rrallvv@gmail.com
- **Čas odpovede:** do 30 dní (zvyčajne skôr)

Máte tiež právo podať sťažnosť u svojho miestneho úradu na ochranu údajov (napr. DPA vášho členského štátu EÚ, Kalifornský generálny prokurátor alebo kórejský PIPC). Na Slovensku je to Úrad na ochranu osobných údajov SR.

---
⚠️ **Upozornenie o preklade**: Toto je preklad poskytnutý pre pohodlie.
V prípade akýchkoľvek nezrovnalostí má prednosť [anglická verzia](../privacy.html).
