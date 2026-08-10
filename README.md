# Dardania — Cinnamon uyarlaması

[ShalaOS](https://github.com/edizsale/shalaos)'un KDE Plasma için tasarlanan **dardania**
temasının Cinnamon masaüstüne uyarlanmış hâli: koyu zemin, kırmızı vurgu
(`rgb(228, 20, 30)`). Renk paleti, KDE tarafındaki `DardaniaDark.colors` dosyasıyla
birebir aynı — iki masaüstünde de aynı "dardania" kimliği.

Bu tema iki parçadan oluşur:

- **`gtk-3.0/`** — GTK3 uygulamalarının kontrolleri (düğme, giriş kutusu, menü vb.)
- **`cinnamon/`** — Cinnamon kabuğu (panel, başlat menüsü, bildirimler, takvim, OSD)

## Dahil OLMAYAN şey: pencere kenarlığı ve düğmeleri

Bilinçli bir tercih: bu tema **Muffin/Metacity pencere dekorasyonuna dokunmuyor**.
Küçült/büyüt/kapat düğmeleri ve pencere kenarlığı, sistemde hâlâ ayarlı olan tema neyse
onu kullanmaya devam eder. Cinnamon Ayarları → Temalar'da **"Pencere Kenarlıkları"**
seçeneğini değiştirmene gerek yok (değiştirmek de istemiyorsan hiç dokunma).

## Kurulum

```bash
git clone https://github.com/edizsale/dardania-cinnamon.git
mkdir -p ~/.themes
cp -r dardania-cinnamon ~/.themes/Dardania
```

Sonra **Cinnamon Ayarları → Temalar**'ı aç:

- **Kontroller (Controls):** Dardania
- **Masaüstü (Desktop):** Dardania
- **Pencere Kenarlıkları (Window borders):** dokunma, olduğu gibi bırak

Değişiklik anında uygulanır, oturum yeniden başlatmaya gerek yok.

## Bilinen sınırlamalar

- **Görsel olarak test edilmedi.** Bu tema, KDE tarafındaki gerçek renk değerlerinden
  yola çıkılarak GTK3/Cinnamon CSS'i olarak elle yazıldı; canlı bir Cinnamon ortamında
  render edilip gözle kontrol edilmedi. Çalışan uygulamaların çoğunda (panel, menü,
  düğmeler, giriş kutuları, bildirimler) doğru görünmesi beklenir, ama bazı applet'lerde
  veya nadir kullanılan diyaloglarda varsayılan görünüm sızabilir.
- **Simge teması ve imleç teması dahil değil** — yalnızca renk/kontrol teması. İstersen
  ayrı bir simge temasıyla (ör. Papirus, Qogir) birlikte kullanabilirsin.
- **Yalnızca GTK3.** Çoğu Cinnamon uygulaması ve kabuğun kendisi GTK3/St tabanlı olduğu
  için bu yeterli olmalı; GTK4/libadwaita uygulamaları (varsa) bu temayı kullanmaz.
- Bir şey bozuk/çirkin görünüyorsa ekran görüntüsüyle bildir — hangi uygulama/pencere
  olduğunu bilmek düzeltmeyi kolaylaştırır.

## Kaynak

Renk paleti: [`edizsale/dardania`](https://github.com/edizsale/dardania) (KDE Plasma
dardania teması, private repo) → `color-schemes/DardaniaDark.colors`.

## Lisans

GPL-3.0 — bkz. [`LICENSE`](LICENSE). İsim ve renk paleti ShalaOS/dardania kimliğinin bir
parçasıdır.
