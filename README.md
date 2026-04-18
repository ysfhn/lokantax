# Lokantax

Tek dosyalık statik landing page. React + Babel CDN üzerinden tarayıcıda çalışır, **build adımı yoktur**.

## Yapı

```
index.html      ← tüm sayfa ve React bileşenleri
styles.css      ← stiller
assets/         ← görseller (uygulama ekranları, logo)
```

## Yerelde önizleme

Tarayıcı ES module / fetch güvenliği için basit bir HTTP sunucu yeterli:

```bash
python3 -m http.server 8080
# veya
npx serve .
```

Sonra `http://localhost:8080` adresini aç.

## Cloudflare Pages'e dağıtım

Build adımı gerekmiyor:

1. Cloudflare Pages → **Create a project** → **Direct upload**
2. Proje klasörünü (`index.html`, `styles.css`, `assets/`) sürükle-bırak
3. Yayınla

İsteğe bağlı olarak GitHub'a bağlanırsan **build command** boş, **output directory** `/` olmalıdır.
