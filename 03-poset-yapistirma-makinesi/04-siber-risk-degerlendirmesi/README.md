# Siber risk değerlendirmesi

[Makine projesine dön](../README.md)

Bu değerlendirmede başlangıç durumundaki B1–B3 tasarım varsayımları kullanılır. Puanlar eğitim amaçlı tahminlerdir. L olasılık, S zarar şiddeti ve E maruziyet için 1–3 aralığı kullanılır. S=3 ölümcül etki senaryosu ayrıca önceliklendirilir

Skor = L × S × E. Ders föyündeki bantlar 1–3 düşük, 4–8 orta, 9–17 yüksek ve 18–27 kritik olarak uygulanmıştır. L için 1 düşük, 2 mümkün, 3 kolay tetiklenebilir; E için 1 bakım gibi seyrek, 2 dönemsel, 3 her çevrimde maruziyet kabul edilmiştir. S için 1 hafif, 2 ciddi yaralanma, 3 ölümcül etki kullanılmıştır

| Risk | Tehditten fiziksel sonuca uzanan senaryo | L | S | E | Skor | Öncelik |
| --- | --- | --- | --- | --- | --- | --- |
| R01 / V01 | Yerel kişi ortak HMI hesabıyla ısıtma süresini artırır → yüzey daha uzun sıcak kalır → koruyucu yetersizse temasta yanık | 3 | 2 | 3 | 18 | Kritik |
| R02 / V02 | Ele geçirilen uzak servis hesabı PLC çevrimini değiştirir → beklenmedik kapanma talebi oluşur → emniyet zinciri de etkisizse el sıkışır | 2 | 2 | 3 | 12 | Yüksek |
| R03 / V03 | Değiştirilmiş bakım dosyası PLC'ye yüklenir → açılma veya ısıtma sırası bozulur → koruyucular yetersizken müdahale edilirse sıkışma veya yanık | 2 | 2 | 2 | 8 | Orta |

Her senaryoda fiziksel yaralanma, belirtilen koruma koşuluna bağlıdır. Hedefte koruma çalışıyorsa beklenen sonuç üretimin durması, ürün kaybı veya reddedilen komuttur. Basınç ve sıcaklık seçilince S puanları yeniden incelenir

| Risk | Hedef önlemler | Sorumlu | Kapanış kanıtı | Kalan risk |
| --- | --- | --- | --- | --- |
| R01 | Kişisel roller, izinli ayar aralığı, sabit koruyucu ve EF3 | Otomasyon ve emniyet | T01, T03, T06 | Test sonrası yeniden puanlanacak |
| R02 | VPN/MFA, süreli oturum, Z2 ayrımı ve EF1–EF2 | OT güvenliği ve emniyet | T01, T02, T04, T05 | Test sonrası yeniden puanlanacak |
| R03 | Dosya kaynağı/bütünlük doğrulaması, onay, test ve geri dönüş | Bakım ve otomasyon | T07, T08, T09 | Test sonrası yeniden puanlanacak |

Mevcut kayıt kararı üç risk için de “Önlem planlandı, doğrulama bekleniyor”dur. Üretime kabul kararı test kanıtı ve sorumlu onayı gerektirir

[Zafiyetler](../10-zafiyet-kayitlari/README.md) · [Doğrulama](../15-dogrulama-test/README.md)
