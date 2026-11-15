# Yazılım ve firmware envanteri

[Makine projesine dön](../README.md)

Bu envanter cihaz üzerinde çalışması planlanan yazılım türlerini gösterir. Gerçek ürün seçimi yapılınca üretici bilgisi, sürüm, destek durumu ve bütünlük özeti aynı satırda tamamlanır

| Yazılım ID | Varlık | Yazılım | Sürüm/kaynak durumu | Yedeklenecek öğe |
| --- | --- | --- | --- | --- |
| SW01 | A01 | PLC firmware ve çevrim uygulaması | Ürün seçilmedi, uygulama tasarımı mevcut | Proje, reçete sınırları, cihaz konfigürasyonu |
| SW02 | A02 | HMI runtime ve ekran projesi | Ürün seçilmedi | Ekranlar, roller, ayarlar |
| SW03 | A03 | Emniyet firmware ve programı | Ürün seçilmedi | Onaylı emniyet projesi ve doğrulama özeti |
| SW04 | A09 | İşletim sistemi ve mühendislik aracı | Platform seçilmedi | Kurulum listesi, sürüm ve lisans bilgisi |
| SW05 | A10 | VPN ve güvenlik duvarı firmware | Ürün seçilmedi | Filtre kuralları ve hesap yapılandırması |
| SW06 | A11 | Jump server işletim sistemi ve oturum aracı | Platform seçilmedi | Erişim politikası, denetim kayıtları |

Vulnerability kontrolü için yalnız yazılım adı yeterli değildir. Ürün/versiyon, etkin özellik ve erişilebilir arayüz birlikte kontrol edilir. Kurulumda bakım sorumlusu sürüm ekranını veya üretici çıktısını kanıt olarak kaydeder

[SBOM](../09-sbom/README.md) · [Zafiyet kayıtları](../10-zafiyet-kayitlari/README.md)
