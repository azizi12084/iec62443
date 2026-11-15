# Uzak erişim

[Makine projesine dön](../README.md)

Uzak bakımın amacı HMI/PLC arızalarının incelenmesi ve onaylı normal kontrol güncellemeleridir. Erişim varsayılan kapalıdır

1. Bakım talebinde kişi, gerekçe, hedef cihaz, yapılacak işlem ve başlangıç/bitiş zamanı yazılır
2. Yerel bakım sorumlusu üretim durumunu kontrol eder. Hareket veya program değişikliği gerektiren bakım için makine uygun güvenli duruma alınır
3. OT sorumlusu kişisel hesabı ve ikinci doğrulamayı kontrol ederek VPN yolunu açar
4. Kullanıcı jump server üzerinden mühendislik bilgisayarına bağlanır. Yalnız onaylı Z1 hedeflerine erişir
5. Oturum zamanı, erişilen cihazlar, dosya aktarımı ve değişiklikler kaydedilir. Yerel görevli bakım boyunca ulaşılabilirdir
6. Süre sonunda erişim otomatik sona erer. Yerel görevli kontrolleri doğrular ve gerekiyorsa üretimi yerel başlatma komutuyla açar

Oturum örneği, planlanan kayıt

| Alan | Değer |
| --- | --- |
| Talep | RA-01 |
| Amaç | A02 HMI ayar-yetki sorununu incelemek |
| Yetki | Görüntüleme, yükleme için ayrı CHG onayı |
| Süre | Onaylanan bakım penceresi, bitişte otomatik kapatma |
| Kanıt | Kullanıcı, giriş/çıkış zamanı, hedef ve yapılan işlemler |
| Durum | Tasarım örneği, oturum açılmadı |

Şüpheli işlemde uzak oturum kesilir, makine durumu yerel olarak değerlendirilir ve olay kaydı açılır. Emniyet programı değiştirme ve emniyet reseti yerel yetkili işlemidir

[Roller](../07-kullanici-rol-matrisi/README.md) · [Olay müdahalesi](../13-olay-mudahalesi/README.md)
