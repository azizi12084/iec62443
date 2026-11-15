# Aday Bileşenler İçin CVE Analizi

Bu çalışma, kurgusal poşet ısıl yapıştırma makinesinin üç varlığı için yayımlanmış güvenlik açıklarını inceler. Siemens ürünleri, tasarımda ilgili işlevi yerine getirebilecek örnek adaylar olarak seçildi. Her eşleştirme ürün, sürüm ve erişim koşuluna bağlıdır. Ürün seçimi ve saha doğrulaması bekleniyor.

[Zafiyet kayıtları](README.md) · [Yazılım envanteri](../08-yazilim-firmware-envanteri/README.md) · [Risk değerlendirmesi](../04-siber-risk-degerlendirmesi/README.md)

| CVE | Aday bileşen ve varlık | Etkilenen sürüm | Üreticinin bildirdiği düzeltme | İlgili risk |
| --- | --- | --- | --- | --- |
| CVE-2026-27662 | SIMATIC HMI MTP700 Unified Comfort Panel (6AV2128-3GB06-0AX1), A02 / SW02 | V21 öncesi | V21 veya sonrası | R01 |
| CVE-2022-32251 | SINEMA Remote Connect Server, A10 / SW05 için uzak erişim altyapısı adayı | V3.1 öncesi | V3.1 veya sonrası | R02 |
| CVE-2025-40759 | SIMATIC STEP 7 V20 (TIA Portal), A09 / SW04 üzerindeki mühendislik yazılımı adayı | V20 Update 4 öncesindeki V20 sürümleri | V20 Update 4 veya sonrası | R03 |

Düzeltme sürümleri, tabloda belirtilen CVE ve ürün için üreticinin bildirdiği alt sınırlardır. Kurulumda uyumlu ve desteklenen sürüm seçilir.

## CVE-2026-27662 — Operatör paneli

- **Önkoşul ve etki.** Etkilenen sürümde, uygun erişim koruması bulunmadığında panelin kontrol ekranından web tarayıcısına yetkisiz ulaşılabilir. Makinede bunun reçete değişikliğine dönüşmesi, tarayıcıdan yazılabilir bir arayüze erişilebilmesine ve PLC sınır kontrollerine bağlıdır. Açığın duyurulan doğrudan etkisi tarayıcı erişimidir.
- **Karar ve doğrulama.** Panelin sipariş numarası ve sistem sürümü kaydedilir. Düzeltme kurulumundan sonra kontrol paneli erişim koruması ve görev çubuğu ayarı kontrol edilir. Operatör hesabıyla reçete kısıtları ayrıca T06 kapsamında doğrulanır. R01 kapsamında sıcak yüzeye erişim ve EF3 kontrolleri T03 ile ele alınır.
- [Siemens ProductCERT · SSA-387223](https://cert-portal.siemens.com/productcert/html/ssa-387223.html)

## CVE-2022-32251 — Uzak erişim sunucusu

- **Önkoşul ve etki.** Etkilenen sunucuya erişebilen düşük yetkili bir kullanıcı, eksik doğrulama nedeniyle rol ve izinleri değiştirerek yönetici yetkisi kazanabilir. Üretim ağına ilerleyebilmesi, ayrı OT güvenlik duvarının ve hedef kısıtlarının durumuna bağlıdır. Emniyet kontrolörüne doğrudan erişim için hedef tasarımda ağ yolu tanımlanmamıştır.
- **Karar ve doğrulama.** Sunucu sürümü ve erişilebilirliği kontrol edilir. Etkilenen kurulumda güncelleme uygulanana kadar servis erişimi kısıtlanır. Güncellemeden sonra düşük yetkili hesabın yönetici işlemlerini yapamadığı ve uzak erişim yolunun hedeflerle sınırlı olduğu test ortamında doğrulanır. T04 ve T05 ağ kontrollerine bağlanır.
- [Siemens ProductCERT · SSA-484086](https://cert-portal.siemens.com/productcert/html/ssa-484086.html)

## CVE-2025-40759 — Mühendislik bilgisayarı

- **Önkoşul ve etki.** Etkilenen STEP 7 sürümü güvensiz bir proje dosyasını işlerken saldırgan kodu mühendislik uygulamasında çalışabilir. Değiştirilmiş mantığın PLC'ye ulaşması ayrıca yükleme yetkisine, ağ erişimine ve bakım onayına bağlıdır.
- **Karar ve doğrulama.** STEP 7 sürümü ile güncelleme seviyesi doğrulanır. Yalnız güvenilir kaynaktan gelen proje dosyaları kullanılır. Güncelleme sonrası onaylı bir proje kopyası test ortamında açılır. Kaynağı veya bütünlüğü doğrulanamayan dosyanın açılmadan reddedildiği T07 kapsamında kontrol edilir.
- [Siemens ProductCERT · SSA-493396](https://cert-portal.siemens.com/productcert/html/ssa-493396.html)

## Risk kaydına aktarma

V01–V03, makinenin başlangıç tasarımındaki zayıflıkları ifade eder. CVE kayıtları, belirli üretici ürünlerindeki yayımlanmış açıkları ve bunların R01–R03 ile ilişkisini gösterir. Uygulamada ürün ve sürüm eşleşirse, erişim koşulu ayrıca değerlendirilir ve sonuç R kaydına tarih, kanıt, sorumlu ve düzeltme kararıyla eklenir. Üç CVE için mevcut proje durumu **aday eşleşme, saha doğrulaması bekleniyor**.
