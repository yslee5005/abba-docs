---
layout: default
title: Adatvédelmi Szabályzat — Abba
---

# Adatvédelmi Szabályzat

**Utolsó frissítés: 2026. április 22.**

## 1. Bevezetés

Az Abba („mi", „miénk", „az alkalmazás") egy mobil ima- és Csendes idő (Quiet Time) kísérő, amelyet keresztények számára készítettünk, akik mélyebben szeretnének imádkozni. Ez az Adatvédelmi Szabályzat leírja, hogyan gyűjti, használja, tárolja és védi az Abba az Ön adatait, amikor az iOS alkalmazást használja (Bundle ID: `com.ystech.abba`).

Az Abba jelenleg független fejlesztői projektként üzemel. Amikor ebben a szabályzatban „mi"-ről beszélünk, az Abba csapatát értjük. Ha az Abba a jövőben bejegyzett vállalattá válik, ez a szabályzat ennek megfelelően frissül.

Ez a szabályzat világszerte érvényes. Követjük az EU Általános Adatvédelmi Rendeletének (GDPR), a California Consumer Privacy Actnek (CCPA) és a koreai személyes adatok védelméről szóló törvénynek (PIPA) elveit, ahol alkalmazható.

## 2. Az általunk gyűjtött adatok

### 2.1 Fiókadatok
Az Abba **alapértelmezetten anonim**. Amikor először nyitja meg az alkalmazást, létrehozunk egy anonim felhasználói azonosítót (UUID), hogy imái és beállításai szinkronizálódhassanak a munkamenetek között. Nem kell nevet, e-mail-címet vagy telefonszámot megadnia az Abba használatához.

Opcionálisan bejelentkezhet az **Apple Sign-In** vagy **Google Sign-In** segítségével, hogy biztonsági másolatot készítsen adatairól. Ebben az esetben megkapjuk az Ön e-mail-címét és egy egyedi azonosítót az Apple-től vagy a Google-tól. Az Apple Sign-Inhez használhatja az „E-mail elrejtése" funkciót, ha szeretné.

### 2.2 Imatartalom (fő adatok)
Amikor az Abbát használja, gyűjtjük:
- Az Ön kimondott imáinak **hangfelvételeit**
- Az ezekből a felvételekből készült **átiratokat**
- Az Ön által írt vagy generált **elmélkedési szövegeket és reflexiókat**
- Az Ön által könyvjelzőzött **bibliai részeket**

Ezek a legérzékenyebb adatok, amelyeket az Abba kezel, és gondosan kezeljük őket. Hangfelvételei a saját privát mappájában kerülnek tárolásra biztonságos tárhelyünkön. Csak Ön férhet hozzá. Nem hallgatjuk meg, nem osztjuk meg és nem használjuk marketing célokra.

### 2.3 Előfizetési adatok
Ha előfizet az Abba Próra, egy harmadik fél szolgáltatás, a **RevenueCat** rögzíti előfizetésének állapotát (aktív, lejárt, próbaidőszak stb.) az anonim azonosítóval együtt. **Nem** kapjuk meg a hitelkártyaszámát — az az Apple-nél marad.

### 2.4 Technikai információk
- Eszköz nyelve (az alapértelmezett alkalmazásnyelv beállításához)
- Összeomlási naplók maszkolt személyes adatokkal (Sentryn keresztül)
- Push értesítési token (FCM, opcionális — csak ha engedélyezi az értesítéseket)
- Alkalmazás- és iOS-verzió (hibakereséshez)

## 3. Hogyan használjuk az Ön adatait

Adatait a következőkre használjuk:
- **AI-elemzés biztosítása** imáiról és Csendes idő reflexióiról (Google Gemini)
- **Adatainak szinkronizálása** munkamenetek és eszközök között
- **Előfizetésének kezelése** és jogosultságok
- **Hibák javítása és az alkalmazás fejlesztése** összeomlási jelentések segítségével
- **Opcionális push értesítések küldése** (napi Csendes idő emlékeztetők) ha beleegyezik

**Nem**:
- Jelenítünk meg semmilyen reklámot
- Adjuk el adatait senkinek
- Osztjuk meg imatartalmait harmadik felekkel (kivéve az alább leírt AI-feldolgozást)
- Használjuk tartalmait AI-modellek betanítására

## 4. Harmadik fél szolgáltatásai

Az Abba kisszámú megbízható szolgáltatásra támaszkodik a működéséhez.

| Szolgáltatás | Cél | Küldött adatok | Régió |
|---|---|---|---|
| **Supabase** | Adatbázis és hitelesítés | Anonim azonosító, imák, metaadatok | USA / EU |
| **Google Gemini API** | Imák AI-elemzése | Csak imaszöveg | Google Cloud |
| **RevenueCat** | Előfizetéskezelés | Anonim azonosító, vásárlási bizonylatok | USA |
| **Sentry** | Összeomlási jelentések (PII maszkolva) | Hibanyomok e-mailek, hosszú átiratok, JWT-k nélkül | USA / EU |
| **Firebase Cloud Messaging** | Push értesítések (opcionális) | FCM token | Google Cloud |
| **Apple Sign-In / Google Sign-In** | Opcionális fiókkapcsolás | E-mail, szolgáltatói azonosító | Apple / Google |

**Google Gemini:** A Google közzétett szabályzata szerint a fizetős API-használathoz a Geminibe küldött imatartalmak **nem kerülnek felhasználásra a Google AI-modelljeinek betanítására**. A feldolgozás átmeneti.

**Sentry PII-maszkolás:** Az összeomlási jelentések elküldése előtt maszkolási szabályokat alkalmazunk — az e-mailek, 50 karakternél hosszabb koreai átiratok, JWT-k és egyéb azonosítók eltávolításra kerülnek.

## 5. Adattárolás és biztonság

- Minden átvitt adat HTTPS-en (TLS 1.2+) keresztül titkosított.
- A nyugvó adatokat adatbázis-szolgáltatónk titkosítása védi.
- A Supabase **sor szintű biztonsága (RLS)** biztosítja, hogy csak a saját adataihoz férjen hozzá.
- A hangfájlokat felhasználónkénti mappákban tároljuk, a hozzáférést hitelesítési tokenje vezérli.
- A hozzáférési tokenek iOS Secure Enclave-ben (`flutter_secure_storage`) kerülnek tárolásra, soha nem egyszerű beállításokban.

Adatait addig őrizzük meg, amíg fiókja aktív. Ha törli fiókját, adatait **30 napon belül** eltávolítjuk, kivéve ott, ahol jogszabály alapján kötelesek vagyunk nyilvántartást vezetni (például az előfizetési vásárlások adóügyi nyilvántartásai, amelyeket az Apple/RevenueCat saját szabályzatai szerint tárol).

## 6. Az Ön jogai

A személyes adataival kapcsolatban az alábbi jogokkal rendelkezik:

- **Hozzáférés** — kérheti az Önről tárolt adatok másolatát
- **Helyesbítés** — kérheti pontatlan információk javítását
- **Törlés** — kérheti fiókja és adatai törlését (elérhető az alkalmazásban: Beállítások → Fiók → Fiók törlése, vagy e-mailben)
- **Hordozhatóság** — kérheti adatai exportját géppel olvasható formátumban
- **Tiltakozás** — tiltakozhat bizonyos adatkezelés ellen
- **Hozzájárulás visszavonása** — bármikor visszavonhatja a push értesítésekhez, AI-feldolgozáshoz vagy fiókkapcsoláshoz adott hozzájárulását

A GDPR- (EU) és CCPA-lakosok (Kalifornia) számára ezek a jogok törvényileg garantáltak. Bármely jog gyakorlásához küldjön e-mailt a **rrallvv@gmail.com** címre. 30 napon belül válaszolunk.

## 7. Gyermekek adatvédelme

Az Abba 4+ besorolással rendelkezik az App Store-ban. Tudatosan nem gyűjtünk információt 13 év alatti (COPPA) vagy 16 év alatti (GDPR, egyes EU-országokban) gyermekektől ellenőrizhető szülői hozzájárulás nélkül. Ha úgy gondolja, hogy egy gyermek személyes adatokat adott meg, kérjük, lépjen kapcsolatba velünk, és azonnal töröljük őket.

## 8. Nemzetközi adattovábbítások

Infrastruktúránk az Egyesült Államokban és az Európai Unióban található. Az Abba használatával hozzájárul adatai ezekbe a régiókba történő továbbításához és feldolgozásához. Ahol szükséges, az általános szerződési feltételekre (SCC) támaszkodunk.

## 9. Kormányzati és jogi kérések

Felhasználói adatokat csak akkor adunk ki, ha jogszabály megköveteli (érvényes idézés, bírósági végzés vagy egyenértékű). Még nem teszünk közzé átláthatósági jelentést, de elkötelezettek vagyunk, hogy értesítsük az érintett felhasználókat, ha jogszabály megengedi.

## 10. A szabályzat módosításai

Az Adatvédelmi Szabályzatot frissíthetjük, ahogy az Abba fejlődik. Jelentős változások esetén értesítjük Önt az alkalmazásban, és frissítjük a „Utolsó frissítés" dátumot a tetején. Az Abba folyamatos használata a változások után azt jelenti, hogy elfogadja a frissített szabályzatot.

## 11. Kapcsolat

Kérdések, kérések vagy panaszok?

- **E-mail:** rrallvv@gmail.com
- **Válaszidő:** 30 napon belül (általában hamarabb)

Jogában áll panaszt tenni a helyi adatvédelmi hatóságánál (pl. NAIH Magyarországon, az EU tagállama DPA-ja, Kalifornia főügyésze vagy Korea PIPC-je).

---

⚠️ **Fordítási megjegyzés**: Ez egy kényelmi célból biztosított fordítás. Eltérés esetén az [angol változat](../privacy.html) irányadó.
