# Kullanıcı ve rol matrisi

[Makine projesine dön](../README.md)

Hesaplar kişiye özeldir. Rolün izin verdiği eylemler ayrıca görev ve bakım onayına bağlıdır

| İşlem | Operatör | Bakım/otomasyon | Emniyet sorumlusu | OT yöneticisi | Uzak servis |
| --- | --- | --- | --- | --- | --- |
| Durum görüntüleme | Evet | Evet | Evet | Evet | Onaylı oturum |
| Yerel çevrim başlatma | Evet | Test koşulunda | Test koşulunda | Hayır | Hayır |
| Onaylı reçete seçme | Evet | Evet | Hayır | Hayır | Hayır |
| Süre/reçete değiştirme | Hayır | Sınırlar içinde, onayla | Risk incelemesi | Hayır | Bakım gözetiminde, onayla |
| Normal PLC/HMI programı yükleme | Hayır | CHG onayıyla | Emniyet etkisini inceler | Hayır | Bakım gözetiminde, CHG onayıyla |
| Emniyet programı değiştirme | Hayır | Destek | Yerel, CHG onayıyla | Hayır | Hayır |
| Hesap ve ağ kuralı yönetme | Hayır | Talep | İnceleme | Onaylı değişiklikle | Hayır |
| Yerel emniyet reseti | Eğitim ve alan kontrolüyle | Eğitim ve alan kontrolüyle | Evet | Hayır | Hayır |

Acil durdurma fiziksel erişilebilir bir kumandadır ve kullanıcı girişine bağlı değildir. Süre değiştirme, yükleme ve hesap yönetimi kayıtları kişi adıyla tutulur. Hesaptan ayrılınca oturum kapanır; kullanıcı ayrıldığında hesabı devre dışı bırakılır

Yetkisiz süre değişikliği ve ayrıcalık kazanma denemesi T06 kapsamında kontrol edilir. Paylaşılan varsayılan hesaplar hedefte devre dışı bırakılır
