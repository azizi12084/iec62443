# Yama ve güncelleme

[Makine projesine dön](../README.md)

Yama kararı varlık, sürüm ve zafiyet etkisi üzerinden verilir. Güncelleme sonrası proses ve emniyet bağımlılıkları yeniden kontrol edilir

1. Üretici duyurusu ve ilgili V kaydı incelenir, etkilenme gerekçesi kaydedilir
2. Mevcut proje, yapılandırma ve sürüm bilgisi yedeklenir. Geri dönülecek sürümün uyumluluğu doğrulanır
3. Paket resmî kaynaktan alınır. Üretici imzası veya güvenilir kanaldan sağlanan bütünlük özeti kontrol edilir
4. Uygun test ortamında yükleme, çevrim ve emniyet testleri planlanır. Üretim geçişi başarılı doğrulamadan sonra onaylanır
5. Bakım penceresinde güncelleme uygulanır. T01–T03, T06 ve T09 değişiklik etkisine göre tekrarlanır
6. Envanter ve SBOM güncellenir, kanıtlar CHG kaydına bağlanır

Yama hemen uygulanamıyorsa etkilenen arayüz kısıtlanır, uzak erişim kapatılabilir ve izleme artırılır. Geçici kontrolün sorumlusu ve yeniden inceleme tarihi belirlenir

Örnek karar kaydı U-01, SW02 rol denetimi değişikliği içindir. İlgili zafiyet V01, değişiklik CHG-01, yedek BAK-01 ve kabul testi T06'dır. Gerçek paket ve sürüm seçimi beklenmektedir. Başarısızlıkta bakım durdurulur ve onaylı geri dönüş uygulanır

[Yedekleme](../12-yedekleme-geri-yukleme/README.md) · [Değişiklik yönetimi](../14-degisiklik-yonetimi/README.md)
