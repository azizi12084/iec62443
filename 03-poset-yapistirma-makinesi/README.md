# Yarı Otomatik Pnömatik Poşet Isıl Yapıştırma Makinesi

**Hazırlayan — Muhammed Azizi · Grup — Gündüz / B**

## Amaç ve çalışma çevrimi

Operatör plastik poşetin ağzını çenelerin arasına yerleştirir ve yerel başlatma butonuna basar. Normal PLC, emniyet izni mevcutsa pnömatik çeneyi kapatır. Yapıştırma ve soğutma adımlarından sonra çene açılır ve operatör poşeti alır. HMI çevrim durumunu ve ayarları gösterir

Yarı otomatik çalışma, poşetin yerleştirilmesi ve alınmasının operatöre ait olduğunu ifade eder. Basınçlı hava çeneyi hareket ettirir, ısı ve basınç poşet ağzının birleşmesini sağlar

## Tasarım kapsamı ve varsayımlar

Bu dosyadaki makine kurgusaldır. Başlangıç durumuna ilişkin B1–B3 varsayımları, üç zafiyet senaryosunun incelenebilmesi için tanımlanmıştır. Hedef mimari bu zafiyetleri gidermeyi amaçlar

| Kod | Tasarım kararı veya varsayım |
| --- | --- |
| A1 | Çevrim kontrolünde normal PLC, HMI, sıcaklık ve çene konum sensörleri kullanılır |
| A2 | Emniyet ışık perdesi ve acil durdurma, ayrı bir emniyet kontrolörüne kablolu bağlanır. Emniyet programına uzaktan erişim kapalıdır |
| A3 | Çene hareketinin pnömatik durdurma yöntemi, durma süresi ve koruyucu açıklıkları donanım seçimiyle doğrulanacaktır |
| A4 | Bakım için yerel bir mühendislik bilgisayarı ve kontrollü uzak destek yolu tasarıma eklenmiştir |
| A5 | Hedefte sıcaklık sınır aşımında ısıtıcı enerjisini kesen bağımsız bir sınırlayıcı ve kesme elemanı öngörülür. Ayarı ve güvenilirliği donanım incelemesiyle belirlenecektir |
| B1 | Başlangıç senaryosunda HMI ayar hesabı ortak kullanılır ve operatörün süre değiştirme yetkisi sınırsızdır |
| B2 | Başlangıç senaryosunda uzak servis üretim ağına doğrudan ulaşabilir, ikinci doğrulama yoktur |
| B3 | Başlangıç senaryosunda bakım projesi dosyasının kaynağı ve bütünlüğü yüklemeden önce kontrol edilmez |

Marka, model, firmware sürümü, çalışma sıcaklığı, basınç ve kapasite henüz seçilmemiştir. Bu alanlar envanterde açıkça belirtilmiştir. Güvenlik seviyesi (SL-T) ile emniyet performans hedefi (PLr/SIL) ayrıntılı değerlendirme gerektirir

## Belgeler

[SWOT analizi](SWOT_Analizi.md) · [Kaynaklar](Kaynaklar.md)

| No | Siber güvenlik eki |
| --- | --- |
| 01 | [Varlık envanteri](01-varlik-envanteri/README.md) |
| 02 | [Ağ mimarisi](02-ag-mimarisi/README.md) |
| 03 | [Emniyet fonksiyonları](03-emniyet-fonksiyonlari/README.md) |
| 04 | [Siber risk değerlendirmesi](04-siber-risk-degerlendirmesi/README.md) |
| 05 | [Zone ve conduit](05-zone-conduit/README.md) |
| 06 | [Uzak erişim](06-uzak-erisim/README.md) |
| 07 | [Kullanıcı ve rol matrisi](07-kullanici-rol-matrisi/README.md) |
| 08 | [Yazılım ve firmware envanteri](08-yazilim-firmware-envanteri/README.md) |
| 09 | [Yazılım bileşen listesi (SBOM)](09-sbom/README.md) |
| 10 | [Zafiyet kayıtları](10-zafiyet-kayitlari/README.md) |
| 11 | [Yama ve güncelleme](11-yama-guncelleme/README.md) |
| 12 | [Yedekleme ve geri yükleme](12-yedekleme-geri-yukleme/README.md) |
| 13 | [Olay müdahalesi](13-olay-mudahalesi/README.md) |
| 14 | [Değişiklik yönetimi](14-degisiklik-yonetimi/README.md) |
| 15 | [Doğrulama ve test](15-dogrulama-test/README.md) |

## Kanıt durumu

15 klasörün her birinde makineye uyarlanmış analiz, tasarım veya prosedür bulunur. Test dosyasındaki sonuç alanları “Planlandı” durumundadır. Gerçek cihaz taraması, yazılım kurulumu ve fiziksel doğrulama yapılmamıştır. SBOM için üretici bileşen verileri ve CVE eşleştirmesi için ürün/sürüm bilgileri gereklidir

Klasör yapısı proje için benimsenen 15 başlığa göre hazırlanmıştır. Dersin resmî teslim şablonu elde edildiğinde başlık ve sıralama karşılaştırılacaktır

## Görsel referanslar

[![Audion Power Sealer PLUS 720 ön görünümü](https://www.audion.com/media/delnpmt0/powersealer-plus-720-front.jpg?height=188&v=1db0056d831ee60&width=335)](https://www.audion.com/uk/products/power-sealer-plus)

**Audion Power Sealer PLUS 720.** Poşet girişinin, yapıştırma çenesinin ve operatör ekranının yerleşimine örnek.

[![IMPAK iS2 yapıştırma ayarları ekranı](https://www.impakcorporation.com/image/data/Case%20study/dual-element-control1.png)](https://www.impakcorporation.com/multiple-seal-widths)

**IMPAK iS2.** Yapıştırma ayarlarının bir operatör ekranından nasıl seçilebildiğine örnek. Görseller üreticilerin örnek makinelerine aittir.
