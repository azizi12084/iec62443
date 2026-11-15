# Zafiyet kayıtları

[Makine projesine dön](../README.md)

Aşağıdaki üç zafiyet, başlangıç tasarım varsayımlarının analizidir. V01–V03 proje içi kayıt numaralarıdır. CVE eşleştirmesi, seçilmiş gerçek ürün ve sürüm için daha sonra yapılacaktır

| Kayıt | Zafiyet ve geçerlilik koşulu | Etkilenen varlık | Etki ve karar |
| --- | --- | --- | --- |
| V01 | B1 geçerliyse ortak HMI hesabı ile sınırsız süre değişikliği | A02, A01 / SW02, SW01 | Yetkisiz reçete değişikliği ve ürün kaybı; R01 koşulunda yanık. Rol ayrımı ve PLC tarafında ayar sınırı uygulanmalı |
| V02 | B2 geçerliyse uzak servis hesabından Z1'e doğrudan erişim ve MFA eksikliği | A10, A09, A01 | Hesap ele geçirilirse program değişikliği veya duruş; R02 koşulunda sıkışma. Erişim kapatılıp kontrollü bakım yolu kurulmalı |
| V03 | B3 geçerliyse doğrulanmamış bakım projesi yükleme | A09, A01 / SW04, SW01 | Değiştirilmiş mantık yüklenebilir; R03 koşulunda yaralanma. Kaynak, bütünlük, test ve onay zorunlu hale getirilmeli |

| Kayıt | Geçerlilik incelemesi | Düzeltme doğrulaması | Durum |
| --- | --- | --- | --- |
| V01 | Hesap/rol listesi ve yazılabilir ayar alanları | T06, ardından T01 ve T03 | Varsayımsal başlangıç bulgusu, önlem planlandı |
| V02 | Ağ kuralları ve oturum açma yöntemi | T04 ve T05 | Varsayımsal başlangıç bulgusu, önlem planlandı |
| V03 | Dosya kabul ve yükleme süreci | T07 ve T08 | Varsayımsal başlangıç bulgusu, önlem planlandı |

## CVE kaydı geldiğinde karar

Bakım sorumlusu üretici duyurusundaki ürün ve etkilenen sürüm aralığını SW envanteriyle karşılaştırır. Etkilenen özellik etkin mi, saldırı yolu erişilebilir mi ve telafi edici kontrol var mı soruları cevaplanır. Kayda CVE numarası, duyuru bağlantısı, inceleme tarihi, etki kararı ve sorumlu eklenir

Etkilenme belirsizse kayıt incelemede kalır. Etkilenme doğrulanırsa R kaydına bağlanır ve yama veya geçici azaltım kararı verilir. Sayısal CVSS tek başına fiziksel risk puanının yerini almaz

[Risk kaydı](../04-siber-risk-degerlendirmesi/README.md) · [Yama süreci](../11-yama-guncelleme/README.md)
