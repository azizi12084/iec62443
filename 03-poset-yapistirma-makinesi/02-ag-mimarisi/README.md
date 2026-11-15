# Ağ mimarisi

[Makine projesine dön](../README.md)

Hedef mimaride üretim, emniyet ve bakım üç ayrı bölge olarak ele alınır. Uzak bakım, yerel yetkilinin onayıyla açılan bir tasarım özelliğidir

```mermaid
flowchart TB
    R["Uzak bakım kullanıcısı"] --> G["VPN ve güvenlik duvarı"]
    subgraph Z3["Z3 · Bakım"]
        J["Jump server"] --> E["Mühendislik bilgisayarı"]
    end
    G --> J
    E -->|Onaylı hedef ve süre| F["OT güvenlik duvarı"]
    subgraph Z1["Z1 · Üretim"]
        H["HMI"] <--> P["Normal PLC"]
    end
    F --> H
    F --> P
    subgraph Z2["Z2 · Emniyet"]
        S["Işık perdesi ve acil durdurma"] --> C["Emniyet kontrolörü"]
        C --> V["Pnömatik emniyet sistemi"]
    end
    C -. Kablolu izin ve durum .-> P
```

Z2 kontrolörünün ağ üzerinden programlama bağlantısı hedef tasarımda kapalıdır. Yerel emniyet programlama ihtiyacı üretim durdurulmuşken ayrı onayla karşılanır. Normal PLC, emniyet iznini okuyabilir. Bu izin normal program tarafından geçersiz kılınamaz

VPN ve OT filtreleme işlevleri tek bir çok arayüzlü endüstriyel güvenlik duvarında veya iki cihazda uygulanabilir. Şema işlevleri gösterir. Ağ cihazı modeli ve protokol seçimi kurulum öncesi karardır

Saha sensörleri ve valflerin kabloları PLC giriş/çıkış bağlantılarıdır. Kablosuz ağ ve bulut bağlantısı bu proje kapsamında bulunmaz

[İzinli bağlantılar](../05-zone-conduit/README.md) · [Uzak erişim işlemi](../06-uzak-erisim/README.md)
