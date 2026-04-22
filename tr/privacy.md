---
layout: default
title: Gizlilik Politikası — Abba
---

# Gizlilik Politikası

**Son Güncelleme: 22 Nisan 2026**

## 1. Giriş

Abba ("biz", "uygulamamız", "uygulama"), daha derin dua etmek isteyen Hristiyanlar için tasarlanmış mobil bir dua ve Sessiz Zaman (Quiet Time) rehberidir. Bu Gizlilik Politikası, iOS uygulamasını (Bundle ID: `com.ystech.abba`) kullandığınızda Abba'nın bilgilerinizi nasıl topladığını, kullandığını, sakladığını ve koruduğunu açıklar.

Abba şu anda bağımsız bir geliştirici projesi olarak faaliyet göstermektedir. Bu politikada "biz" dediğimizde, Abba ekibini kastediyoruz. Abba gelecekte tescilli bir şirket haline gelirse, bu politika buna göre güncellenecektir.

Bu politika dünya çapında geçerlidir. Geçerli olduğu yerlerde AB Genel Veri Koruma Tüzüğü (GDPR), Kaliforniya Tüketici Gizliliği Yasası (CCPA) ve Kore Kişisel Bilgileri Koruma Yasası (PIPA) ilkelerine uyuyoruz. Türkiye'deki kullanıcılar için Kişisel Verilerin Korunması Kanunu (KVKK) kapsamındaki hakları gözetiyoruz.

## 2. Topladığımız Bilgiler

### 2.1 Hesap Bilgileri
Abba **öncelikle anonim** çalışır. Uygulamayı ilk açtığınızda, dualarınız ve ayarlarınızın oturumlar arasında senkronize olabilmesi için anonim bir kullanıcı kimliği (UUID) oluştururuz. Abba'yı kullanmak için ad, e-posta veya telefon numarası vermeniz gerekmez.

Verilerinizi yedeklemek için isteğe bağlı olarak **Apple ile Giriş** veya **Google ile Giriş** kullanabilirsiniz. Bu durumda Apple veya Google'dan e-posta adresinizi ve benzersiz bir tanımlayıcıyı alırız. Tercih ederseniz Apple ile Giriş'te "E-postamı Gizle" özelliğini kullanabilirsiniz.

### 2.2 Dua İçeriği (Temel Veri)
Abba'yı kullandığınızda şunları toplarız:
- Sözlü dualarınızın **ses kayıtları**
- Bu kayıtlardan oluşturulan **transkriptler**
- Yazdığınız veya ürettiğiniz **tefekkür metinleri ve düşünceler**
- Yer işareti koyduğunuz **Kutsal Kitap pasajları**

Bu, Abba'nın işlediği en hassas veridir ve onunla özenle ilgileniyoruz. Sesiniz, güvenli depolamamızdaki kendi özel klasörünüzde saklanır. Yalnızca siz erişebilirsiniz. Onu dinlemiyoruz, paylaşmıyoruz veya pazarlama için kullanmıyoruz.

### 2.3 Abonelik Bilgileri
Abba Pro'ya abone olursanız, **RevenueCat** adlı üçüncü taraf bir hizmet, abonelik durumunuzu (aktif, süresi dolmuş, deneme vb.) anonim kimlikle birlikte kaydeder. Kredi kartı numaranızı **almıyoruz** — o Apple'da kalır.

### 2.4 Teknik Bilgiler
- Cihaz dili (uygulama varsayılan dilini ayarlamak için)
- Kişisel verileri maskelenmiş kilitlenme günlükleri (Sentry aracılığıyla)
- Push bildirim tokenı (FCM, isteğe bağlı — yalnızca bildirimleri etkinleştirirseniz)
- Uygulama ve iOS sürümü (hata ayıklama için)

## 3. Bilgilerinizi Nasıl Kullanırız

Bilgilerinizi şu amaçlarla kullanırız:
- Dualarınız ve Sessiz Zaman düşüncelerinize **AI analizi sağlamak** (Google Gemini)
- Verilerinizi oturumlar ve cihazlar arasında **senkronize etmek**
- **Aboneliğinizi ve haklarınızı yönetmek**
- Kilitlenme raporları aracılığıyla **hataları düzeltmek ve uygulamayı iyileştirmek**
- Kabul ederseniz **isteğe bağlı push bildirimleri göndermek** (günlük Sessiz Zaman hatırlatıcıları)

Şunları **yapmıyoruz**:
- Herhangi bir reklam göstermek
- Verilerinizi kimseye satmak
- Dua içeriğinizi üçüncü taraflarla paylaşmak (aşağıda açıklanan AI işlemi hariç)
- İçeriğinizi AI modellerini eğitmek için kullanmak

## 4. Üçüncü Taraf Hizmetler

Abba, çalışmak için az sayıda güvenilir hizmete dayanır.

| Hizmet | Amaç | Gönderilen Veri | Bölge |
|---|---|---|---|
| **Supabase** | Veritabanı ve kimlik doğrulama | Anonim ID, dualar, üstveri | ABD / AB |
| **Google Gemini API** | Duaların AI analizi | Yalnızca dua metni | Google Cloud |
| **RevenueCat** | Abonelik yönetimi | Anonim ID, satın alma makbuzları | ABD |
| **Sentry** | Kilitlenme raporlama (PII maskeli) | E-postalar, uzun transkriptler, JWT'ler kaldırılmış hata izleri | ABD / AB |
| **Firebase Cloud Messaging** | Push bildirimleri (isteğe bağlı) | FCM tokenı | Google Cloud |
| **Apple ile Giriş / Google ile Giriş** | İsteğe bağlı hesap bağlama | E-posta, sağlayıcı kimliği | Apple / Google |

**Google Gemini:** Google'ın ücretli API kullanımı için yayınlanmış politikasına göre, Gemini'ye gönderilen dua içeriği **Google'ın AI modellerini eğitmek için kullanılmaz**. İşleme geçicidir.

**Sentry PII maskeleme:** Kilitlenme raporları göndermeden önce maskeleme kuralları uygularız — e-postalar, 50 karakterden uzun transkriptler, JWT'ler ve diğer tanımlayıcılar çıkarılır.

## 5. Veri Depolama ve Güvenlik

- Tüm iletim halindeki veriler HTTPS (TLS 1.2+) ile şifrelenir.
- Depolanan veriler, veritabanı sağlayıcımızın şifrelemesi ile korunur.
- Supabase'deki **Satır Düzeyinde Güvenlik (RLS)**, yalnızca kendi verilerinize erişebilmenizi sağlar.
- Ses dosyaları kullanıcı başına klasörlerde saklanır ve erişim, kimlik doğrulama tokenınızla kontrol edilir.
- Erişim tokenları iOS Secure Enclave'de (`flutter_secure_storage`) saklanır, asla düz tercihlerde değil.

Hesabınız aktif olduğu sürece verilerinizi saklarız. Hesabınızı silerseniz, verilerinizi **30 gün** içinde kaldırırız, ancak yasal olarak kayıt tutmamız gereken durumlar hariç (örneğin, Apple/RevenueCat'in kendi politikalarına göre sakladığı abonelik satın alma vergi kayıtları).

## 6. Haklarınız

Kişisel verileriniz üzerinde aşağıdaki haklara sahipsiniz:

- **Erişim** — hakkınızda tuttuğumuz verilerin bir kopyasını isteme
- **Düzeltme** — yanlış bilgileri düzeltmemizi isteme
- **Silme** — hesabınızın ve verilerinizin silinmesini isteme (uygulama içinde: Ayarlar → Hesap → Hesabı Sil veya e-posta ile)
- **Taşınabilirlik** — verilerinizin makine okunabilir bir formatta dışa aktarılmasını isteme
- **İtiraz** — belirli işlemlere itiraz etme
- **Onayı geri çekme** — push bildirimleri, AI işleme veya hesap bağlamaya onayınızı istediğiniz zaman geri çekebilirsiniz

GDPR (AB) ve CCPA (Kaliforniya) sakinleri için bu haklar yasal olarak güvence altındadır. Herhangi bir hakkı kullanmak için **rrallvv@gmail.com** adresine e-posta gönderin. 30 gün içinde yanıt veriyoruz.

## 7. Çocukların Gizliliği

Abba, App Store'da 4+ olarak derecelendirilmiştir. Doğrulanabilir ebeveyn onayı olmadan 13 yaşın altındaki (COPPA) veya bazı AB ülkelerinde 16 yaşın altındaki (GDPR) çocuklardan bilgi toplamıyoruz. Bir çocuğun kişisel bilgi sağladığına inanıyorsanız, lütfen bizimle iletişime geçin ve derhal sileceğiz.

## 8. Uluslararası Veri Aktarımları

Altyapımız Amerika Birleşik Devletleri'nde ve Avrupa Birliği'nde barındırılmaktadır. Abba'yı kullanarak, verilerinizin bu bölgelere aktarılmasına ve işlenmesine onay vermiş olursunuz. Gerektiğinde Standart Sözleşme Maddelerine (SCC) dayanırız.

## 9. Hükümet ve Yasal Talepler

Kullanıcı verilerini yalnızca yasal olarak gerekli olduğunda (geçerli bir mahkeme celbi, mahkeme emri veya eşdeğeri) açıklarız. Henüz bir şeffaflık raporu yayınlamıyoruz, ancak yasal olarak izin verildiğinde etkilenen kullanıcıları bilgilendirmeyi taahhüt ediyoruz.

## 10. Bu Politikadaki Değişiklikler

Abba geliştikçe bu Gizlilik Politikasını güncelleyebiliriz. Önemli değişiklikler yaptığımızda, sizi uygulamada bilgilendireceğiz ve üstteki "Son Güncelleme" tarihini güncelleyeceğiz. Değişikliklerden sonra Abba'yı kullanmaya devam etmeniz, güncellenmiş politikayı kabul ettiğiniz anlamına gelir.

## 11. Bize Ulaşın

Sorular, istekler veya şikayetler?

- **E-posta:** rrallvv@gmail.com
- **Yanıt süresi:** 30 gün içinde (genellikle daha kısa)

Ayrıca yerel veri koruma kurumunuza (örneğin, AB üye devletinizin DPA'sı, Kaliforniya Başsavcısı veya Kore PIPC'si) şikayette bulunma hakkınız da vardır.

---
⚠️ **Çeviri Bildirimi**: Bu çeviri, kolaylık sağlamak için sunulmuştur.
Herhangi bir tutarsızlık durumunda, [İngilizce versiyon](../privacy.html) geçerli olacaktır.
