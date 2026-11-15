# Olay müdahalesi

[Makine projesine dön](../README.md)

Örnek olay IR-01, HMI üzerinde onaysız süre değişikliği görülmesidir. V01 ve R01 kayıtlarıyla ilişkilidir. Aşağıdaki akış masa başı olay planıdır

| Aşama | Yapılacak işlem | Sorumlu ve kanıt |
| --- | --- | --- |
| Tespit | Değişikliğin zamanı, eski/yeni değer, hesap ve makine durumu kaydedilir | Operatör, ekran/olay kaydı |
| İlk müdahale | Tehlike varsa yerel güvenli durdurma uygulanır. Şüpheli uzak oturum kapatılır | Operatör ve OT sorumlusu |
| Sınırlama | Şüpheli hesap devre dışı bırakılır, hedef cihazın bakım erişimi kısıtlanır | OT sorumlusu, erişim kaydı |
| İnceleme | HMI, PLC, VPN ve jump server kayıtları korunur, onaylı projeyle fark incelenir | Otomasyon, zaman damgalı kopyalar |
| Düzeltme | Yetki açığı giderilir, gerekirse doğrulanmış yedek geri yüklenir | Bakım, CHG ve BAK kaydı |
| Geri dönüş | Ayarlar ve ilgili emniyet işlevleri doğrulanır, yerel yetkili çalışmayı başlatır | Emniyet ve bakım, T01–T03/T06 |
| Kapanış | Kök neden, etki, belirsizlikler ve kalıcı önlemler kaydedilir | Olay sorumlusu, güncel risk kaydı |

Kanıtın kim tarafından ne zaman alındığı ve nerede saklandığı yazılır. Makineyi güvenli tutma önceliği korunarak kayıtlar alınır. Kurcalanan ayarı geri çevirmeden önce mevcut değer ve ilgili kayıtlar saklanır

Bildirim tarafları yerel bakım, emniyet, OT sorumlusu ve gerekiyorsa üreticidir. Dış bildirim yükümlülükleri gerçek ürün ve işletmenin kapsamına göre değerlendirilir. Bu plan için yasal süre iddiası veya gerçekleşmiş olay kaydı oluşturulmamıştır
