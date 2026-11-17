# Firebase yapılandırması (özel / private)

Bu açık kaynak pakette **gerçek Firebase yapılandırması paylaşılmıyor**.
`app/google-services.json` dosyası kasıtlı olarak pakete eklenmedi ve `.gitignore` ile GitHub yüklemelerinden hariç tutuldu.

Projeyi kendi bilgisayarında Firebase ile derlemek için:

1. Kendi Firebase Console projen üzerinden Android uygulamasına ait `google-services.json` dosyasını edin.
2. Bu dosyayı **yalnızca yerel bilgisayarında** `app/google-services.json` konumuna koy.
3. Dosyayı GitHub'a commit etme.

**Not:** `google-services.json` çıkarıldığında Google Services Gradle eklentisi nedeniyle proje yapılandırma olmadan derlenmeyebilir. Bu durum dosyaların bozuk olduğu anlamına gelmez.

Firebase istemci yapılandırması tek başına sunucu tarafı gizli anahtar gibi değerlendirilmez; yine de herkese açık paylaşmama tercihini koruyoruz. Gerçek servis hesabı anahtarlarını veya özel tokenları hiçbir zaman projeye ekleme.
