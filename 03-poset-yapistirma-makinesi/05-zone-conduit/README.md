# Zone ve conduit

[Makine projesine dön](../README.md)

Zone, benzer güvenlik gereksinimlerine sahip varlık grubudur. Conduit, bölgeler arasında izin verilen iletişim yollarını ve bunların koruma koşullarını kapsar. Projenin bölgelemesi hedef mimaridir

| Bölge | Kapsam | İhtiyaç |
| --- | --- | --- |
| Z1 Üretim | A01, A02, A07, A12 | Çevrim ve reçete bütünlüğü, çalışma sürekliliği |
| Z2 Emniyet | A03–A06, A08 | Tehlikeli hareket ve sıcaklığa karşı koruma |
| Z3 Bakım | A09–A11 | Yetkili ve izlenebilir bakım |
| Dış taraf | Uzak servis bilgisayarı | Kimlik doğrulama ve sınırlı erişim |

| Yol | Kaynak → hedef | İzin ve sınır |
| --- | --- | --- |
| C01 | Dış taraf → VPN → jump server | Kişisel hesap, MFA, yerel onay, süreli oturum |
| C02 | Jump server → mühendislik bilgisayarı | Tek onaylı bakım oturumu, işlem kaydı |
| C03 | Mühendislik bilgisayarı → Z1 PLC/HMI | Bakım penceresinde belirlenen hedef ve servis; diğer erişimler engelli |
| C04 | HMI ↔ normal PLC, Z1 içi | Gerekli proses verileri; reçete alanları rol ve sınır kontrolüne tabi |
| C05 | Z2 → normal PLC | Kablolu izin/durum, emniyet programına yazma yetkisi sağlamaz |

Z1 veya Z3'ten Z2'ye ağ üzerinden programlama yolu tanımlanmamıştır. Fiziksel servis bağlantısı kilitli panoda tutulur ve yerel onayla kullanılır. Z1'e dış ağdan doğrudan erişim kapalıdır

Port numaraları üretici ve servis seçildikten sonra izin listesine eklenir. Kuralın kaynağı, hedefi, amacı, sorumlusu ve geçerlilik süresi kayıt altına alınır. SL-T belirlemek için bu bölgelere yönelik ayrıntılı tehdit ve risk değerlendirmesi gerekir

[Ağ şeması](../02-ag-mimarisi/README.md) · [Kaynaklar](../Kaynaklar.md)
