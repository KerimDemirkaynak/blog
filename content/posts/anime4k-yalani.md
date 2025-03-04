---
author: ["Ryan Lucia", "Kerim Demirkaynak"]
title: "4K Anime Yalanı"
date: "2019-08-24"
description: "4K Anime video filtresi hakkında gerçekler."
tags: ["anime", "4k anime", "anime4k", "video filtresi"]
ShowToc: true
comments: true
cover:
    image: "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQxtvD-OHI0QeB1YC6zeubf8tfo1786D4OPNF8OR2Si5x3ZQ8suRxIntBU&s=10" # image path/url
---
 
Her yıl birkaç kez, Reddit’te “Yeni Nesil Üstün Görüntü Yükseltme Algoritması” başlıklı gönderiler görmeye alışkınım. Normalde bu tür şeyleri görmezden gelirim, ancak bu sefer birkaç neden beni detaylı bir inceleme yapmaya itti:  

1. Pek çok kişi bana Anime4K deposunu göndererek fikrimi sordu. Bu yazıyı yazmak, kendimi tekrar etmekten kurtaracak.  
2. Depo, Reddit ve diğer sosyal medya platformlarında oldukça olumlu geri dönüşler aldı. Ancak, ciddi eksikliklerini ele alan iyi bir eleştiriyle karşılaşmadım.  
3. Anime4K’nın yaratıcısı, algoritmanın yetenekleri hakkında büyük iddialarda bulundu, ancak bu iddialar pek de geçerli görünmüyor. Ayrıca, bunları okurken kötü bir ruh halindeydim.  
4. Bu makalede bahsedeceğim sorunlar oldukça yaygın ve gelecekte benzer iddialarla gelen başka projeleri değerlendirirken yardımcı olabilir.  

## Anime4K Gerçekten Bir Üstün Görüntü Yükseltme Algoritması mı?

Makale, **“üst düzey”, “yüksek kaliteli”** bir görüntü yükseltme algoritmasından bahsederek başlıyor. Ancak, bu tür iddiaların adil bir karşılaştırma ile desteklenmesi gerekir. Ne yazık ki, burada böyle bir şey göremiyoruz. Daha büyük bir sorun da şu:  

### **Anime4K, Bir Görüntü Yükseltme Algoritması Değildir.**  

Eğer [makaleye](https://github.com/bloc97/Anime4K/blob/f7e6b38b0db82de1ab3df83204dd656e9adbc022/Preprint.md) göz atarsanız, Anime4K’nın aslında videonun çözünürlüğünü değiştirmediğini fark edersiniz. Bu bir **keskinleştirme filtresidir**. Yani, sadece çizgileri keskinleştirir ve bu kadar.  

Bir keskinleştirme filtresi yapmakta elbette bir sorun yok, ancak bunu doğru şekilde adlandırmak gerekir.  

### **Yanıltıcı İddialar ve Karşılaştırmalar**  

Anime4K’nın makalesini okuduğunuzda, yazarın bazı iddialarının gerçeği yansıtmadığını fark edebilirsiniz. Örneğin:  

- **Anime4K, gerçekte yalnızca bir keskinleştirme filtresi olduğu halde üstün bir yükseltme algoritması gibi sunuluyor.**  
- **Diğer keskinleştirme filtreleri ile herhangi bir karşılaştırma yapılmamış.** Oysa, bu tür teknikler uzun zamandır var ve zaten benzer çıktılar üreten birçok filtre mevcut.  
- **Filtre aslında Jinc algoritması ile birlikte kullanılmış.** Anime4K tek başına çözünürlüğü artırmadığı için, yazar Jinc ile görüntüyü büyütüp ardından Anime4K’yı uygulamış. Ancak, bunu başlangıçta açıkça belirtmemiş.  

Bu da demek oluyor ki, makalede gösterilen “üstün kalite” örnekleri aslında **Jinc + Anime4K** kombinasyonunun sonucu. Fakat yazar, Jinc’i başta hiç belirtmeyerek sonuçları Anime4K’ya mal etmiş.  

### **Karşılaştırmalar ve Görsel Örnekler**  

Aşağıda, yazarın sunduğu iki karşılaştırmayı görebilirsiniz. Eğer fark göremiyorsanız, bir göz doktoruna görünmeyi düşünebilirsiniz. :-)  

#### **Örnek 1: Anime4K’nın Keskinleştirme Etkisi**  

![Anime4K Karşılaştırma 1](https://redvice.org/assets/images/anime4k-comparison1.png)  

Anime4K’nın çizgileri keskinleştirdiğini görebiliyoruz. Ancak, bu işlem aynı zamanda **aliasing (kenar tırtıklanması)** sorununa da yol açıyor. Ayrıca, çizgiler gözle görülür şekilde incelmiş ve bozulmuş.  

#### **Örnek 2: Banding ve Keskinleştirme Sorunları**  

![Anime4K Karşılaştırma 2](https://redvice.org/assets/images/anime4k-comparison2.png)  

Burada, pencere çerçevesindeki banding (renk geçişlerinde basamaklı görünüm) efektinin keskinleştirme işlemiyle daha da belirginleştiğini görebilirsiniz.  

Bu örneklerde de görüldüğü gibi, Anime4K **çizgileri keskinleştirmek için detay kaybına sebep oluyor.**  

### **Rastgele Seçilen Örnekler mi?**  

Yazar, karşılaştırmalardaki kareleri **rastgele seçtiğini** iddia ediyor. Ancak, bu pek olası görünmüyor.  

- Gerçekten rastgele kareler seçilseydi, her filtre için farklı avantaj ve dezavantajların görülebileceği daha çeşitli sonuçlar olurdu.  
- İnsanlar, genellikle daha keskin görüntüleri daha kaliteli olarak değerlendirir. Yani, çift kör testlerin sonuçları, sübjektif algılara dayandığı için yanıltıcı olabilir.  

![Grafik 1](https://redvice.org/assets/images/anime4k-graph.png)  

Ayrıca, yazar **niceliksel ölçümleri (PSNR, SSIM, VMAF, vb.) geçersiz sayıyor** ve sadece 4K’ya odaklanıyor. Ancak, bu ölçümler **farklı filtrelerin performansını adil bir şekilde değerlendirmek için önemli** ve bunları tamamen göz ardı etmek doğru değil.  

## **Sonuç: Pazarlama vs. Gerçeklik**  

Özetle, **Anime4K aslında bir görüntü yükseltme algoritması değil, sadece bir keskinleştirme filtresi.**  

Eğer keskinleştirilmiş görüntüler hoşunuza gidiyorsa, zaten **NGU gibi daha iyi ve gerçek zamanlı çalışan filtreler var.** Anime4K’nın en büyük sorunu, **keskinleştirme işleminin detay kaybı, aliasing ve bozulmalara sebep olması.**  

Bu tür “devrimsel” video filtrelerine her zaman şüpheyle yaklaşmakta fayda var. Çoğu zaman **pazarlama abartısı, teknik gerçeklerden çok daha ağır basıyor.**  

---

### **Dipnot**  

> Görüntü keskinliği konusunda sübjektif değerlendirmeler yapmak her zaman zordur. Ses mühendisliğinde, yüksek ses seviyeleri genellikle daha kaliteli olarak algılanır. Aynı durum video için de geçerlidir; insanlar daha keskin görüntüleri genellikle daha iyi olarak değerlendirir.
