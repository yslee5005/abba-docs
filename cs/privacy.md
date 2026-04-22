---
layout: default
title: Zásady ochrany osobních údajů — Abba
---

# Zásady ochrany osobních údajů

**Poslední aktualizace: 22. dubna 2026**

## 1. Úvod

Abba („my", „naše", „aplikace") je mobilní společník pro modlitbu a Tichý čas (Quiet Time) vytvořený pro křesťany, kteří chtějí hlouběji prožívat modlitbu. Tyto Zásady ochrany osobních údajů popisují, jak Abba shromažďuje, používá, uchovává a chrání vaše informace, když používáte aplikaci pro iOS (Bundle ID: `com.ystech.abba`).

Abba je v současnosti provozována jako nezávislý vývojářský projekt. Když v těchto zásadách používáme „my", máme na mysli tým Abba. Pokud se Abba v budoucnu stane registrovanou společností, tyto zásady budou odpovídajícím způsobem aktualizovány.

Tyto zásady platí celosvětově. Dodržujeme zásady obecného nařízení EU o ochraně osobních údajů (GDPR), California Consumer Privacy Act (CCPA) a korejského zákona o ochraně osobních údajů (PIPA), kde je to relevantní.

## 2. Informace, které shromažďujeme

### 2.1 Informace o účtu
Abba je **anonymní ve výchozím nastavení**. Když otevřete aplikaci poprvé, vytvoříme anonymní ID uživatele (UUID), aby bylo možné synchronizovat vaše modlitby a nastavení napříč relacemi. Nemusíte poskytovat jméno, e-mail ani telefonní číslo, abyste mohli používat Abba.

Volitelně se můžete přihlásit pomocí **Apple Sign-In** nebo **Google Sign-In** pro zálohování dat. V tom případě obdržíme vaši e-mailovou adresu a jedinečný identifikátor od Apple nebo Google. Pokud chcete, můžete u Apple Sign-In použít funkci „Skrýt můj e-mail".

### 2.2 Obsah modliteb (základní data)
Při používání Abba shromažďujeme:
- **Zvukové záznamy** vašich mluvených modliteb
- **Přepisy** generované z těchto záznamů
- **Texty meditací a reflexe**, které píšete nebo generujete
- **Biblické pasáže**, které si označíte

Toto jsou nejcitlivější data, která Abba zpracovává, a zacházíme s nimi s péčí. Vaše zvukové záznamy jsou uloženy ve vaší vlastní soukromé složce na našem zabezpečeném úložišti. Přístup máte pouze vy. Neposloucháme je, nesdílíme je ani je nepoužíváme pro marketing.

### 2.3 Informace o předplatném
Pokud si předplatíte Abba Pro, služba třetí strany zvaná **RevenueCat** zaznamenává stav vašeho předplatného (aktivní, vypršelé, zkušební atd.) spolu s anonymním ID. **Nedostáváme** číslo vaší kreditní karty — to zůstává u Apple.

### 2.4 Technické informace
- Jazyk zařízení (pro nastavení výchozího jazyka aplikace)
- Záznamy o chybách s maskovanými osobními údaji (přes Sentry)
- Token push notifikací (FCM, volitelný — pouze pokud povolíte notifikace)
- Verze aplikace a iOS (pro ladění)

## 3. Jak používáme vaše informace

Vaše informace používáme k:
- **Poskytování AI analýzy** vašich modliteb a reflexí Tichého času (Google Gemini)
- **Synchronizaci vašich dat** napříč relacemi a zařízeními
- **Správě vašeho předplatného** a oprávnění
- **Opravě chyb a zlepšování aplikace** prostřednictvím hlášení o pádech
- **Odesílání volitelných push notifikací** (každodenní připomínky Tichého času), pokud souhlasíte

**Neděláme**:
- Nezobrazujeme reklamu žádného druhu
- Neprodáváme vaše data nikomu
- Nesdílíme obsah vašich modliteb s třetími stranami (kromě zpracování AI popsaného níže)
- Nepoužíváme váš obsah k trénování AI modelů

## 4. Služby třetích stran

Abba spoléhá na malé množství důvěryhodných služeb pro svůj provoz.

| Služba | Účel | Odesílaná data | Region |
|---|---|---|---|
| **Supabase** | Databáze a ověření | Anonymní ID, modlitby, metadata | USA / EU |
| **Google Gemini API** | AI analýza modliteb | Pouze text modlitby | Google Cloud |
| **RevenueCat** | Správa předplatného | Anonymní ID, potvrzení o nákupu | USA |
| **Sentry** | Hlášení pádů (PII maskováno) | Stopy chyb bez e-mailů, dlouhých přepisů, JWT odstraněno | USA / EU |
| **Firebase Cloud Messaging** | Push notifikace (volitelné) | FCM token | Google Cloud |
| **Apple Sign-In / Google Sign-In** | Volitelné propojení účtu | E-mail, ID poskytovatele | Apple / Google |

**Google Gemini:** Podle zveřejněné politiky Google pro placené použití API obsah modliteb odeslaný do Gemini **není používán k trénování AI modelů Google**. Zpracování je přechodné.

**Sentry PII maskování:** Před odesláním hlášení o pádech uplatňujeme pravidla maskování — e-maily, korejské přepisy delší než 50 znaků, JWT a další identifikátory jsou odstraněny.

## 5. Ukládání dat a bezpečnost

- Všechna data při přenosu jsou šifrována přes HTTPS (TLS 1.2+).
- Data v klidu jsou chráněna šifrováním našeho poskytovatele databáze.
- **Row-Level Security (RLS)** v Supabase zajišťuje, že máte přístup pouze ke svým vlastním datům.
- Zvukové soubory jsou uloženy ve složkách jednotlivých uživatelů s přístupem řízeným vaším ověřovacím tokenem.
- Přístupové tokeny jsou uloženy v iOS Secure Enclave (`flutter_secure_storage`), nikdy v běžných preferencích.

Vaše data uchováváme po dobu aktivního účtu. Pokud smažete svůj účet, odstraníme vaše data do **30 dnů**, s výjimkou případů, kdy jsme právně povinni uchovávat záznamy (například daňové záznamy o nákupech předplatného, které Apple/RevenueCat uchovávají podle vlastních zásad).

## 6. Vaše práva

Máte následující práva týkající se vašich osobních údajů:

- **Přístup** — požádat o kopii dat, která o vás uchováváme
- **Oprava** — požádat nás o opravu nepřesných informací
- **Vymazání** — požádat nás o smazání vašeho účtu a dat (dostupné v aplikaci: Nastavení → Účet → Smazat účet, nebo e-mailem)
- **Přenositelnost** — požádat o export dat ve strojově čitelném formátu
- **Námitka** — vznést námitku proti určitému zpracování
- **Odvolání souhlasu** — můžete kdykoli odvolat souhlas s push notifikacemi, zpracováním AI nebo propojením účtů

Pro rezidenty GDPR (EU) a CCPA (Kalifornie) jsou tato práva zaručena zákonem. Chcete-li uplatnit jakékoli právo, pošlete e-mail na **rrallvv@gmail.com**. Odpovídáme do 30 dnů.

## 7. Soukromí dětí

Abba je v App Store hodnocena 4+. Vědomě neshromažďujeme informace od dětí mladších 13 let (COPPA) nebo mladších 16 let (GDPR, v některých zemích EU) bez ověřitelného rodičovského souhlasu. Pokud se domníváte, že dítě poskytlo osobní údaje, kontaktujte nás a okamžitě je smažeme.

## 8. Mezinárodní přenosy dat

Naše infrastruktura je hostována v USA a Evropské unii. Používáním Abba souhlasíte s přenosem a zpracováním vašich dat v těchto regionech. Kde je to nutné, spoléháme na Standardní smluvní doložky (SCC).

## 9. Vládní a právní žádosti

Uživatelská data zpřístupňujeme pouze tehdy, pokud to vyžaduje zákon (platné předvolání, soudní příkaz nebo ekvivalent). Zatím nezveřejňujeme zprávu o transparentnosti, ale zavazujeme se informovat dotčené uživatele, pokud to zákon umožňuje.

## 10. Změny této politiky

Tyto Zásady ochrany osobních údajů můžeme aktualizovat podle toho, jak se Abba vyvíjí. Při podstatných změnách vás upozorníme v aplikaci a aktualizujeme datum „Poslední aktualizace" nahoře. Pokračující používání Abba po změnách znamená, že přijímáte aktualizované zásady.

## 11. Kontaktujte nás

Dotazy, žádosti nebo stížnosti?

- **E-mail:** rrallvv@gmail.com
- **Doba odpovědi:** do 30 dnů (obvykle dříve)

Máte také právo podat stížnost u místního úřadu pro ochranu osobních údajů (např. ÚOOÚ v ČR, DPA vašeho členského státu EU, kalifornského generálního prokurátora nebo korejského PIPC).

---

⚠️ **Upozornění na překlad**: Toto je překlad poskytnutý pro pohodlí. V případě rozporů má přednost [anglická verze](../privacy.html).
