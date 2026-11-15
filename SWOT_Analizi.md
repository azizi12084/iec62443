# Yarı Otomatik Pnömatik Poşet Isıl Yapıştırma Makinesi — SWOT Analizi

Bu çalışma, ders projesi için tasarlanan kurgusal bir makineyi ele alır. Operatör poşeti yerleştirip çevrimi başlatır. PLC, pnömatik çenenin kapanmasını, ısıl yapıştırmayı ve soğutmayı yönetir. Çene açıldığında operatör poşeti alır. Yapıştırma süresi HMI üzerinden ayarlanır.

| Başlık | Etken | Makineye etkisi |
| --- | --- | --- |
| **Güçlü yön (G1)** | PLC ile sıralı çevrim kontrolü | Kapatma, yapıştırma, soğutma ve açma adımları belirli bir sırada yürütülür. Bu sayede çevrim adımları ayrı ayrı gözlemlenebilir ve test edilebilir. |
| **Güçlü yön (G2)** | HMI üzerinden ayarlanabilir yapıştırma süresi | Poşet tipi değiştiğinde uygun çalışma ayarı arayüzden uygulanabilir. |
| **Zayıf yön (Z1)** | Poşetin elle yerleştirilmesi | Operatörün eli sıcak ve hareketli çeneye yaklaşır. Poşet ağzı eğik yerleştirilirse yapıştırma da düzensiz olabilir. |
| **Zayıf yön (Z2)** | HMI ayarlarını kimlerin değiştirebileceğinin henüz tanımlanmamış olması | Tasarımda operatörün ve yetkili personelin erişebileceği ayarlar belirlenmelidir. |
| **Fırsat (F1)** | Benzer ticari makineler için üretici kaynaklarının bulunması | Poşet girişinin ve operatör arayüzünün yerleşimi için karşılaştırma örnekleri sağlar. |
| **Fırsat (F2)** | Küçük ölçekli paketleme atölyelerinde olası kullanım | Elle beslemeyi sürdüren ve kapatma işlemini standartlaştırmak isteyen atölyeler olası bir kullanım alanıdır. |
| **Tehdit (T1)** | Tedarik edilen poşetlerin kalınlığının partiden partiye değişmesi | Önceki ayarlar yeni partide kullanılırsa yapıştırma yeterli olmayabilir. |
| **Tehdit (T2)** | Yetkisiz bir kişinin operatör ekranından süreyi değiştirmeye çalışması | Değişiklik başarılı olursa poşet yeterince kapanmayabilir. Senaryo, kişinin ekrana erişebildiği varsayımına dayanır. |

## Analizden çıkan tasarım kararları

- **Makine emniyeti (Z1 + F1).** Çenenin, operatörün eli yapıştırma bölgesindeyken kapanmasını önlemek bir tasarım hedefidir. Benzer makineler poşet girişinin yerleşimini incelemek için referans olarak kullanılacaktır. Koruma yöntemi, emniyet fonksiyonları çalışmasında belirlenecektir.
- **Siber güvenlik (G2 + Z2 + T2).** Yapıştırma süresini değiştirme yetkisinin yetkili rolle sınırlandırılması ve değişikliklerin kaydedilmesi önerilir. Bu öneri, ayar değiştirme yetkisi bulunmayan bir hesapla yapıştırma süresi değiştirilmeye çalışılarak sınanabilir.
- **Proses kalitesi (G1 + G2 + T1).** Yeni bir poşet partisi geldiğinde üretime başlamadan önce numune üzerinde yapıştırma kontrolü yapılması önerilir. Testte kullanılan süre ve sonuç kaydedilerek yeni partinin ayarı belirlenebilir.
