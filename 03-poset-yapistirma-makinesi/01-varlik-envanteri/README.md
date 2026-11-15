# Varlık envanteri

[Makine projesine dön](../README.md)

Her satır hedef tasarımda kullanılan bir varlığı gösterir. Bakım sorumlusu envanteri her onaylı değişiklikte günceller

| ID | Varlık | Görev ve korunacak bilgi | Bölge | Sorumlu |
| --- | --- | --- | --- | --- |
| A01 | Normal PLC | Çevrim programı ve reçete sınırları | Z1 | Otomasyon |
| A02 | HMI | Operatör oturumu, süre ayarı ve olay kayıtları | Z1 | Otomasyon |
| A03 | Emniyet kontrolörü | EF1–EF2 mantığı ve yeniden başlatma kilidi | Z2 | Emniyet |
| A04 | Emniyet ışık perdesi | Girişte algılama | Z2 | Emniyet |
| A05 | Acil durdurma ve yerel reset | Emniyet durdurma talebi ve yeniden etkinleştirme | Z2 | Emniyet |
| A06 | Pnömatik emniyet elemanları ve silindir | Çenenin hareketinin güvenli durdurulması | Z2 / saha | Emniyet |
| A07 | Isıtıcı, sıcaklık ve konum sensörleri | Normal proses kontrolü | Z1 / saha | Bakım |
| A08 | Bağımsız sıcaklık sınırlayıcı ve kesme elemanı | Sınır aşımında ısıtıcı enerjisini kesme | Z2 / saha | Emniyet |
| A09 | Mühendislik bilgisayarı | Proje dosyaları ve onaylı yükleme aracı | Z3 | Otomasyon |
| A10 | VPN ağ geçidi ve güvenlik duvarı | Oturum doğrulama ve trafik kuralları | Z3 sınırı | OT güvenliği |
| A11 | Jump server | Uzak bakım oturumunun denetimi | Z3 | OT güvenliği |
| A12 | Anahtar ve ağ kablolaması | Z1 bağlantıları | Z1 | OT güvenliği |
| A13 | Çevrimdışı yedek ortamı | Onaylı program ve yapılandırma kopyaları | Güvenli yerel saklama | Bakım |

PLC/HMI programları, ayar dosyaları, hesap listesi, bakım kayıtları ve emniyet projesi kritik dijital varlıklardır. Model, seri numarası, firmware sürümü ve yedek bütünlük özeti kurulumda bu kayıtlarla eşleştirilir

[Yazılım envanteri](../08-yazilim-firmware-envanteri/README.md) · [Bölge eşleştirmesi](../05-zone-conduit/README.md)
