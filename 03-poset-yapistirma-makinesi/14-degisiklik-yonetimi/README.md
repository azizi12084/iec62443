# Değişiklik yönetimi

[Makine projesine dön](../README.md)

Her değişiklik, talep eden kişi ve gerekçesiyle kaydedilir. Etkilenen varlık, risk, emniyet etkisi, yedek, test ve geri dönüş kararı aynı kayıtta bulunur

| Alan | CHG-01 örnek kaydı |
| --- | --- |
| Talep | HMI süre ayarı için ortak hesabın kaldırılması ve rol ayrımı |
| Gerekçe | V01 ve R01 |
| Etkilenen öğeler | A02/SW02 ve A01/SW01 ayar sınırları |
| Değişiklik | Operatör onaylı reçeteyi seçer, bakım yetkili sınırlar içinde değiştirir |
| Emniyet etkisi | Süre sınırları, ısıtma davranışı ve EF3 ile bağımlılık incelenir |
| Yedek | BAK-01, değişiklik öncesi onaylı proje |
| Test | T06, T03 ve çevrim doğrulaması T09 |
| Geri dönüş | Test başarısızsa üretime geçilmez, doğrulanmış yedek geri yüklenir |
| Uygulayan | Bakım/otomasyon rolü, gerçek kişi uygulamada atanacak |
| Onay | Emniyet etkisi için emniyet sorumlusu, erişim için OT sorumlusu |
| Durum | Öneri, uygulanmadı |

Uygulama sonrası eski/yeni sürüm, tarih, yapan kişi ve test sonuçları kaydedilir. Risk, envanter, SBOM ve yedek kayıtları güncellenir. Acil değişiklikte de sorumlu, gerekçe, ilk kontroller ve sonradan tamamlanacak doğrulama kaydedilir

[Yama akışı](../11-yama-guncelleme/README.md) · [Test planı](../15-dogrulama-test/README.md)
