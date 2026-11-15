# Doğrulama ve test

[Makine projesine dön](../README.md)

Bu tablo kabul testlerinin planıdır. Donanım ölçümleri ve fiilî uygulama sonuçları henüz mevcut değildir. Fiziksel emniyet testleri uygun test araçlarıyla yetkili kişi tarafından yürütülür

| Test | İlgili öğe | Senaryo | Kabul koşulu | Durum |
| --- | --- | --- | --- | --- |
| T01 | EF1 / R02 | Algılama alanını başlatma öncesinde ve kapanma sırasında test parçasıyla kesmek | Başlatma engellenir veya çene elin erişim süresinden önce durur; alan açılması otomatik başlatmaz | Planlandı |
| T02 | EF2 | Çevrimde acil durdurma, sonra butonu serbest bırakma | Tehlikeli hareket durur, ısıtıcı beslemesi kesilir, yeni başlatma gerekir | Planlandı |
| T03 | H2 / EF3 / R01 | Koruyucu açıklığı ve aşırı sıcaklık algılamasını uygun yöntemle incelemek | Sıcak yüzeye erişim önlenir; bağımsız sınır aşımında ısıtıcı kesilir | Planlandı |
| T04 | V02 / C01–C03 | Dış ağdan doğrudan erişim, yanlış doğrulama ve süresi dolmuş oturum denemesi | Z1 doğrudan erişim engelli, MFA gerekli, süre sonunda oturum sonlanır | Planlandı |
| T05 | Z2 ayrımı / R02 | Z1/Z3'ten emniyet programına erişim denemesi, normal PLC'den uygunsuz kapanma talebi | Programlama yolu erişilemez, emniyet zinciri talebi engeller | Planlandı |
| T06 | V01 / CHG-01 | Operatör hesabıyla süre değiştirmek, bakım hesabıyla sınır dışı değer girmek | Yetkisiz ve sınır dışı değişiklik reddedilir, kullanıcı/zaman kaydı oluşur | Planlandı |
| T07 | V03 | Kaynağı belirsiz veya özeti uyuşmayan bakım dosyası sunmak | Dosya kabul sürecinde reddedilir, yükleme yapılmaz | Planlandı |
| T08 | BAK-01 | Uygun test ortamında onaylı yedeği geri yüklemek | Program, ayarlar ve roller eşleşir; çevrim/emniyet kontrolleri başarılıdır; süre ölçülür | Planlandı |
| T09 | SW01 / R03 | Normal çevrim, haberleşme kaybı ve güç geri gelmesi | Sıra doğru, kayıpta tanımlı duruş, dönüşte yerel yeni başlatma gerekir | Planlandı |
| T10 | H3 | Enerji yalıtım prosedürünü yetkili kişiyle doğrulamak | Kaynaklar kilitli, kalan enerji kontrol altında, çene hareket edemez, sıcaklık güvenli | Planlandı |
| T11 | IR-01 | Onaysız süre değişikliği için masa başı olay tatbikatı | Tespit, erişim kesme, kanıt ve geri dönüş sorumluları doğru sırayla çalışır | Planlandı |

Sonuç kaydında test ID, tarih, cihaz/yazılım sürümü, test eden kişi, beklenen ve gerçekleşen sonuç, kanıt bağlantısı ve sapma bulunur. Başarısızlık varsa ilgili V/R/CHG kaydı açık kalır. Yeni test sonucu önceki sonucun geçmişini koruyarak eklenir

Belge paketi hazırlanırken yerel dosya bağlantıları, 15 klasörün varlığı ve risk–zafiyet–test referansları kontrol edilmiştir. Bu belge kontrolleri fiziksel makine doğrulamasından ayrı bir kanıt türüdür
