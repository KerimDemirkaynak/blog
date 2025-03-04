---
author: ["Kerim Demirkaynak"]
title: "Hugo ile Disqus Yorum Sistemi Entegrasyonu"
date: "2025-03-03"
description: "Bu rehber, Hugo kullananlar için Disqus yorum sistemini nasıl entegre edeceklerini adım adım anlatır."
tags: ["hugo", "blog", "disqus", "papermod", "website"]
ShowToc: true
comments: true
cover:
    image: "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRgSUTlu7jZrxOv2tgWvCuUuOe5eB0MKmrtcsshfGM9-Ln7OXc6xjBL3x-X&s=10" # image path/url
---

## 1. Disqus Hesabı Oluşturma
Öncelikle [Disqus](https://disqus.com/) üzerinde bir hesap açmalısınız.

1. [Disqus'a kaydolun](https://disqus.com/)
2. **"I want to install Disqus on my site"** seçeneğini seçin.
3. **Website Name** kısmına blog adınızı yazın.
4. **Choose Your Unique Disqus URL** kısmında **shortname** belirleyin (Örnek: `ornekblog`).
5. **Basic Plan** seçeneğini seçin (Ücretsiz).
6. **Platform olarak "Universal Code" seçin.**
7. **Disqus kısa adınızı (shortname) not alın.** Örn: `ornekblog.disqus.com`

---

## 2. Hugo'da Disqus'u Etkinleştirme
Hugo projenizin ana dizininde yer alan **config.yml** veya **config.toml** dosyasını açın.

### **📝 `config.yml` için:**
```yaml
disqus:
  enable: true
  shortname: "ornekblog"
params:
  comments: true
```
📝 config.toml için:
```
disqusShortname = "ornekblog"

[params]
  comments = true
```
NOT: ornekblog yerine kendi Disqus kısa adınızı (shortname) yazmalısınız.

---

## 3. comments.html Dosyasını Düzenleme

Hugo temanızın yorum sistemini desteklediğinden emin olun.

1. layouts/partials/comments.html dosyasını oluşturun (Eğer yoksa).


2. İçine şu kodu ekleyin:

```
<div class="disqus markdown">
    {{ partial "disqus.html" . }}
</div>
```
Bu kod, Disqus yorum sistemini yüklemek için ayrı bir disqus.html dosyasını çağıracaktır.

---

## 4. disqus.html Dosyasını Oluşturma

Şimdi layouts/partials/ dizininde disqus.html dosyasını oluşturun ve aşağıdaki kodları ekleyin:
```
<div id="disqus_thread"></div>
<script>
    var disqus_config = function () {
        this.page.url = window.location.href;
        this.page.identifier = window.location.pathname;
    };
    (function() {
        var d = document, s = d.createElement('script');
        s.src = 'https://ornekblog.disqus.com/embed.js';
        s.setAttribute('data-timestamp', +new Date());
        (d.head || d.body).appendChild(s);
    })();
</script>
<noscript>Lütfen JavaScript’i etkinleştirerek <a href="https://disqus.com/?ref_noscript">Disqus yorumlarını</a> görün.</noscript>
```
Önemli:

ornekblog.disqus.com kısmını kendi Disqus shortname’inizle değiştirin.

---

## 5. İçerik Dosyalarında Yorumları Etkinleştirme

Yorumları belirli sayfalarda göstermek için content/posts/ altındaki .md dosyalarına şu satırı ekleyin:
```
comments: true
```
Örnek içerik dosyası (content/posts/ornek-yazi.md):
```
---
title: "Hugo'da Disqus Yorumları"
date: 2025-03-03
comments: true
---
```

---

## 6. Değişiklikleri Test Etme ve Yayınlama

Yerel Sunucuda Test Etme

Terminalde aşağıdaki komutu çalıştırın:
```
hugo serve --disableFastRender
```
Tarayıcıda http://localhost:1313/ adresine gidin.

Yorum kutusunun görünüp görünmediğini kontrol edin.


Canlıya Alma (Deploy)

Eğer yorumlar lokalde (localhost) çalışmıyorsa, Disqus bazı güvenlik nedenleriyle yorumları gizleyebilir.
Yorumları görmek için sitenizi canlıya alın:
```
hugo --gc --minify
```
Siteyi GitHub Pages, Netlify, Vercel veya kendi sunucunuza yükleyin.

Gerçek domain üzerinden yorumları test edin.

---

## 7. Olası Sorunlar ve Çözümleri

| **Sorun** | **Çözüm** |
|-----------|----------|
| **Disqus yorumları görünmüyor.** | `config.yml` veya `config.toml` içinde **shortname** doğru mu kontrol edin. |
| **Disqus yüklenirken hata veriyor.** | Tarayıcı konsolunu (`F12 > Console`) açıp hata mesajlarını kontrol edin. |
| **Disqus localhost'ta çalışmıyor.** | Siteyi canlıya alın ve tekrar deneyin. |
| **Disqus çerçevesi (iframe) yüklenmiyor.** | Adblocker veya tarayıcı eklentilerini kapatıp tekrar deneyin. |

---

## 8. Sonuç ve Özet 📝

✅ Disqus hesabı oluşturduk.
✅ config.yml veya config.toml içinde Disqus'u etkinleştirdik.
✅ comments.html ve disqus.html dosyalarını oluşturduk.
✅ Hugo'yu çalıştırarak yorumları test ettik.
✅ Eğer çalışmıyorsa, hataları kontrol edip düzelttik.

Artık Hugo blogunuzda Disqus yorum sistemi aktif! 🚀
Sorularınız varsa Disqus Destek Sayfası: https://help.disqus.com/

---
