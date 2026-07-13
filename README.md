# Atölye Kuzey — Özgün Jekyll Portfolyo Teması

Sıfırdan tasarlanmış, Türkçe içerikli bir Jekyll portfolyo teması. Anasayfada hero, seçili projeler ızgarası ve günlük (blog) şeridi; ayrıca proje arşivi, günlük, hakkında ve iletişim sayfaları bulunur.

## Kurulum

Ruby (3.x) ve Bundler kuruluysa:

```bash
bundle install
bundle exec jekyll serve
```

Site `http://localhost:4000` adresinde açılır.

## İçerik ekleme

**Yeni proje:** `_projects/` klasörüne bir `.md` dosyası ekleyin:

```yaml
---
title: Proje Adı
order: 5              # arşivdeki sırası
category: Konut
client: İşveren adı
year: 2026
location: Şehir
area: 1.000 m²
thumbnail: /assets/images/gorsel.jpg
---
Proje anlatımı buraya (Markdown).
```

**Yeni yazı:** `_posts/` klasörüne `YYYY-AA-GG-baslik.md` biçiminde dosya ekleyin. İlk paragraf otomatik olarak özet kabul edilir.

**Görseller:** `assets/images/` içindeki SVG'ler yer tutucudur; kendi fotoğraflarınızla değiştirip proje dosyalarındaki `thumbnail` yolunu güncelleyin.

## Kimliği özelleştirme

- Renkler ve yazı tipleri: `_sass/_base.scss` içindeki `:root` değişkenleri
- Site adı, açıklama, sosyal bağlantılar: `_config.yml`
- Menü: `_includes/header.html`
- Footer kolonları ve bülten metni: `_includes/footer.html`

## Yapı

```
_layouts/    default, home, page, project, post
_includes/   head, header, footer
_sass/       _base (tokenlar), _components (bileşenler)
_projects/   proje koleksiyonu
_posts/      günlük yazıları
assets/      css, js, images
```

## Notlar

- İletişim ve bülten formları statiktir; Formspree, Netlify Forms vb. bir servise `action` vererek çalışır hâle getirebilirsiniz.
- Tema; klavye odak halkaları, atlama bağlantısı ve `prefers-reduced-motion` desteğiyle erişilebilirlik göz önünde bulundurularak yazılmıştır.
