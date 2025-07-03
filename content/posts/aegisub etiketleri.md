---
author: ["Kerim Demirkaynak"]
title: "Aegisub Etiketleri"
date: "2025-07-03"
description: "Aşağıda göreceğimiz etiket listesi Aegisub programına özgü değildir, ancak ASS (Advanced Substation Alpha) altyazı formatı tarafından desteklenmektedir."
tags: ["aegisub", "aegisub etiketleri", "altyazı düzenleme", "advanced substation alpha"]
ShowToc: true
comments: true
cover:
    image: "https://konachan.net/sample/ba5e9f2ca3d37255f07913a552442bc8/Konachan.com%20-%20145179%20sample.jpg" # image path/url
---
 
# Genel Yapı

Bir **ASS** dosyasında etiketler, diyalog satırı içinde, `Text` alanında bulunur ve küme parantezleri (`{}`) içine alınır.

```txt
Format: Layer, Start, End, Style, Name, MarginL, MarginR, MarginV, Effect, Text
Dialogue: 0,0:00:01.00,0:00:05.00,Default,,0,0,0,,{tags}Metin burada
```

Aegisub arayüzünde şöyle bir şey görürüz:

![image.png](https://media.fansubhub.com/d/uploads/images/aegisub/tags/tags-ejemplo-1.png?sign=daNElU2jPS-aTXFw66_nqC3adCvXNyYvSK0KYEQI3xU=:0)

# Temel Etiketler

## Kalın

`\bN` - Metne kalınlık uygulamak için.

`N`, kalın formatlamayı 'açık' veya 'kapalı' olarak ayarlamak için `1` ve `0` arasında değiştirilebilir.

| Biçim | Çıktı |
| :--- | :--- |
| `{\b1}Bu metin kalın{\b0} ve bu değil.` | **Bu metin kalın** ve bu değil. |

Bu düğme ile kullanılır:  
![bold.png](https://media.fansubhub.com/d/uploads/images/aegisub/tags/negrita.png?sign=qjwOxyoxCqr53x_ynD00ZxJU0qAg0Rh4gs06gYZL6SE=:0)

## İtalik

`\iN` - Metni italik yapmak için.

*   `N`, italik formatlamayı açmak veya kapatmak için `1` ve `0` arasında değiştirilebilir.

| Biçim | Çıktı |
| :--- | :--- |
| `{\i1}Burası italik{\i0} ve artık değil.` | *Burası italik* ve artık değil. |

Bu düğme ile kullanılır:  
![cursiva.png](https://media.fansubhub.com/d/uploads/images/aegisub/tags/cursiva.png?sign=6-WMJwVw37Z7yoW0J1OB7bKHhOOLaiYxKOxHr25LukI=:0)

## Altı Çizili

`\uN` - Metnin altını çizmek için.

*   `N`, alt çizgiyi uygulamak veya uygulamamak için `1` ve `0` arasında değiştirilebilir.

| Biçim | Çıktı |
| :--- | :--- |
| `Bir metni bu şekilde {\u1}vurgulayabilirsiniz{\u0}.` | Bir metni bu şekilde <span style="text-decoration: underline;">vurgulayabilirsiniz</span>. |

Bu düğme ile kullanılır:  
![subrayado.png](https://media.fansubhub.com/d/uploads/images/aegisub/tags/subrayado.png?sign=H-u8ZX9DlNEIGa8YRVa2q6RMnoc5d2ego5CMsoLJRJg=:0)

## Üstü Çizili

`\sN` - Bu etiket, metnin üzerini çizmek için kullanılır.

*   `N`, üst çizgiyi uygulamak veya uygulamamak için `1` ve `0` arasında değiştirilebilir.

| Biçim | Çıktı |
| :--- | :--- |
| `{\s1}Bunu görmezsiniz{\s0} ama bunu görürsünüz.` | <s>Bunu görmezsiniz</s> ama bunu görürsünüz. |

Bu düğme ile kullanılır:  
![tachar.png](https://media.fansubhub.com/d/uploads/images/aegisub/tags/tachar.png?sign=SDo9Y66RH4WEU4GFzqa_hknnGmdLFscOhuxpE2M0-zY=:0)

## Yazı Tipi Boyutu

`\fsN` - Metnin yazı tipi boyutunu belirtir.

`N`, piksel cinsinden metin boyutudur.

Metin boyutunu metin stilinin varsayılan boyutuna sıfırlamak için, bir değer girmeme (`{\fs}` gibi) veya `N`'yi `0` olarak bırakma seçeneğiniz vardır.

| Biçim | Çıktı |
| :--- | :--- |
| `Burada metnin nasıl {\fs24}büyüdüğünü{\fs} görebiliriz.` | Burada metnin nasıl <span style="font-size: 24px;">büyüdüğünü</span> görebiliriz. |

Bu düğme ile kullanılır:  
![font.png](https://media.fansubhub.com/d/uploads/images/aegisub/tags/font.png?sign=qZzme8v6UFw02evlVQaXuMVp3gnW5__0lpyn1s-KZM0=:0)

## Yazı Tipi

`\fnYazıTipiAdı` - Metnin yazı tipini değiştirir.

Yazı tipini metin stilinin varsayılanına sıfırlamak için, bir değer **girmeme** (`{\fn}` gibi) veya bir yazı tipi belirtme (`\fnArial` gibi) seçeneğiniz vardır.

| Biçim | Çıktı |
| :--- | :--- |
| `Normal yazı tipinden farklı bir {\fnGrill Sans}yazı tipi.` | Normal yazı tipinden farklı bir <span style="font-family: Grill Sans, serif;">yazı tipi</span>. |

Bu düğme ile kullanılır:  
![font.png](https://media.fansubhub.com/d/uploads/images/aegisub/tags/font.png?sign=qZzme8v6UFw02evlVQaXuMVp3gnW5__0lpyn1s-KZM0=:0)

## Kenarlık

`\bordN` - Nesne için kenarlık seviyesini ayarlar.

*   `N`, `0` ile `∞` arasında bir sayı olabilir.

| Biçim | Çıktı |
| :--- | :--- |
| `{\bord2}Örnek.` | ![borde1.png](https://media.fansubhub.com/d/uploads/images/aegisub/tags/borde1.png?sign=ZRczQeGKuSg8a_iTtCjOxXQHGjLBPLs6-sS02Rsvldo=:0) |
| `{\bord8}Örnek.` | ![borde2.png](https://media.fansubhub.com/d/uploads/images/aegisub/tags/borde2.png?sign=j65cpUtlK4mRlBbFfqHH2Ndfa40O2yxkM4tL78W2Um8=:0) |

Bu etiket, `\xbordN` ve `\ybordN` olmak üzere iki varyantla eksenler tarafından kontrol edilebilir.  
Bu varyantların her biri, nesnenin kenarlık seviyesini ilgili eksende kontrol edecektir.

## Gölge

`\shadN` - Nesnenin sahip olacağı gölge kaydırma seviyesini ayarlar. Kenarlığın aksine, gölge büyümez, ancak yatay ve dikey olarak kayar.

*   `N`, `0` ile `∞` arasında bir sayı olabilir.

| Biçim | Çıktı |
| :--- | :--- |
| `{\shad2}Örnek.` | ![shad1.png](https://media.fansubhub.com/d/uploads/images/aegisub/tags/shad1.png?sign=_bxowY2cTuxc-cd_I9uxjll8TJsFhF-rGtErfA4QLTU=:0) |
| `{\shad8}Örnek.` | ![shad2.png](https://media.fansubhub.com/d/uploads/images/aegisub/tags/shad2.png?sign=MUU30ENbKH6YX96Tcf_Y0my_e6W8D_YGUBEA8ozl05k=:0) |

Bu etiket, eksenler tarafından kontrol edilebilir ve iki varyantı vardır: `\xshadN` ve `\yshadN`.  
Bu varyantların her biri, nesnenin gölge seviyesini ilgili eksende kontrol edecektir.

## Renk ve Alfa

`\c&H000000&` - Bununla nesnenin rengini değiştirebiliriz. Rengi varsayılana sıfırlamak için değeri `\c` olarak bırakabiliriz. Renk **HEX** formatında kodlanmıştır; ancak, **RGB** (_Kırmızı, Yeşil, Mavi_) değil, **BGR** (_Mavi, Yeşil, Kırmızı_)'dir. Renkleri manuel olarak uygularken bu dikkate alınmalıdır.

Rengi [Aegisub](/en/Aegisub) arayüzünden uygularsak, **HEX** kodumuzu otomatik olarak **RGB**'den **BGR**'ye dönüştürecektir.

| Biçim | Çıktı |
| :--- | :--- |
| `{\c&H0000FF&}Kanlı{\c} bir metin oluşturmak için, ya da ona benzer bir şey.` | <span style="color: red;">Kanlı</span> bir metin oluşturmak için, ya da ona benzer bir şey. |

<br>

### Bu renk etiketinin dört varyantı vardır: `\1c`, `\2c`, `\3c`, `\4c`.

*   `\1c` harfin içi, yani ana renk için kullanılır.
*   `\2c` bir karaoke satırında henüz söylenmemiş heceleri doldurmak için kullanılır.
*   `\3c` harfin kenarlığı içindir.
*   `\4c` harfin gölgesi için kullanılır.

![colores.png](https://media.fansubhub.com/d/uploads/images/aegisub/tags/colores.png?sign=Weaf_Fwos21G1Fb7Wv6t1nzb0FdwUWCUQixgirAvvyc=:0)

Benzer şekilde, metnin bir bölümünün görünürlüğünü belirlemek için dört alfa varyantı vardır: `\1a` ana alfa için, `\2a` karaoke'de henüz söylenmemiş hecelerin renginin alfası için, `\3a` kenarlık alfası için ve `\4a` gölge alfası için.

Farklı alfalar manuel olarak veya Aegisub arayüzündeki renk seçiciden ayarlanabilir ve basılan düğmeye bağlı olarak nesnenin belirli bir bölümüne uygulanacaktır.

![alpha.png](https://media.fansubhub.com/d/uploads/images/aegisub/tags/alpha.png?sign=16N80foyM7YA9I1BvUbtscC1We-U_5k8V8NUpgwvMIc=:0)

## Bulanıklaştırma

`\blurN` - Nesnenin bulanıklaştırma derecesini ayarlar.

*   `N`, `0` ile `100` arasında bir sayı olabilir.

Nesnenin ana gövdesine ve varsa gölgesine etki eder. Nesnenin bir kenarlığı varsa, o zaman ana gövdeye değil kenarlığa etki eder. Her iki durumda da, `\blur` **her zaman** gölgeye etki edecektir.

| Biçim | Çıktı |
| :--- | :--- |
| `{\shad2\blur2}Örnek.` | ![blur1.png](https://media.fansubhub.com/d/uploads/images/aegisub/tags/blur1.png?sign=hA4VVHFa5AQIGY6EhBEFKTqp8JGbQByD5skF8vuIAg0=:0) |
| `{\shad2\bord2\blur2}Örnek.` | ![blur2.png](https://media.fansubhub.com/d/uploads/images/aegisub/tags/blur2.png?sign=HAGqF-PTw4yd-Pp7tTbAAha9MlSTksHY3VlfTv9ujCU=:0) |
| `{\blur2}Örnek.` | ![blur3.png](https://media.fansubhub.com/d/uploads/images/aegisub/tags/blur3.png?sign=79ZpDBhn67a1eZf9yOjvKmvpT_5qrf20V-0KdgJkye4=:0) |

## Asimetrik Bulanıklaştırma

`\beN` - `blur`'a benzer asimetrik bir bulanıklaştırma ayarlar, ancak farklı bir dağılma ivmesine sahiptir, bu da alan derinliği bulanıklıkları oluştururken kullanışlıdır.

*   `N`, `0` ile `100` arasında bir sayı olabilir.

Nesnenin ana gövdesine ve varsa gölgesine etki eder. Nesnenin bir kenarlığı varsa, o zaman ana gövdeye değil kenarlığa etki eder. Her iki durumda da, `\be` **her zaman** gölgeye etki edecektir.

| Biçim | Çıktı |
| :--- | :--- |
| `{\shad2\be2}Örnek.` | ![blur1.png](https://media.fansubhub.com/d/uploads/images/aegisub/tags/blur1.png?sign=hA4VVHFa5AQIGY6EhBEFKTqp8JGbQByD5skF8vuIAg0=:0) |
| `{\shad2\bord2\be2}Örnek.` | ![blur2.png](https://media.fansubhub.com/d/uploads/images/aegisub/tags/blur2.png?sign=HAGqF-PTw4yd-Pp7tTbAAha9MlSTksHY3VlfTv9ujCU=:0) |
| `{\be2}Örnek.` | ![blur3.png](https://media.fansubhub.com/d/uploads/images/aegisub/tags/blur3.png?sign=79ZpDBhn67a1eZf9yOjvKmvpT_5qrf20V-0KdgJkye4=:0) |

## Yavaşça Belirme (Fade)

`\fad(T1,T2)` - Yavaşça belirme ve kaybolmayı belirtir.

*   `T1`, satırın başlangıcından itibaren, tamamen görünmezden tamamen görünür hale gelmesi için milisaniye cinsinden geçen süredir.
*   `T2`, satırın sonundan itibaren, tamamen görünürden tamamen görünmez hale gelmesi için milisaniye cinsinden geçen süredir.

Örneğin, `\fad(500,300)` komutunda, satır belirmek için ilk `500` milisaniyeyi, kaybolmak için ise son `300` milisaniyeyi kullanır. Değer `0` ise, satırın o bölümü için hiçbir şey yapılmaz. Değerlerin girilmesi zorunludur.

| Biçim | Çıktı |
| :--- | :--- |
| `{\fad(1500,1500)}Örnek.` | ![gif_fad.gif](https://media.fansubhub.com/d/uploads/images/aegisub/tags/gif_fad.gif?sign=dotPSGQxVN4yI_PUitQeErCt4XWZe-m6ASrqCFAwhV8=:0) |

## Konumlandırma

`\pos(px,py)` - `X` ve `Y` eksenlerindeki konumlandırmayı belirtir.

*   `px` yatay konumu, `py` ise dikey konumu belirler.

Örneğin, `\pos(350,140)` nesnenin ekranın sol kenarından 350 piksel ve üst kenarından 140 piksel uzağa konumlandırılacağı anlamına gelir.

| Biçim | Çıktı |
| :--- | :--- |
| `{\pos(350,140)}Örnek.` | ![pos.png](https://media.fansubhub.com/d/uploads/images/aegisub/tags/pos.png?sign=8Urai8-dfzDhRbwYznaWJYEXxm0754txEef7sflzLAg=:0) |

## Hizalama

`\anN` - `\pos` belirtilmişse `\pos`'a göre, `\pos` yoksa tüm ekrana göre hizalamayı belirtir.

`N`, 1 ile 9 arasında bir sayı olabilir ve bu sayı, sayısal tuş takımı gibi hizalamayı belirler.

Olasılıklarınız şunlardır:

![an.png](https://media.fansubhub.com/d/uploads/images/aegisub/tags/an.png?sign=sSt0hipGK0hMuaHmGs8cM2x1Cr_XWdu5cLb_xpG1rQE=:0)

Eğer `\pos` belirlenmişse, o nokta referans olarak kullanılır.

| Biçim | Çıktı |
| :--- | :--- |
| `{\an5}Örnek.` | ![an5.png](https://media.fansubhub.com/d/uploads/images/aegisub/tags/an5.png?sign=hNvqGKV2_OzKEIlwZO4pcdibNWorm-aWhjzmOCZsnpM=:0) |
| `{\an4}Örnek.` | ![an4.png](https://media.fansubhub.com/d/uploads/images/aegisub/tags/an4.png?sign=WfzlzEGa9ToBcqufzIlJaB0kVf1t-1WhRzcSAtQxEas=:0) |

Hizalamanın aynı zamanda paragrafların nasıl düzenlendiğini ve metnin yazıldıkça nasıl büyüdüğünü de belirlediğini belirtmekte fayda var.

## Kenar Boşluklarını Yoksay

`\q2` - Satırın ekranın yatay kenar boşluklarını yok saymasını sağlar, böylece video dışındaki tüm boş alan kullanılabilir.

Başka ayarı yoktur.

| Biçim | Çıktı |
| :--- | :--- |
| `{\an4\fs600}q2 olmadan örnek` | ![sinq2.png](https://media.fansubhub.com/d/uploads/images/aegisub/tags/sinq2.png?sign=9nr3QjW4JpfCZjuDiI90fH63JTBAXn5MMt8wqb_pMag=:0) |
| `{\an4\fs600\q2}q2 ile örnek` | ![conq2.png](https://media.fansubhub.com/d/uploads/images/aegisub/tags/conq2.png?sign=loHFnoJIwdABKy0uus51FSpEOTAaYwxrqVaFEWxeu_s=:0) |

Gördüğümüz gibi, `\q2` etiketi bulunduğunda, metin birikmeden video dışına devam eder.

## Ölçek

`\pN` - Vektör çiziminin ölçeğini bildirir. Bu çoğunlukla şekiller için kullanılır.

*   `N`, `0` ile `∞` arasında bir sayı olabilir ve `{}`'den sonra girilen şeklin ölçeğini belirler.

| Biçim | Çıktı |
| :--- | :--- |
| `{\p1}m 796 428 l 992 428 992 632 796 632` | ![p1.png](https://media.fansubhub.com/d/uploads/images/aegisub/tags/p1.png?sign=BOzRIF5DSwD-Ae9QZqSXxA-srkUBLF1w5Zq5GqUh7Fk=:0) |
| `{\p2}m 796 428 l 992 428 992 632 796 632` | ![p2.png](https://media.fansubhub.com/d/uploads/images/aegisub/tags/p2.png?sign=namUzaHJFqCgJuRDYP88a0GQqyUreb7U2mSGaMU79yA=:0) |

# Gelişmiş Etiketler

## Boyutlandırma

`\fscxN`, `\fscyN` - Bir nesnenin genişlik (`X`) ve yükseklik (`Y`) cinsinden boyutlarını yüzde olarak belirler.

*   `N`, `0`'dan `∞`'a kadar bir sayı olabilir ve nesnenin gösteriminin `X` eksenindeki genişliğine ve `Y` eksenindeki yüksekliğine göre yüzde olarak boyutlandırılmasını temsil eder.

| Biçim | Çıktı |
| :--- | :--- |
| `{\fscx100\fscy100}Örnek.` | ![fsc100.png](https://media.fansubhub.com/d/uploads/images/aegisub/tags/fsc100.png?sign=zDdRrhT4TIcKv2Bz6H4iRiWcZyKBLffK_y3wNNJ2jK0=:0) |
| `{\fscx200\fscy200}Örnek.` | ![fsc200.png](https://media.fansubhub.com/d/uploads/images/aegisub/tags/fsc200.png?sign=uLZuqrc5NuDtuCaQUu29lvJxGzTksyrSjWz4qKc6KLU=:0) |

## Döndürme

`\frzN`, `\fryN`, `\frxN` - Bir nesnenin farklı eksenler (`X`, `Y`, `Z`) etrafındaki dönüşünü belirler.

*   `N`, `0` ile `360` arasında bir sayı olabilir ve dönüş derecesini belirler.  
    Sayı `360`'dan büyükse, nesne bir kez döner ve kalan dereceleri konumunu belirlemek için kullanır.

| Biçim | Çıktı |
| :--- | :--- |
| `{\frz45}Örnek` | ![frz.png](https://media.fansubhub.com/d/uploads/images/aegisub/tags/frz.png?sign=xq4jkLKIin8G5I3gWEVuD0UMLwq_CuNSUEzd-DScgao=:0) |
| `{\fry45}Örnek` | ![fry.png](https://media.fansubhub.com/d/uploads/images/aegisub/tags/fry.png?sign=1utyhfzu642ovvBvHEM-NGD5i5_t1mceFCcV1gFSkno=:0) |
| `{\frx45}Örnek` | ![frx.png](https://media.fansubhub.com/d/uploads/images/aegisub/tags/frx.png?sign=PC_n9FtmJ3wAK7b9bUM_QcTzQrOgYBr-zyjs68_bVzE=:0) |

Gördüğümüz gibi, üç tür `\fr` de metnimizin açısını her eksende manipüle etmemize olanak tanır, bu da her birine belirli bir dönüş ve aynı anda birkaçını uygulama yeteneği verir.

## Orijin (Merkez Noktası)

`\org(ox,oy)` - Tüm `\fr` etiketleri için dönüş merkezini belirtir. Belirtilmezse, ona bağlı olan etiketler, dönüş merkezlerini belirlemek için `\pos`'u veya ekran hizalamasına dayalı konumu kullanır.

*   `ox`, `X` koordinatıdır.
*   `oy`, `Y` koordinatıdır.

Orijini kullanırken dikkatli olmak gerekir, çünkü ekrandan çok uzakta bir orijin, nesnemizi görünür piksellerden çok uzağa gönderebilir ve manipüle edilmesini veya yeniden konumlandırılmasını imkansız hale getirebilir.

| Biçim | Çıktı |
| :--- | :--- |
| `{\org(200,500)\frz45}Örnek` | ![origen1.png](https://media.fansubhub.com/d/uploads/images/aegisub/tags/origen1.png?sign=mzyH5gyM7a6HWY9MaT4JFRXlPw2d7FMfgtv2M94CVZA=:0) |
| `{\org(200,500)\fry45}Örnek` | ![origen2.png](https://media.fansubhub.com/d/uploads/images/aegisub/tags/origen2.png?sign=4YdoNK1BGWS1n3COYCBSppXSA9xk-T1KUVokuAiXaGw=:0) |
| `{\org(200,500)\frx45}Örnek` | ![origen3.png](https://media.fansubhub.com/d/uploads/images/aegisub/tags/origen3.png?sign=vx15rRa43kk3UJw4dv6d39kLLYKzBTHbOP7SDjE2y98=:0) |

Orijini hareket ettirmek, tüm dönüş hesaplamasını değiştirir ve nasıl çalıştığını anlamak, istenen sonuca ulaşmak için çok önemlidir.

## Eğme (Skew)

`\faxN` ve `\fayN` - Nesnenin eğilme miktarını belirler.

*   `N`, `0`'dan `∞`'a kadar bir sayı olabilir ve nesnenin eğik düzlemde ne kadar "bozuk" görüneceğini belirler.

Çoğunlukla perspektifte kullanılır ve `Y` ekseninin `X` eksenine göre hücum açısını düzeltmemize olanak tanır, böylece zorunlu olarak 90 derece olmaz.

| Biçim | Çıktı |
| :--- | :--- |
| `{\fax-0.5}Örnek.` | ![fax.png](https://media.fansubhub.com/d/uploads/images/aegisub/tags/fax.png?sign=6aDjnQPV8iT2BISHlOS-hMa1S3JoyO1kAO2Qp-D48Q8=:0) |
| `{\fay-0.5}Örnek.` | ![fay.png](https://media.fansubhub.com/d/uploads/images/aegisub/tags/fay.png?sign=VHbs-1aCESbCEVT6X5NAXWeg0xR9UFJ1pZxvrsbS2qw=:0) |

## Taşıma (Translation)

`\move(x1,y1,x2,y2,t1,t2)` - Belirtilen bir başlangıç konumundan belirtilen bir hedef konumuna belirli bir sürede düz bir çizgide hareket ayarlar. Nesnenin sabit hızla ve ivme değiştirmeden bir ötelemesini gerçekleştirir.

*   `x1` ve `y1` başlangıç koordinatlarıdır.
*   `x2` ve `y2` hedef koordinatlarıdır.
*   `t1` ve `t2` geçerli satıra göre milisaniye cinsinden zamanlardır; `t1` başlangıç zamanı ve `t2` bitiş zamanıdır.

Eğer `t1` ve `t2` belirtilmezse, satırın tüm uzunluğu öteleme süresi olarak kabul edilir.

| Biçim | Çıktı |
| :--- | :--- |
| `{\move(419.35,174.22,1405.34,845.1,0,4963)}Örnek.` | ![move.gif](https://media.fansubhub.com/d/uploads/images/aegisub/tags/move.gif?sign=Hzrzav1AWWCFWKf3YQNPvPsFT5_Q4uFQbKRJ7SOdvqY=:0) |

## Dönüşüm (Transformation)

`\t(t1,t2,acc,etiketler)` - Belirtilen bir başlangıç zamanından ve belirtilen bir hedef zamana kadar, geçerli satıra göre, bir ivme değerine dayanarak, daha önce satırda beyan edilen değerlerden¹, stil değerlerinden² veya varsayılan değerlerden³, bu önem sırasına göre bir dönüşüm oluşturur.

Dönüşümün `t1` milisaniyesinden `t2` milisaniyesine gitmesini sağlar, ta ki sonunda beyan edilen `etiketler` beyan edilen değerle kalana kadar. Bu dönüşüm, `acc` değerine bağlı olarak başlangıçta daha hızlı ve sonda daha yavaş olabilir veya tam tersi olabilir. `acc` değeri 0 ile 1 arasında bir sayı veya hatta ondalık değerler olabilir.

| Biçim | Çıktı |
| :--- | :--- |
| `{\fscx150\fscy150\bord2\t(0,5000,1,\fscx20\bord15\fay-0.2)}Örnek.` | ![t1.gif](https://media.fansubhub.com/d/uploads/images/aegisub/tags/t1.gif?sign=Ldx_T8A_uJY5d08hdQMwpvT0-WVBbJ1kvKJNrIOqq4A=:0) |

> **Uyarı:**
> `\t( )` tüm etiketleri dönüştüremez. `\org( )`, `\pos( )`, `\move( )` ve `\clip( )`'i dönüştüremez (`\clip` sadece dikdörtgen ise dönüştürülebilir).

## Kontrollü Geçiş (Fade)

`\fade(alfa1,alfa2,alfa3,t1,t2,t3,t4)` - Belirtilen bir başlangıç zamanı ve alfadan bir geçiş ayarlar, ardından ara bir duruma ilerleme ve son bir zaman ve alfaya başka bir geçiş ayarlar.

`alfa1`'i başlangıç durumu olarak alarak, `t1`'e ulaşana kadar bu durumda kalır. O noktada, `t2`'ye ulaşana kadar `alfa2`'ye dönüşür. `t3`'e kadar bu durumda kalır, o noktada `t4`'e ulaşana kadar `alfa3`'e dönüşmeye başlar.

*   `alfa1`, `alfa2` ve `alfa3`, `0` ile `255` arasında sayılar olabilir; `0` tamamen görünür ve `255` tamamen görünmezdir.
*   `t1`, ilk ilerlemenin milisaniye cinsinden başlangıç zamanıdır ve satır zamanına dayanır.
*   `t2` aynı kuralları izler, ancak ilk ilerlemenin bitiş zamanını temsil eder.
*   `t3` diğer `t`'lerle aynıdır, ancak ikinci ilerlemenin başlangıcını, `t4` ise bitişini temsil eder.

| Biçim | Çıktı |
| :--- | :--- |
| `{\fade(0,255,0,1000,2500,3500,5000)\pos(926,666)}Örnek.` | ![fade.gif](https://media.fansubhub.com/d/uploads/images/aegisub/tags/fade.gif?sign=7dV3a7yqD3QpK3BQeTYtiBtw-yIuIaeuG_XtxXVkqkM=:0) |

## Vektörel Kırpma (Clipping)

`\clip(x1, y1, x2, y2)` ve `\iclip(x1, y1, x2, y2)` - Nesnemizin gösteriminin vektörel bir kırpmasını gerçekleştirir.

*   `\clip`, nesnemizi görmek için bir pencere oluşturur.
*   `\iclip`, nesnenin o bölümünü silen görünmez bir kutu oluşturur.

| Biçim | Çıktı |
| :--- | :--- |
| `{\clip(549.38,404.5,1027.17,694)}Örnek.` | ![clip.png](https://media.fansubhub.com/d/uploads/images/aegisub/tags/clip.png?sign=d83jfWMU6qVEGWTFVsL_oewidMGivkW9TpMgHfhKwgY=:0) |
| `{\iclip(549.38,404.5,1027.17,694)}Örnek.` | ![iclip.png](https://media.fansubhub.com/d/uploads/images/aegisub/tags/iclip.png?sign=rWjKZ6MLELPMEeX5gnA0AKynOMkAtciIrQsgtDyBshs=:0) |

Bu `\clip`'ler dikdörtgen tiptedir ve `\t( )` etiketi ile dönüştürülebilirler. Daha karmaşık `\clip`'ler dönüştürülemez ve yalnızca kare kare yazılarak canlandırılabilir.

*   `\clip` ve `\iclip` aynı satırda bir arada bulunamaz; satır başına yalnızca bir tür olabilir.
*   `\clip` ve `\iclip` birbirine eklenebilir; birinin koordinatlarını kopyalayıp diğerinden sonra, iki koordinat kümesi arasında bir boşluk bırakarak yapıştırmanız yeterlidir. Bir `\clip`'in koordinatları, bir `\iclip` için bekleyebileceğimiz etkiyi yaratmayacaktır.
*   `\clip` ve `\iclip`'in polaritesi vardır. Daha fazla görünür alan ekleyebilir veya bir `\clip` içinde `\iclip` olarak işlev görebilirler. Polarite, `\clip`'in çizim yönüne bağlıdır. Saat yönündeyse, kırpmaya eklenir. Saat yönünün tersineyse, seçimden çıkarılır.

> **Bilgi:**
> Eğer bu saat yönündeki `\clip`'i eklersem...
>
> | Biçim | Çıktı |
> | :--- | :--- |
> | <div style="max-width: 500px;">`{\clip(m 648.31 446.31 l 728.75 403.69 821.25 399.67 876.75 439.08 871.12 498.59 836.53 531.56 775.4 570.96 719.1 582.22 674.86 576.59 629.01 563.72 605.68 529.95 596.03 495.37 606.49 474.46 620.16 461.59)}Örnek.`</div> | ![clipej1.png](https://media.fansubhub.com/d/uploads/images/aegisub/tags/clipej1.png?sign=5I24mzNrYgiOg1Z_cffrEkQulnlaJOB1iH1zngPwObc=:0) |
>
> Aynı yönde yapılmış bu diğeriyle aşağıdaki sonucu elde ederiz:
>
> | Biçim | Çıktı |
> | :--- | :--- |
> | <div style="max-width: 500px;">`{\clip(m 786.66 445.51 l 869.51 414.15 944.32 410.13 1017.51 428.62 1059.34 461.59 1071.4 529.95 1010.27 588.65 898.47 624.04 811.6 609.56 770.57 570.16 748.05 523.51 752.07 486.52 758.51 468.03)}`</div> | ![clipej2.png](https://media.fansubhub.com/d/uploads/images/aegisub/tags/clipej2.png?sign=cfzeu6_t4oXXvkUgxjEWsk9EsZFojvSwcl09qkH8cjM=:0) |
>
> Gördüğümüz gibi, **eklenmişler**. İkinci `\clip`, birincinin görünürlük alanını genişletti.

> **Bilgi:**
> Ancak, başlangıçtaki `\clip`'i bu diğer saat yönünün tersi efektiyle tekrar eklersek...
>
> | Biçim | Çıktı |
> | :--- | :--- |
> | <div style="max-width: 500px;">`{\clip(m 731.53 514.94 l 765.68 524.38 783.84 512.04 791.1 490.98 785.29 473.54 770.03 467.73 755.51 468.46 735.16 480.08 730.81 490.25 727.17 502.6 703.93 484.44 687.22 480.81 654.53 489.52 643.63 506.95 645.81 530.2 667.6 549.08 699.57 553.44 721.36 546.9 730.08 529.47 730.08 521.48)}`</div> | ![clipej3.png](https://media.fansubhub.com/d/uploads/images/aegisub/tags/clipej3.png?sign=XlD53Hkp0xHrVFlcXLTgY6A06S6ehJ669G0uXX1NEjA=:0) |
>
> Gördüğümüz gibi, ikinci `\clip`'im birincide bir delik açtı.
