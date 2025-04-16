---
author: ["Kerim Demirkaynak"]
title: "GitHub Pages ile Bluesky'da Doğrulanmış Bir Kullanıcı Adı Alma Rehberi"
date: "2024-12-01"
description: "Bluesky'da kendi alan adınızı doğrulanmış bir kullanıcı adı olarak nasıl kullanabileceğinizi ve GitHub Pages üzerinden bunu nasıl gerçekleştirebileceğinizi adım adım anlatıyoruz."
tags: ["bluesky", "github", "doğrulama", "handle", "kişisel web"]
ShowToc: true
comments: true
cover:
  image: "https://miro.medium.com/v2/resize:fit:750/format:webp/1*NYD599YEezEXI-RF5Dh9hw.png"
---

## 1. Neden GitHub Kullanmalıyız?

Twitter (X) hızla kötüleşen bir platforma dönüşürken birçok kişi gibi ben de [Bluesky](https://bsky.app)'a geçiş yaptım. Burada doğrulanmak için ödeme yapmanıza gerek yok. Kendi alan adınızı veya web sayfanızı kullanarak doğrulanabiliyorsunuz.  

Ancak özel bir alan adınız yoksa ne olacak? Cevap basit: GitHub Pages! Ücretsiz, kolay ve size özel bir doğrulama yöntemi sunuyor.

---

## 2. GitHub Pages Sayfanızı Oluşturun

İlk adım olarak GitHub hesabınızda bir depo (repository) oluşturun. Şu yapıyı izlemelisiniz:

https://github.com/KULLANICI_ADINIZ/KULLANICI_ADINIZ.github.io

Bu sayfada bir README.md dosyası ile kendinizi tanıtabilirsiniz. Daha profesyonel görünmek isterseniz basit bir HTML sayfası da hazırlayabilirsiniz.

### Sayfayı Aktif Etme

- Depo ayarlarına (`Settings`) gidin.
- Sol menüde “Pages” sekmesini seçin.
- Kaynaktan (`Source`) `main` dalını seçin.
- Sayfanız artık şu adreste yayında olacak:

https://KULLANICI_ADINIZ.github.io/

---

## 3. Bluesky Ayarlarını Yapın

Bluesky hesabınıza gidin:  
🔗 [https://bsky.app/settings](https://bsky.app/settings)

- “Hesap” sekmesine geçin.
- “Kullanıcı adı” kısmına tıklayın.
- “Kendi alan adım var” → **“DNS Paneli Yok”** seçeneğini seçin.
- Açılan kutuya `KULLANICI_ADINIZ.github.io` yazın.

Bluesky size doğrulama için gerekli bir metin verecek. Bu metni alıp aşağıdaki adımları izleyin.

---

## 4. `.well-known` Dosyasını Oluşturun

GitHub reposunda `.well-known` adlı bir klasör oluşturun ve içine **`atproto-did`** adında bir dosya ekleyin. Dosyanın içeriği yalnızca Bluesky'ın size verdiği doğrulama metni olmalıdır.

### Yol şöyle olacak:

https://KULLANICI_ADINIZ.github.io/.well-known/atproto-did

Ancak dikkat! `.well-known` klasörü GitHub Pages'te varsayılan olarak görünmez. Görünür yapmak için repo kök dizinine bir `_config.yml` dosyası ekleyin ve içine şu satırı yazın:

```yaml
include: [".well-known"]
```

---

5. Bluesky Üzerinde Onayla

GitHub sayfanızdaki dosya yayınlandıktan sonra Bluesky’a dönün ve işlemi onaylayın. Artık doğrulanmış bir kullanıcı adı olarak KULLANICI_ADINIZ.github.io kullanabilirsiniz.


---

Örnek:

Benim sayfam:
🔗 https://kerimdemirkaynak.github.io/


---

Sonuç

Kendi alan adınız olmasa bile GitHub sayesinde profesyonel bir şekilde Bluesky'da doğrulanmış olabilirsiniz. Ayrıca bu işlem tamamen ücretsiz!

Bluesky’ın açık ve merkeziyetsiz yapısı bu tür çözümleri mümkün kılıyor. GitHub bilginiz varsa, bu fırsatı mutlaka değerlendirin!
