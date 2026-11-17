<div align="right">
  <a href="README.md">English</a> | <strong>Türkçe</strong>
</div>

# Flawless | Kişisel Gelişim ve Takip Uygulaması

**Flawless**, **23 Kasım ile 10 Ocak** arasındaki hedeflerimi ve günlük ilerlememi tek bir yerden takip edebilmek için hazırladığım kişisel Android uygulamasıdır. Görevlerimi, alışkanlıklarımı ve gün içinde yaptıklarımı ayrı ayrı takip etmek yerine düzenli biçimde gözlemleyebileceğim bir sistem oluşturmak istedim.

Bu proje ticari bir uygulamadan çok **kişisel takip ve öğrenme projesidir**. Amacım belirli bir zaman aralığında daha düzenli hareket etmek, tamamladığım işleri görmek ve alışkanlıklarımı değerlendirebilmek.

## Neden geliştirdim?

23 Kasım–10 Ocak aralığını kendim için bir takip dönemi olarak belirledim. Bu süreyi küçük aşamalara bölerek görevlerimi, günlük rutinlerimi ve kişisel hedeflerimi somut olarak izlemek istedim. Uygulamayı geliştirirken Android uygulama mimarisi, arayüz tasarımı, durum yönetimi ve yerel veri saklama konularında da deneyim kazanmayı hedefledim.

## Özellikler

- **Ana ekran:** günlük ilerleme ve hedef dönemine ilişkin genel görünüm.
- **Görevler:** görev ekleme, düzenleme, önceliklendirme, tamamlama ve silme.
- **Alışkanlıklar:** düzenli yapılan aktiviteleri ve tamamlanan günleri takip etme.
- **Günlük takip:** su, spor, İngilizce çalışması ve öğün kayıtları.
- **Günlük:** düşünceleri yazma ve günün ruh hâlini kaydetme.
- **Profil ve tercihler:** bazı takip değerlerini ve uygulama ayarlarını yönetme.
- **Yerel kayıt:** temel takip verilerini Android DataStore ile cihazda saklama.

## Kullanılan teknolojiler

- Kotlin
- Jetpack Compose / Material 3
- Android Jetpack ViewModel
- DataStore Preferences
- WorkManager
- Gradle (Kotlin DSL)
- Firebase ile ilgili Gradle yapılandırması (kişisel yapılandırma dosyası gerektirir)

## Kurulum

1. Repository'yi klonlayın:

   ```bash
   git clone https://github.com/burakunal516/Flawless-App.git
   ```

2. Projeyi **Android Studio** ile açıp Gradle eşitlemesini tamamlayın.
3. Aşağıdaki Firebase yapılandırmasını kendi projeniz için ekleyin.
4. Uygulamayı uyumlu bir Android cihazda veya emülatörde çalıştırın.

### Önemli: Firebase dosyasını sizin eklemeniz gerekiyor

Projeye ait gerçek `app/google-services.json` dosyasını **gizlilik tercihim nedeniyle herkese açık GitHub repository'sine eklemedim**. Bu dosya yanlışlıkla silinmiş değil, bilinçli olarak paylaşım dışında bırakılmıştır.

Mevcut Google Services Gradle yapılandırmasıyla projeyi derlemek için:

1. [Firebase Console](https://console.firebase.google.com/) üzerinden **kendi** Firebase projenizi oluşturun veya seçin.
2. Android uygulaması ekleyin. Paket/uygulama kimliği `com.burak` olmalıdır. (Kimliği değiştirirseniz Firebase kaydını da ona uygun yapın.)
3. Oluşturulan `google-services.json` dosyasını indirin.
4. Dosyayı bilgisayarınızda `app/google-services.json` konumuna ekleyin.
5. Android Studio'da Gradle eşitlemesi yapıp projeyi derleyin.

**Kendi Firebase yapılandırma dosyanızı, servis hesabı anahtarlarını, gizli anahtarları veya tokenları GitHub'a yüklemeyin.** `.gitignore`, `google-services.json` dosyasını hariç tutacak şekilde ayarlanmıştır. Ek bilgi için [`FIREBASE_KURULUM.md`](FIREBASE_KURULUM.md) dosyasına bakın. Bu dosya olmadan Google Services Gradle eklentisi nedeniyle derleme hatası alınabilir.

> Not: Kaynak kodda Firebase AI bağımlılığı ve Google Services yapılandırması bulunuyor. Ancak temel takip kayıtları DataStore ile cihazda tutuluyor. Günlük kayıtların Firebase'e eşitlendiği iddia edilmiyor.

## Geliştirme notu

Uygulamayı geliştirirken yapay zekâ destekli araçlardan yararlandım. Projenin çıkış noktası, 23 Kasım–10 Ocak dönemindeki kişisel takip ihtiyacımdı.

## Proje durumu

Kişisel proje / geliştirmeye açık. Uygulama geliştikçe bazı özellikler ve kurulum gereksinimleri değişebilir.
