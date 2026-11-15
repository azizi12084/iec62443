# Yazılım bileşen listesi (SBOM)

[Makine projesine dön](../README.md)

SBOM, bir yazılımın bileşenlerini ve aralarındaki bağımlılıkları tanımlar. Bu proje için aşağıdaki liste, yazılım tasarımı ve üreticiden istenecek bileşen bilgisini eşleştirir. Kurulu yazılımdan üretilmiş envanterin hazırlanması ürün seçimine bağlıdır

| Bileşen ID | Ad | Üst öğe / ilişki | Tedarikçi | Sürüm ve kanıt |
| --- | --- | --- | --- | --- |
| B01 | Çevrim uygulaması | SW01 üzerinde çalışması planlanıyor | Proje uygulaması | Kod ve derleme henüz oluşturulmadı |
| B02 | Reçete sınırı kontrol mantığı | B01 parçası | Proje uygulaması | Tasarım gereksinimi, T06 ile doğrulanacak |
| B03 | HMI ekran ve rol projesi | SW02 runtime üzerinde çalışması planlanıyor | Proje uygulaması | Kod ve sürüm henüz oluşturulmadı |
| B04 | PLC üretici runtime/kütüphaneleri | SW01 bağımlılıkları | Seçilecek üretici | Üretici SBOM'u istenecek |
| B05 | HMI runtime/kütüphaneleri | SW02 bağımlılıkları | Seçilecek üretici | Üretici SBOM'u istenecek |
| B06 | VPN yazılım bağımlılıkları | SW05 bağımlılıkları | Seçilecek üretici | Üretici SBOM'u istenecek |

Toplanacak alanlar bileşen adı, tedarikçi, sürüm, benzersiz tanımlayıcı, bağımlılık ilişkisi, listeyi oluşturan kişi ve tarih bilgisidir. Sağlanabiliyorsa dosya özeti ve lisans bilgisi de eklenir

Bakım sorumlusu üreticinin SPDX veya CycloneDX çıktısını ilgili cihaz/sürümle eşleştirir. İç içe bağımlılıklar CVE taramasında değerlendirilir. Eşleşme bulunduğunda V kaydı açılır, gerçek kullanım ve erişim koşulu incelenir

[CISA SBOM FAQ](https://www.cisa.gov/sites/default/files/2024-07/SBOM%20FAQ%202024.pdf) · [Yazılım envanteri](../08-yazilim-firmware-envanteri/README.md)
