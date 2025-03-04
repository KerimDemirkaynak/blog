---
author: ["Kerim Demirkaynak"]
title: "Android İçin Firefox'u AMOLED Tema Yapma Rehberi"
date: "2025-03-04"
description: "Bu rehber, Firefox Beta sürümünü düzenleyerek AMOLED uyumlu bir siyah tema eklemenize yardımcı olacaktır."
tags: ["firefox", "firefox beta", "firefox mobile", "amoled tema"]
ShowToc: true
comments: true
cover:
    image: "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRCVLN7nmN3jr4DQnANlPUr-VInjMePo2_zVQ&s" # image path/url
---

## **1. Firefox Beta APK İndirme**  

Öncelikle Firefox'un Beta sürümünü indirmeniz gerekmektedir. Güncel beta sürümlerini aşağıdaki bağlantıdan bulabilirsiniz:  

🔗 **[Firefox Beta APK İndir](https://ftp.mozilla.org/pub/fenix/releases/)**  

İndirdiğiniz APK'yı modifiye etmek için **APK Tool, APK Editor Pro veya MT Manager** gibi bir APK düzenleme aracına ihtiyacınız olacak.  

## **2. APK Dosyasını Açma ve Düzenleme**  

APK dosyanızın içeriğini açmak için tercih ettiğiniz düzenleme aracını kullanın.  

📂 **İlgili dosyanın yolu:**

/res/values-night/colors.xml

Bu dosyayı açtıktan sonra aşağıdaki kodu bulun:  

```xml
<color name="fx_mobile_layer_color_1">@color/photonGrey10</color>
<color name="fx_mobile_layer_color_2">@color/photonDarkGrey80</color>
```
Ve şu şekilde değiştirin:
```
<color name="fx_mobile_layer_color_1">@color/photonBlack</color>
<color name="fx_mobile_layer_color_2">@color/photonDarkGrey90</color>
```
Firefox'un yeni sürümlerinde bazı eksik tanımlamalar olabilir. Eğer derleme hatası alırsanız, colors.xml dosyasının en altına şu satırı ekleyin:
```
<color name="photonBlack">#ff000000</color>
```
## 3. Örnek Tam Kod (Firefox 136.0b9 Sürümü İçin)

Eğer değiştirdiğiniz dosyada referans almak isterseniz, aşağıda tamamlanmış colors.xml dosyası bulunmaktadır.
```
<?xml version="1.0" encoding="utf-8"?>
<resources>
<color name="accent_high_contrast_normal_theme">@color/photonViolet40</color>
<color name="accent_normal_theme">@color/photonViolet50</color>
<color name="add_on_private_browsing_exterior_circle_background_normal_theme">@color/accent_normal_theme</color>
<color name="fill_link_from_clipboard_normal_theme">@color/photonViolet40</color>
<color name="fx_mobile_action_color_critical">@color/photonPink70A69</color>
<color name="fx_mobile_action_color_form_default">@color/photonLightGrey05</color>
<color name="fx_mobile_action_color_form_disabled">@color/photonDarkGrey05</color>
<color name="fx_mobile_action_color_form_on">@color/photonViolet40</color>
<color name="fx_mobile_action_color_form_selected">@color/photonViolet40</color>
<color name="fx_mobile_action_color_form_surface">@color/photonDarkGrey05</color>
<color name="fx_mobile_action_color_indicator_active">@color/photonLightGrey90</color>
<color name="fx_mobile_action_color_indicator_inactive">@color/photonDarkGrey05</color>
<color name="fx_mobile_action_color_information">@color/photonBlue60</color>
<color name="fx_mobile_action_color_primary">@color/photonViolet60</color>
<color name="fx_mobile_action_color_primary_disabled">@color/photonViolet60A50</color>
<color name="fx_mobile_action_color_quarternary">@color/photonDarkGrey80</color>
<color name="fx_mobile_action_color_secondary">@color/photonDarkGrey05</color>
<color name="fx_mobile_action_color_success">@color/photonGreen70</color>
<color name="fx_mobile_action_color_tertiary">@color/photonDarkGrey10</color>
<color name="fx_mobile_action_color_warning">@color/photonYellow40A41</color>
<color name="fx_mobile_border_color_accent">@color/photonViolet40</color>
<color name="fx_mobile_border_color_critical">@color/photonRed20</color>
<color name="fx_mobile_border_color_disabled">@color/photonLightGrey05A40</color>
<color name="fx_mobile_border_color_form_default">@color/photonLightGrey05</color>
<color name="fx_mobile_border_color_inverted">@color/photonLightGrey30</color>
<color name="fx_mobile_border_color_primary">@color/photonDarkGrey05</color>
<color name="fx_mobile_border_color_secondary">@color/photonDarkGrey10</color>
<color name="fx_mobile_border_color_toolbar_divider">@color/photonDarkGrey60</color>
<color name="fx_mobile_icon_color_accent_blue">@color/photonBlue20</color>
<color name="fx_mobile_icon_color_accent_green">@color/photonGreen20</color>
<color name="fx_mobile_icon_color_accent_pink">@color/photonPink20</color>
<color name="fx_mobile_icon_color_accent_violet">@color/photonViolet20</color>
<color name="fx_mobile_icon_color_accent_yellow">@color/photonYellow20</color>
<color name="fx_mobile_icon_color_action_secondary">@color/photonLightGrey05</color>
<color name="fx_mobile_icon_color_action_tertiary">@color/photonLightGrey05</color>
<color name="fx_mobile_icon_color_active">@color/photonViolet40</color>
<color name="fx_mobile_icon_color_button">@color/photonLightGrey05</color>
<color name="fx_mobile_icon_color_critical">@color/photonRed20</color>
<color name="fx_mobile_icon_color_critical_button">@color/photonRed20</color>
<color name="fx_mobile_icon_color_disabled">@color/photonLightGrey05A40</color>
<color name="fx_mobile_icon_color_gradient_end">@color/photonBlue20</color>
<color name="fx_mobile_icon_color_gradient_start">@color/photonViolet20</color>
<color name="fx_mobile_icon_color_primary">@color/photonLightGrey05</color>
<color name="fx_mobile_icon_color_primary_inactive">@color/photonLightGrey05A60</color>
<color name="fx_mobile_icon_color_secondary">@color/photonLightGrey40</color>
<color name="fx_mobile_layer_color_1">@color/photonBlack</color>
<color name="fx_mobile_layer_color_2">@color/photonDarkGrey90</color>
<color name="fx_mobile_layer_color_3">@color/photonDarkGrey80</color>
<color name="fx_mobile_layer_color_accent">@color/photonViolet40</color>
<color name="fx_mobile_layer_color_accent_nonopaque">@color/photonViolet50A32</color>
<color name="fx_mobile_layer_color_accent_opaque">#ff423262</color>
<color name="fx_mobile_layer_color_critical">@color/photonPink80</color>
<color name="fx_mobile_layer_color_information">@color/photonBlue50</color>
<color name="fx_mobile_layer_color_scrim">@color/photonDarkGrey90A95</color>
<color name="fx_mobile_layer_color_search">@color/photonDarkGrey80</color>
<color name="fx_mobile_layer_color_success">@color/photonGreen80</color>
<color name="fx_mobile_layer_color_warning">@color/photonYellow70A77</color>
<color name="fx_mobile_text_color_accent">@color/photonViolet20</color>
<color name="fx_mobile_text_color_accent_disabled">@color/photonViolet20A60</color>
<color name="fx_mobile_text_color_action_primary_disabled">@color/photonLightGrey05A40</color>
<color name="fx_mobile_text_color_action_secondary">@color/photonLightGrey05</color>
<color name="fx_mobile_text_color_action_tertiary">@color/photonLightGrey05</color>
<color name="fx_mobile_text_color_critical">@color/photonRed20</color>
<color name="fx_mobile_text_color_critical_button">@color/photonRed20</color>
<color name="fx_mobile_text_color_disabled">@color/photonLightGrey05A40</color>
<color name="fx_mobile_text_color_primary">@color/photonLightGrey05</color>
<color name="fx_mobile_text_color_secondary">@color/photonLightGrey40</color>
<color name="mozac_feat_prompt_cancel_save_dialog_text_color">@color/fx_mobile_text_color_accent</color>
<color name="mozac_feature_readerview_text_color">@color/fx_mobile_text_color_primary</color>
<color name="neutral_faded_normal_theme">#1ffbfbfe</color>
<color name="neutral_normal_theme">@color/photonGrey20</color>
<color name="prompt_login_edit_text_cursor_color_normal_theme">@color/photonViolet50</color>
<color name="search_suggestion_indicator_icon_bookmark_color_normal_theme">@color/photonBlue40</color>
<color name="search_suggestion_indicator_icon_color_normal_theme">@color/photonGreen60</color>
<color name="sync_disconnected_background_normal_theme">#ff5b5846</color>
<color name="sync_disconnected_icon_fill_normal_theme">#fffff36e</color>
<color name="toggle_off_knob_normal_theme">@color/toggle_off_knob_dark_theme</color>
<color name="toggle_off_track_normal_theme">@color/toggle_off_track_dark_theme</color>
<color name="photonBlack">#ff000000</color>
</resources>
```

## 4. APK'yı Yeniden Derleme ve Yükleme

Düzenlemeleri tamamladıktan sonra APK'yı tekrar oluşturup cihazınıza yüklemeniz gerekmektedir. Eğer yükleme sırasında "Paket çakışması" hatası alırsanız, APK düzenleme aracınızdaki yükleme konumunu "auto" olarak ayarlayın.

Bu işlemler tamamlandıktan sonra, Firefox'unuzu açın ve AMOLED dostu siyah tema ile kullanmaya başlayın!

---

## 📌 Notlar:

Bu işlem root gerektirmez, ancak APK modifikasyonu yapıldığı için bazı cihazlarda güvenlik uyarıları alabilirsiniz.

Güncellemelerle birlikte renk dosyalarında değişiklik olabilir, bu yüzden her yeni sürümde dosyayı kontrol edip düzenlemeniz gerekebilir.

Eğer hata alırsanız, Firefox'un önceki sürümlerini kullanmayı deneyebilirsiniz.
