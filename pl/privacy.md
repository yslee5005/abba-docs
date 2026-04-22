---
layout: default
title: Polityka Prywatności — Abba
---

# Polityka Prywatności

**Ostatnia aktualizacja: 22 kwietnia 2026**

## 1. Wprowadzenie

Abba („my", „nasz", „aplikacja") to mobilny towarzysz modlitwy i Cichego Czasu (Quiet Time) stworzony dla chrześcijan, którzy chcą modlić się głębiej. Niniejsza Polityka Prywatności opisuje, w jaki sposób Abba gromadzi, wykorzystuje, przechowuje i chroni Państwa dane, gdy korzystają Państwo z aplikacji iOS (Bundle ID: `com.ystech.abba`).

Abba jest obecnie prowadzona jako niezależny projekt deweloperski. Gdy w niniejszej polityce używamy słowa „my", mamy na myśli zespół Abba. Jeśli w przyszłości Abba stanie się zarejestrowaną firmą, niniejsza polityka zostanie odpowiednio zaktualizowana.

Niniejsza polityka obowiązuje na całym świecie. Przestrzegamy zasad unijnego ogólnego rozporządzenia o ochronie danych (RODO), kalifornijskiej ustawy o ochronie prywatności konsumentów (CCPA) oraz koreańskiej ustawy o ochronie danych osobowych (PIPA), tam gdzie ma to zastosowanie.

## 2. Informacje, które zbieramy

### 2.1 Informacje o koncie
Abba jest **domyślnie anonimowa**. Gdy otwierają Państwo aplikację po raz pierwszy, tworzymy anonimowy identyfikator użytkownika (UUID), aby Państwa modlitwy i ustawienia mogły być synchronizowane między sesjami. Do korzystania z Abba nie trzeba podawać imienia, adresu e-mail ani numeru telefonu.

Mogą Państwo opcjonalnie zalogować się za pomocą **Apple Sign-In** lub **Google Sign-In**, aby utworzyć kopię zapasową danych. W takim przypadku otrzymujemy Państwa adres e-mail i unikalny identyfikator od Apple lub Google. Przy Apple Sign-In można użyć opcji „Ukryj mój e-mail", jeśli się Państwo tak zdecydują.

### 2.2 Treść modlitw (dane podstawowe)
Gdy korzystają Państwo z Abba, zbieramy:
- **Nagrania audio** Państwa wypowiedzianych modlitw
- **Transkrypcje** wygenerowane z tych nagrań
- **Teksty medytacji i refleksje**, które Państwo piszą lub generują
- **Fragmenty Pisma Świętego**, które Państwo oznaczają jako ulubione

Są to najbardziej wrażliwe dane przetwarzane przez Abba i traktujemy je ze szczególną ostrożnością. Nagrania audio są przechowywane w prywatnym folderze na naszej bezpiecznej przestrzeni dyskowej. Tylko Państwo mają do nich dostęp. Nie odsłuchujemy ich, nie udostępniamy ani nie używamy do celów marketingowych.

### 2.3 Informacje o subskrypcji
Jeśli zasubskrybują Państwo Abba Pro, zewnętrzna usługa **RevenueCat** rejestruje status Państwa subskrypcji (aktywna, wygasła, okres próbny itp.) wraz z anonimowym identyfikatorem. **Nie** otrzymujemy numeru Państwa karty kredytowej — pozostaje on u Apple.

### 2.4 Informacje techniczne
- Język urządzenia (do ustawienia domyślnego języka aplikacji)
- Dzienniki awarii z zamaskowanymi danymi osobowymi (przez Sentry)
- Token powiadomień push (FCM, opcjonalny — tylko jeśli włączą Państwo powiadomienia)
- Wersja aplikacji i iOS (do debugowania)

## 3. Jak wykorzystujemy Państwa informacje

Wykorzystujemy Państwa informacje do:
- **Dostarczania analizy AI** Państwa modlitw i refleksji z Cichego Czasu (Google Gemini)
- **Synchronizacji Państwa danych** między sesjami i urządzeniami
- **Zarządzania Państwa subskrypcją** i uprawnieniami
- **Naprawiania błędów i ulepszania aplikacji** poprzez raporty o awariach
- **Wysyłania opcjonalnych powiadomień push** (codzienne przypomnienia o Cichym Czasie), jeśli wyrażą Państwo zgodę

**Nie**:
- Wyświetlamy żadnych reklam
- Sprzedajemy Państwa danych nikomu
- Udostępniamy treści modlitw osobom trzecim (z wyjątkiem przetwarzania AI opisanego poniżej)
- Wykorzystujemy treści do szkolenia modeli AI

## 4. Usługi podmiotów zewnętrznych

Abba opiera się na niewielkiej liczbie zaufanych usług.

| Usługa | Cel | Przesyłane dane | Region |
|---|---|---|---|
| **Supabase** | Baza danych i uwierzytelnianie | Anonimowy ID, modlitwy, metadane | USA / UE |
| **Google Gemini API** | Analiza AI modlitw | Tylko tekst modlitwy | Google Cloud |
| **RevenueCat** | Zarządzanie subskrypcjami | Anonimowy ID, potwierdzenia zakupu | USA |
| **Sentry** | Raporty awarii (maskowane dane osobowe) | Ślady błędów bez e-maili, długich transkrypcji, JWT | USA / UE |
| **Firebase Cloud Messaging** | Powiadomienia push (opcjonalne) | Token FCM | Google Cloud |
| **Apple Sign-In / Google Sign-In** | Opcjonalne łączenie konta | E-mail, ID dostawcy | Apple / Google |

**Google Gemini:** Zgodnie z opublikowaną polityką Google dotyczącą płatnego użycia API, treści modlitw wysyłane do Gemini **nie są wykorzystywane do trenowania modeli AI Google**. Przetwarzanie jest chwilowe.

**Maskowanie danych osobowych w Sentry:** Stosujemy reguły maskowania przed wysłaniem raportów awarii — usuwane są e-maile, koreańskie transkrypcje dłuższe niż 50 znaków, tokeny JWT i inne identyfikatory.

## 5. Przechowywanie i bezpieczeństwo danych

- Wszystkie przesyłane dane są szyfrowane za pomocą HTTPS (TLS 1.2+).
- Dane w spoczynku są chronione szyfrowaniem naszego dostawcy bazy danych.
- **Zabezpieczenia na poziomie wiersza (RLS)** w Supabase zapewniają, że mogą Państwo uzyskać dostęp tylko do swoich własnych danych.
- Pliki audio są przechowywane w folderach poszczególnych użytkowników, z dostępem kontrolowanym przez token uwierzytelniający.
- Tokeny dostępu są przechowywane w iOS Secure Enclave (`flutter_secure_storage`), nigdy w zwykłych preferencjach.

Przechowujemy Państwa dane tak długo, jak długo Państwa konto jest aktywne. Jeśli usuną Państwo konto, usuniemy Państwa dane w ciągu **30 dni**, z wyjątkiem przypadków, gdy jesteśmy prawnie zobowiązani do przechowywania rejestrów (takich jak ewidencja podatkowa zakupów subskrypcji, które Apple/RevenueCat przechowuje zgodnie z własnymi politykami).

## 6. Państwa prawa

Przysługują Państwu następujące prawa dotyczące danych osobowych:

- **Dostęp** — żądanie kopii danych, które o Państwu przechowujemy
- **Sprostowanie** — prośba o poprawienie nieprawidłowych informacji
- **Usunięcie** — prośba o usunięcie konta i danych (dostępne w aplikacji: Ustawienia → Konto → Usuń konto, lub przez e-mail)
- **Przenośność** — żądanie eksportu danych w formacie nadającym się do odczytu maszynowego
- **Sprzeciw** — sprzeciw wobec określonego przetwarzania
- **Wycofanie zgody** — mogą Państwo w każdej chwili wycofać zgodę na powiadomienia push, przetwarzanie AI lub łączenie konta

Dla mieszkańców UE (RODO) i Kalifornii (CCPA) prawa te są gwarantowane przez prawo. Aby skorzystać z któregokolwiek z praw, prosimy wysłać e-mail na **rrallvv@gmail.com**. Odpowiadamy w ciągu 30 dni.

## 7. Prywatność dzieci

Abba ma klasyfikację 4+ w App Store. Świadomie nie zbieramy informacji od dzieci poniżej 13 roku życia (COPPA) ani poniżej 16 roku życia (RODO, w niektórych krajach UE) bez weryfikowalnej zgody rodzica. Jeśli uważają Państwo, że dziecko podało dane osobowe, prosimy o kontakt, a natychmiast je usuniemy.

## 8. Międzynarodowe transfery danych

Nasza infrastruktura jest hostowana w Stanach Zjednoczonych i Unii Europejskiej. Korzystając z Abba, wyrażają Państwo zgodę na transfer i przetwarzanie Państwa danych w tych regionach. W razie potrzeby opieramy się na Standardowych Klauzulach Umownych (SCC).

## 9. Żądania rządowe i prawne

Ujawniamy dane użytkowników tylko wtedy, gdy wymaga tego prawo (ważny wezwanie, nakaz sądowy lub równoważny). Nie publikujemy jeszcze raportu przejrzystości, ale zobowiązujemy się do powiadamiania dotkniętych użytkowników, gdy pozwala na to prawo.

## 10. Zmiany w niniejszej polityce

Możemy aktualizować niniejszą Politykę Prywatności w miarę rozwoju Abba. Przy istotnych zmianach powiadomimy Państwa w aplikacji i zaktualizujemy datę „Ostatnia aktualizacja" na górze. Dalsze korzystanie z Abba po zmianach oznacza akceptację zaktualizowanej polityki.

## 11. Kontakt

Pytania, wnioski lub skargi?

- **E-mail:** rrallvv@gmail.com
- **Czas odpowiedzi:** w ciągu 30 dni (zwykle wcześniej)

Mają Państwo również prawo złożyć skargę do lokalnego organu ochrony danych (np. UODO w Polsce, DPA państwa członkowskiego UE, Prokuratora Generalnego Kalifornii lub koreańskiego PIPC).

---

⚠️ **Informacja o tłumaczeniu**: Jest to tłumaczenie dostarczone dla wygody. W przypadku rozbieżności obowiązuje [wersja angielska](../privacy.html).
