# Yedekleme ve geri yükleme

[Makine projesine dön](../README.md)

Proje için hedef, son onaylı yapılandırmayı geri yükleyebilmektir. Kabul edilen reçete değişiklikleri de yedeğe alınır. Geri yükleme süresi T08 sırasında ölçülecektir

| İçerik | Yedekleme zamanı | Saklama ve sorumlu |
| --- | --- | --- |
| PLC/HMI projesi ve reçeteler | Her onaylı değişiklikten önce ve sonra | Erişimi sınırlı depo ve çevrimdışı kopya, bakım |
| Emniyet projesi ve doğrulama bilgisi | Onaylı değişiklikten önce ve sonra | Ayrı kontrollü kopya, emniyet sorumlusu |
| Ağ/VPN kuralları ve roller | Her onaylı değişiklikte | Erişimi sınırlı yedek, OT sorumlusu |
| Bakım ve olay günlükleri | Olayda hemen, rutin olarak günlük aktarım hedefi | Ayrı kayıt alanı, OT sorumlusu |

BAK-01 örnek kaydında cihaz ID, proje adı, sürüm, dosya özeti, oluşturma zamanı, sorumlu ve CHG numarası tutulur. Gizli bilgiler içeren yedekler şifreli saklanır. Gerçek yedek dosyaları ve parolalar herkese açık depoya konulmaz

Geri yüklemede önce güvenli makine durumu ve dosya bütünlüğü doğrulanır. Uyumluluk kontrolünden sonra yetkili kişi onaylı projeyi yükler. Hesaplar, ayarlar, çevrim, yeniden başlatma ve emniyet işlevleri kontrol edilir. Yerel onaydan sonra çalışma başlatılır

Saklama kararı, proje varsayımı olarak son üç onaylı sürüm ve olayla ilişkili sürümlerin korunmasıdır. Yedek oluşturma ve geri yükleme henüz uygulanmamıştır

[T08 kabul koşulları](../15-dogrulama-test/README.md)
