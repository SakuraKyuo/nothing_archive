[English](README.md) | [Deutsch](README_de-DE.md) | [Español](README_es-ES.md) | [Français](README_fr-FR.md) | **हिन्दी** | [Italiano](README_it-IT.md) | [日本語](README_ja-JP.md) | [Русский](README_ru-RU.md) | [Türkçe](README_tr-TR.md) | [简体中文](README_zh-CN.md)

# Nothing Archive

<img src="../assets/branding/logo.png" width="96" alt="Nothing Archive लोगो">

[![Hits](https://hitscounter.dev/api/hit?url=https%3A%2F%2Fgithub.com%2Fspike0en%2Fnothing_archive&label=Hits&icon=github&color=%23b02a37)](https://github.com/spike0en/nothing_archive)

[![Stars](https://img.shields.io/github/stars/spike0en/nothing_archive?label=Stars&logo=github&logoColor=white&color=fb481f&labelColor=1E1E2F&style=flat)](https://github.com/spike0en/nothing_archive/stargazers)
[![Contributors](https://img.shields.io/github/contributors/spike0en/nothing_archive?label=Contributors&logo=github&logoColor=white&color=2b2a7b&labelColor=1E1E2F&style=flat)](https://github.com/spike0en/nothing_archive/graphs/contributors)
[![Forks](https://img.shields.io/github/forks/spike0en/nothing_archive?label=Forks&logo=github&logoColor=white&color=eeb705&labelColor=1E1E2F&style=flat)](https://github.com/spike0en/nothing_archive/network/members)

[![Total Downloads](https://img.shields.io/github/downloads/spike0en/nothing_archive/total?label=Downloads&logo=github&logoColor=white&color=9E9D10&labelColor=1E1E2F&style=flat)](https://github.com/spike0en/nothing_archive/releases)
[![Latest Release](https://img.shields.io/github/release/spike0en/nothing_archive?label=Latest&logo=git&logoColor=white&color=18673F&labelColor=1E1E2F&style=flat)](https://github.com/spike0en/nothing_archive/releases/latest)

[![Flashing Scripts](https://img.shields.io/badge/Fastboot%20Flashing%20Scripts-1E1E2F?logo=github&logoColor=white&labelColor=1E1E2F&color=67119E&style=flat)](https://github.com/spike0en/nothing_flasher)
[![Support](https://img.shields.io/badge/Nothing%20Community-1E1E2F?style=flat&logo=telegram&logoColor=white&color=1986F2&labelColor=1E1E2F)](https://t.me/s/Nothing_Archive)

---

## अनुक्रमणिका 📑

- [परियोजना के बारे में](#अवलोकन-)
- [अस्वीकरण](#अस्वीकरण-)
- [टिप्पणियाँ](#टिप्पणियाँ-)
- [वर्गीकरण](#वर्गीकरण-)
- [डाउनलोड](#डाउनलोड-)
- [अखंडता जाँच](#अखंडता-जाँच-)
- **गाइड**
  - [OTA साइडलोडिंग](#i-ota-साइडलोडिंग-)
  - [बूटलोडर अनलॉक करना](#ii-बूटलोडर-अनलॉक-करना-)
  - [पार्टीशन का बैकअप लेना](#iii-बूटलोडर-अनलॉक-करने-के-बाद-आवश्यक-पार्टीशन-का-बैकअप-लेना-)
  - [Fastboot का उपयोग करके स्टॉक ROM फ्लैश करना](#iv-fastboot-का-उपयोग-करके-स्टॉक-रोम-फ्लैश-करना-)
  - [बूटलोडर को फिर से लॉक करना](#v-बूटलोडर-को-फिर-से-लॉक-करना-)
- [स्वीकृतियाँ](#स्वीकृतियाँ-)
- [परियोजना का समर्थन करें](#परियोजना-का-समर्थन-करें-)

---

## अवलोकन 🔍

**Nothing Archive** सबसे अद्यतित Nothing OS फर्मवेयर रिपॉजिटरी है, जो **Nothing Phone 1, Phone 2, Phone 2a, Phone 2a Plus, Phone 3a, Phone 3a Pro**, और **CMF Phone 1** के लिए आधिकारिक OTA अपडेट, पूर्ण फर्मवेयर पैकेज और स्टॉक OTA इमेज प्रदान करता है, जो सभी सीधे आधिकारिक OEM सर्वर से प्राप्त किए गए हैं। सभी फाइलें [आर्काइव](https://archive.org/details/nothing-archive) की गई हैं, जिससे आसान पहुँच और दीर्घकालिक संरक्षण सुनिश्चित होता है।

### विशेषताएँ और लाभ:

- 📡 **सीधा OTA इंडेक्सिंग** – आधिकारिक सर्वर से **Nothing OS OTA अपडेट लिंक** को ट्रैक करता है, Nothing और CMF उपकरणों के लिए **वृद्धिशील और पूर्ण अपडेट** तक पहुँच प्रदान करता है।
- 🛠️ **मैन्युअल इंस्टॉलेशन (साइडलोडिंग)** – चरणबद्ध रोलआउट के दौरान या जब OTA अपडेट विफल हो जाते हैं, तो इनबिल्ट **Nothing OS ऑफलाइन अपडेटर या बीटा अपडेटर ऐप** का उपयोग करके या उपलब्ध होने पर कस्टम रिकवरी का उपयोग करके **ADB साइडलोड** के माध्यम से **Nothing OS फर्मवेयर को मैन्युअल रूप से इंस्टॉल करें**।
- 📦 **स्टॉक OTA इमेज** – AOSP के OTA एक्सट्रैक्शन टूल का उपयोग करके **अपरिवर्तित OTA इमेज** प्रदान करता है जो वृद्धिशील OTA अपडेट निकालने की अनुमति देता है, इस प्रकार **पूर्ण फर्मवेयर पैकेज** अनुपलब्ध होने पर **अपग्रेड, डाउनग्रेड और पार्टीशन फ्लैशिंग** को सक्षम करता है।
- 🔓 **रूटिंग और अनरूटिंग सपोर्ट** – **Magisk, KernelSU, और Apatch के लिए स्टॉक बूट इमेज** प्रदान करता है, साथ ही संशोधित पार्टीशन का पता चलने पर मूल बूट इमेज को फ्लैश करके **OTA अपडेट को कार्यात्मक** रखने के लिए **अनरूटिंग** की अनुमति देता है।
- ⚡ **फर्मवेयर फ्लैश करें और डिवाइस अनब्रिक करें** – **fastboot-फ्लैश करने योग्य Nothing OS फर्मवेयर** प्रदान करता है ताकि **बूट लूप को हल करने, सॉफ्ट-ब्रिक्ड डिवाइस को पुनर्प्राप्त करने और स्टॉक ROM को पुनर्स्थापित करने** में मदद मिल सके, जब तक कि fastboot सुलभ हो।

---

## अस्वीकरण 🚨

इस संग्रह का उपयोग करके, उपयोगकर्ता इन शर्तों को स्वीकार करते हैं:
- **✅ प्रामाणिकता** – इस संग्रह में सभी फर्मवेयर फाइलें **अपरिवर्तित, असंशोधित और सीधे OEM से प्राप्त** की गई हैं।
- **⚠️ अपने जोखिम पर फ्लैश करें** – **अनलॉक किए गए बूटलोडर** वाले डिवाइस पर फर्मवेयर इंस्टॉल करने में अंतर्निहित जोखिम होते हैं। **अपने डिवाइस को ब्रिक करने से बचने** के लिए निर्देशों का सावधानीपूर्वक पालन करें।
- **📌 संगतता** – इंस्टॉलेशन से पहले सुनिश्चित करें कि फर्मवेयर आपके **Nothing या CMF डिवाइस संस्करण** से मेल खाता है।
- **🚫 कोई वारंटी या आधिकारिक समर्थन नहीं** – यह एक **समुदाय-संचालित परियोजना है, जो [Nothing](https://nothing.tech) से असंबद्ध** है। कोई भी **अपडेट विफलता, सॉफ़्टवेयर बग, या डिवाइस समस्याएँ** OEM की ज़िम्मेदारी बनी रहती हैं। लेखक और योगदानकर्ता गलत फ्लैशिंग, दुरुपयोग, या फर्मवेयर संशोधनों के कारण **ब्रिक्ड डिवाइस के लिए उत्तरदायी नहीं हैं**। अखंडता सुनिश्चित करने के लिए हमेशा **इस संग्रह से सीधे** फर्मवेयर डाउनलोड करें।
- **🛡️ ओपन सोर्स अखंडता** – पुनर्वितरण की अनुमति **केवल उचित श्रेय के साथ** है। उपयोगकर्ताओं को **इसकी उपलब्धता बनाए रखने के लिए** इस परियोजना का समर्थन और साझा करने के लिए प्रोत्साहित किया जाता है। **स्वतंत्र रूप से उपलब्ध फर्मवेयर को फिर से बेचना सख्त वर्जित है!**

---

## टिप्पणियाँ 📝

- OTA इमेज के लिए रिलीज़ को `<POST_OTA_VERSION>` और `<POST_OTA_VERSION>`_`<NothingOS संस्करण>` प्रारूप का उपयोग करके टैग और नामित किया जाता है, जैसा कि क्रमशः [यहां](https://github.com/spike0en/nothing_archive/releases) दिखाया गया है।
- क्षेत्र-विशिष्ट रिलीज़ को `<POST_OTA_VERSION>`-`GLO/EEA` प्रारूप का उपयोग करके टैग किया जाता है, जो कुछ पुराने `Spacewar` बिल्ड पर लागू होता है जो एकीकृत नहीं हैं। यहां, GLO = ग्लोबल, और EEA = यूरोपीय आर्थिक क्षेत्र।
- Nothing OS ओपन बीटा रिलीज़ को जहाँ लागू हो `-OB` द्वारा दर्शाया जाता है।
- Android डेवलपर प्रीव्यू रिलीज़ को `0.0.0-dev`+`<डिवाइस कोडनेम>`.`<वृद्धिशील दिनांक>` के रूप में टैग किया जाता है।
- जब तक रिलीज़ नोट्स में विशेष रूप से अन्यथा न कहा गया हो, यहां प्रकाशित रिलीज़ डिवाइस के सभी क्षेत्रीय और रंग वेरिएंट के साथ संगत हैं।
- आवश्यक वृद्धिशील OTA फर्मवेयर की व्याख्या पर विस्तृत निर्देशों के लिए, [इस अनुभाग](#i-ota-साइडलोडिंग-) को देखें।

---

## वर्गीकरण 📂

**अपरिवर्तित** स्टॉक OTA इमेज फाइलें `.7z` प्रारूप में संग्रहीत की जाती हैं और उनके पार्टीशन की प्रकृति के आधार पर तीन अलग-अलग समूहों में वर्गीकृत की जाती हैं: **Boot**, **Firmware**, और **Logical**, संबंधित मॉडलों के लिए इस प्रकार हैं:

[इस](https://github.com/spike0en/nothing_archive/tree/main/docs#categorization-) अनुभाग को देखें।

---

## डाउनलोड 📥

इसके **रिलीज़ इंडेक्स** तक पहुँचने के लिए नीचे दी गई ड्रॉपडाउन सूची से अपना **डिवाइस मॉडल** चुनें:

[इस](https://github.com/spike0en/nothing_archive/tree/main/docs#downloads-) अनुभाग को देखें।

---

## अखंडता जाँच ✅

- आप डाउनलोड की गई OTA इमेज फ़ाइल की अखंडता को निम्न आदेशों में से किसी एक से जाँच सकते हैं:

``` bash
  md5sum -c *-hash.md5
  sha1sum -c *-hash.sha1
  sha256sum -c *-hash.sha256
  xxh128sum -c *-hash.xxh128
```
- xxh128 आमतौर पर सबसे तेज़ होता है।

---

## गाइड 📖

### I. OTA साइडलोडिंग 🔄

> दृश्य संदर्भों के लिए, कृपया [इन छवियों](https://github.com/spike0en/test/tree/main/assets/sideloading) को उनके संबंधित क्रम में देखें।

<br>

A. **अस्वीकरण**
  - आधिकारिक वृद्धिशील OTA अपडेट को साइडलोड करना या मैन्युअल रूप से इंस्टॉल करना **पूरी तरह से सुरक्षित** है, जब तक आप उन्हें **सीधे Spike’s Nothing Archive से डाउनलोड** करते हैं।
  - **तृतीय-पक्ष स्रोतों का उपयोग न करें**—Nothing Archive के सभी फर्मवेयर सीधे OEM के आधिकारिक सर्वर से प्राप्त किए जाते हैं।
  - **अंतर्निहित Nothing OS ऑफलाइन अपडेटर टूल** केवल **OEM द्वारा हस्ताक्षरित** अपडेट स्वीकार करता है, जिससे सुरक्षा सुनिश्चित होती है।
  - **अपडेटर** इंस्टॉलेशन से पहले फर्मवेयर के **हैश को सत्यापित** करता है।

<br>

B. **स्टॉक पार्टीशन को पुनर्स्थापित करना (केवल रूट किए गए उपयोगकर्ताओं के लिए)**
  > **यदि आपका बूटलोडर लॉक है, तो सीधे प्वाइंट C पर जाएं!**

1. **अपना वर्तमान Nothing OS संस्करण जांचें:**
   - `सेटिंग्स > फ़ोन के बारे में > डिवाइस बैनर पर टैप करें` पर जाएं।
   - बिल्ड नंबर नोट करें।

2. **अपने वर्तमान फर्मवेयर बिल्ड के लिए स्टॉक इमेज प्राप्त करें:**
   - `-boot-image.7z` फ़ाइल डाउनलोड करें।
   - `.img` फ़ाइलें प्राप्त करने के लिए संग्रह निकालें।

3. **आवश्यक पार्टीशन की पहचान करें:**
   - **Qualcomm डिवाइस:** `boot`, `init_boot` `vendor_boot`, `recovery`, `vbmeta`
   - **MediaTek डिवाइस:** `init_boot`, `recovery`, `vbmeta`

4. बूटलोडर मोड में **स्टॉक पार्टीशन फ्लैश करें**:
   > केवल संशोधित पार्टीशन को फ्लैश करने की आवश्यकता है। साथ ही अपने SoC प्लेटफॉर्म के आधार पर किसी भी अनुपलब्ध पार्टीशन को छोड़ दें।
   ```sh
   fastboot flash boot boot.img
   fastboot flash recovery recovery.img
   fastboot flash vendor_boot vendor_boot.img
   fastboot flash vbmeta vbmeta.img
   fastboot flash init_boot init_boot.img
   ```

5. **सिस्टम में रीबूट करें और सिस्टम अपडेटर के माध्यम से अपडेट करें:**
   - यदि अपडेट **विफल** होता है, तो अगले अनुभाग में **मैन्युअल साइडलोडिंग** के साथ आगे बढ़ें।

6. **रूट को पुनर्स्थापित करना (वैकल्पिक):**
   - अपडेट करने के बाद, आप अपडेट किए गए NOS संस्करण के लिए **पैच किए गए बूट इमेज को फ्लैश** करके फिर से रूट कर सकते हैं।
   - फिर से रूट करने के बाद **मॉड्यूल बरकरार रहेंगे**।

<br>

C. **साइडलोडिंग के साथ आगे बढ़ें**

 - **सही अपडेट फर्मवेयर फ़ाइल डाउनलोड करें:**
   - [यहां](#डाउनलोड-) से अपने डिवाइस के लिए सही OTA फर्मवेयर फ़ाइल ढूंढें।

 - **सही फ़ाइल कैसे चुनें?**
   - रिपॉजिटरी पर नेविगेट करें और अपना डिवाइस मॉडल चुनें।
   - वृद्धिशील OTA कॉलम देखें।
   - **अपना वर्तमान OS बिल्ड नंबर सत्यापित करें**:
     - यहां जाएं: `सेटिंग्स > सिस्टम > फ़ोन के बारे में`।
     - **डिवाइस बैनर** पर टैप करें और **बिल्ड नंबर** नोट करें।

 - **उदाहरण:**
   - मान लीजिए कि आपके **Phone (2)** का बिल्ड नंबर है: `Pong_U2.6-241016-1700`
   - यह मानते हुए कि नवीनतम उपलब्ध OTA अपडेट है: `Pong_V3.0-241226-2001`
   - संबंधित अपडेट पाथवे होगा: `Pong_U2.6-241016-1700 -> Pong_V3.0-241226-2001`
   - सुनिश्चित करें कि आप अपने डिवाइस और OS संस्करण के आधार पर सही पाथवे चुनते हैं।
     - बेहतर स्पष्टता के लिए [इसे](https://github.com/spike0en/nothing_archive/blob/main/assets/sideloading/3.1_ota_sideload.jpg) देखें।

 - **`ota` फ़ोल्डर बनाएँ:**
   - अपने डिवाइस के **आंतरिक स्टोरेज** में `ota` नाम का एक फ़ोल्डर बनाएँ, पूरा पथ है:
     ```
     /sdcard/ota/
     ```
   - डाउनलोड की गई `<firmware>.zip` फ़ाइल को इस फ़ोल्डर में ले जाएँ।

 - **Nothing ऑफलाइन OTA अपडेटर तक पहुँचें:**
    - **फ़ोन ऐप** खोलें और डायल करें:
      ```
      *#*#682#*#*
      ```
   - यह अंतर्निहित ऑफलाइन अपडेटर टूल लॉन्च करेगा।
   - UI `NothingOfflineOtaUpdate` या `NOTHING BETA OTA UPDATE` दिखा सकता है — दोनों काम करते हैं।

 - **अपडेट लागू करें:**
   - अपडेटर स्वचालित रूप से अपडेट फ़ाइल का पता लगाएगा।
   - यदि पता नहीं चलता है, तो मैन्युअल रूप से OTA फ़ाइल ब्राउज़ करें और आयात करें।
   - `Directly Apply OTA` या `Update` (ऐप UI के आधार पर) पर टैप करें।
   - अपडेट पूरा होने तक प्रतीक्षा करें — आपका डिवाइस स्वचालित रूप से रीबूट हो जाएगा।

- **ध्यान दें:**
  - यदि अपडेटर **अज्ञात त्रुटि** दिखाता है, तो फ़ाइल को **"ota"** फ़ोल्डर में मैन्युअल रूप से कॉपी करने के बजाय **"ब्राउज़ करें"** विकल्प का उपयोग करने का प्रयास करें।
  - यदि वृद्धिशील OTA विफल रहता है तो **पूर्ण OTA फर्मवेयर** को साइडलोड किया जा सकता है।
    - **पूर्ण OTA का उपयोग डाउनग्रेड करने के लिए नहीं किया जा सकता है** — यह केवल उसी या उच्चतर बिल्ड में अपडेट कर सकता है।
    - **अनलॉक किए गए बूटलोडर उपयोगकर्ता** कस्टम रिकवरी (जैसे, Phone (2) के लिए OrangeFox) के माध्यम से पूर्ण OTA फ्लैश कर सकते हैं।
  - **हर रिलीज़ में पूर्ण OTA फ़ाइल नहीं होती है** — ऐसे मामलों में इसके बजाय वृद्धिशील का उपयोग करें।

---

### II. बूटलोडर अनलॉक करना 🔓

A. पूर्वापेक्षाएँ
- **अपने डेटा का बैकअप लें** (अनलॉक करने से सब कुछ मिट जाएगा)।
- **ADB और Fastboot टूल इंस्टॉल करें** – [यहां डाउनलोड करें](https://developer.android.com/studio/releases/platform-tools)।
- **USB ड्राइवर इंस्टॉल करें** – [Google USB ड्राइवर](https://developer.android.com/studio/run/win-usb)।
- **डेवलपर विकल्प सक्षम करें**:
  - `सेटिंग्स > फ़ोन के बारे में > "बिल्ड नंबर" पर 7 बार टैप करें।`
- **USB डिबगिंग और OEM अनलॉकिंग सक्षम करें**:
  - `सेटिंग्स > सिस्टम > डेवलपर विकल्प > USB डिबगिंग और OEM अनलॉकिंग सक्षम करें।`
- **स्क्रीन लॉक/पिन/पासवर्ड और लॉग-इन खाते हटाएँ (वैकल्पिक लेकिन अनुशंसित)**
  - बूटलोडर को फिर से लॉक करने से पहले खातों को हटाने से Google FRP (फ़ैक्टरी रीसेट प्रोटेक्शन) लॉक को रोकने में मदद मिलती है। यदि FRP ट्रिगर होता है, तो डिवाइस फ़ैक्टरी रीसेट के बाद पहले से लिंक किए गए Google खाते के लिए पूछेगा। यदि आप क्रेडेंशियल भूल जाते हैं या खाते तक नहीं पहुँच पाते हैं, तो आप अपने डिवाइस से लॉक हो सकते हैं। इससे बचने के लिए, फिर से लॉक करने से पहले सभी Google खातों को हटाने की अनुशंसा की जाती है।

B. अनलॉकिंग प्रक्रिया
- **अपने फ़ोन को USB के माध्यम से पीसी से कनेक्ट करें**।
- प्लेटफ़ॉर्म-टूल फ़ोल्डर में **एक कमांड प्रॉम्प्ट खोलें**:
  - विंडोज: `Shift + राइट क्लिक` > **यहां कमांड प्रॉम्प्ट/Powershell खोलें**।
  - मैक/लिनक्स: **टर्मिनल** खोलें और प्लेटफ़ॉर्म-टूल पर नेविगेट करें।
- **डिवाइस कनेक्शन सत्यापित करें**:
  ```sh
  adb devices
  ```
  यदि संकेत दिया जाए, तो फ़ोन पर USB डिबगिंग की अनुमति दें।

- **बूटलोडर में रीबूट करें:**
   ```sh
   adb reboot bootloader
   ```

- **fastboot कनेक्शन सत्यापित करें:**
   ```sh
   fastboot devices
   ```
   यदि कोई डिवाइस नहीं पाया जाता है, तो USB ड्राइवर पुनः इंस्टॉल करें।

- **बूटलोडर अनलॉक करें:**
   ```sh
   fastboot flashing unlock
   ```

- **अपने फ़ोन पर पुष्टि करें:**
  - नेविगेट करने के लिए **वॉल्यूम कुंजियों** का उपयोग करें और पुष्टि करने के लिए **पावर बटन** का उपयोग करें।
  - आपका डिवाइस **सभी डेटा मिटा देगा** और रीबूट करेगा।

C. अनलॉक के बाद
  - अपने फ़ोन को फिर से सेट करें।
  - **बूटलोडर स्थिति सत्यापित करें**:
    ```sh
    सेटिंग्स > सिस्टम > डेवलपर विकल्प > OEM अनलॉकिंग सक्षम होना चाहिए।
    ```

  - बूटलोडर अब अनलॉक हो गया है और आपका डिवाइस बूट पर ऑरेंज स्टेट चेतावनी दिखाएगा—यह सामान्य है।

---

### III. बूटलोडर अनलॉक करने के बाद आवश्यक पार्टीशन का बैकअप लेना 💾

A. बैकअप क्यों लें?
- बूटलोडर अनलॉक करने के बाद, कस्टम ROM या कर्नेल फ्लैश करने से **पहले** `persist`, `modemst1`, `modemst2`, `fsg`, आदि जैसे आवश्यक पार्टीशन का बैकअप लेना महत्वपूर्ण है।
- इन पार्टीशन में IMEI, नेटवर्क सेटिंग्स और फिंगरप्रिंट सेंसर कैलिब्रेशन सहित महत्वपूर्ण डेटा होता है।
- यदि खो जाता है या दूषित हो जाता है, तो आपके डिवाइस में **सेलुलर कनेक्टिविटी का नुकसान, फिंगरप्रिंट समस्याएँ, या यहाँ तक कि ब्रिक** हो सकता है।
- बैकअप बनाने से यह सुनिश्चित होता है कि यदि कुछ गलत हो जाता है तो आप **अपने डिवाइस को पुनर्स्थापित** कर सकते हैं।

B. आवश्यकताएँ
- **अनलॉक किया गया बूटलोडर**
- **रूट एक्सेस** (Magisk/KSU/Apatch के माध्यम से)
- **Termux ऐप** (F-Droid या Play Store के माध्यम से इंस्टॉल करें)
- **पार्टीशन पथ जांचें:**
  - **Qcom डिवाइस:** `/dev/block/bootdevice/by-name/`
  - **MTK डिवाइस:** `/dev/block/by-name/`

C. बैकअप निर्देश
- **Qualcomm (Qcom) उपकरणों के लिए:**
  - **Termux** खोलें और इसका उपयोग करके रूट एक्सेस प्रदान करें:
    ```sh
    su
    ```

  - निम्नलिखित कमांड को एक बार में कॉपी और पेस्ट करें:
    ```sh
    mkdir -p /sdcard/partitions_backup
    ls -1 /dev/block/bootdevice/by-name | grep -v userdata | grep -v super | \
    while read f; do dd if=/dev/block/bootdevice/by-name/$f of=/sdcard/partitions_backup/${f}.img; done
    ```
    यह **"partitions_backup"** नामक फ़ोल्डर के अंदर **आंतरिक स्टोरेज** में **`super` और `userdata` को छोड़कर सभी पार्टीशन** की इमेज फ़ाइलें बनाएगा।

  - **[वैकल्पिक]** यदि उपरोक्त कमांड विफल रहता है, तो इस विकल्प को आजमाएँ:
    ```sh
    mkdir -p /sdcard/partitions_backup
    for partition in /dev/block/bootdevice/by-name/*; do \
    [[ "$(basename "$partition")" != "userdata" && "$(basename "$partition")" != "super" ]] && \
    cp -f "$partition" /sdcard/partitions_backup/; done
    ```

- **MediaTek (MTK) उपकरणों के लिए:**
  - **Termux** खोलें और इसका उपयोग करके रूट एक्सेस प्रदान करें:
    ```sh
    su
    ```

  - निम्नलिखित सभी कमांड को एक बार में कॉपी और पेस्ट करें:
    ```sh
    mkdir -p /sdcard/partitions_backup/
    cd /sdcard/partitions_backup
    dd if=/dev/block/by-name/nvram of=/sdcard/partitions_backup/nvram.img
    dd if=/dev/block/by-name/nvdata of=/sdcard/partitions_backup/nvdata.img
    dd if=/dev/block/by-name/persist of=/sdcard/partitions_backup/persist.img
    dd if=/dev/block/by-name/nvcfg of=/sdcard/partitions_backup/nvcfg.img
    dd if=/dev/block/by-name/protect1 of=/sdcard/partitions_backup/protect1.img
    dd if=/dev/block/by-name/protect2 of=/sdcard/partitions_backup/protect2.img
    ```

D. बैकअप संग्रहीत करना
  - **"partitions_backup"** फ़ोल्डर को अपने **पीसी या सुरक्षित स्टोरेज** में ले जाएँ।
  - **इन बैकअप को साझा न करें!** इनमें IMEI जैसे अद्वितीय डिवाइस डेटा होते हैं।

E. पार्टीशन पुनर्स्थापित करना
 - **MTK डिवाइस:**
   ```sh
   fastboot flash nvram nvram.img
   fastboot flash nvdata nvdata.img
   fastboot flash nvcfg nvcfg.img
   fastboot flash persist persist.img
   ```
   **रिकवरी मोड** में रीबूट करें → **फ़ैक्टरी रीसेट** करें → **सिस्टम** में रीबूट करें।

 - **QCom डिवाइस:**
   ```sh
   fastboot flash persist persist.img
   fastboot flash modemst1 modemst1.img
   fastboot flash modemst2 modemst2.img
   ```
   **इस मामले में फ़ैक्टरी रीसेट अनिवार्य नहीं है।**

---

### IV. Fastboot का उपयोग करके स्टॉक ROM फ्लैश करना ⚡

A. **फ्लैशिंग फ़ोल्डर की तैयारी:**
  - अपने डिवाइस मॉडल और फर्मवेयर बिल्ड के लिए निम्नलिखित फ़ाइलें डाउनलोड करें और उन्हें एक समर्पित फ़ोल्डर में रखें:
    - image-boot.7z
    - image-firmware.7z
    - image-logical.7z.001-00x

  - [यहां](https://www.7-zip.org/) से 7-Zip इंस्टॉल करें।
  - फ़ाइलें निकालें:
    - विंडोज: राइट-क्लिक → "*\" में निकालें
    - बैश उपयोगकर्ता:
      7za -y x "*7z*"

B. **फ्लैशिंग के साथ आगे बढ़ना:**
  - [यहां](https://developer.android.com/studio/run/win-usb) से संगत USB ड्राइवर इंस्टॉल करें।
  - सुनिश्चित करें कि जब डिवाइस **बूटलोडर मोड** में हो तो **डिवाइस मैनेजर** में `Android Bootloader Interface` दिखाई दे।
  - यदि एक्सट्रैक्शन स्क्रिप्ट का पहले उपयोग किया गया था, तो इसे सीधे निष्पादित करें। अन्यथा:
    - सभी निकाली गई इमेज फ़ाइलों को [Fastboot फ्लैशिंग स्क्रिप्ट](https://github.com/spike0en/nothing_fastboot_flasher/blob/main/README.md#-download) के साथ एक ही फ़ोल्डर में ले जाएँ।
    - हॉटफ़िक्स शामिल हैं यह सुनिश्चित करने के लिए हमेशा नवीनतम स्क्रिप्ट डाउनलोड करें।
  - इंटरनेट से जुड़े रहते हुए स्क्रिप्ट चलाएँ (नवीनतम `platform-tools` लाने के लिए) और संकेतों का पालन करें:
    - पुष्टि प्रश्नावली का उत्तर दें।
    - डेटा मिटाना है या नहीं चुनें: (Y/N)
    - दोनों स्लॉट में फ्लैश करना है या नहीं चुनें: (Y/N)
    - Android सत्यापित बूट अक्षम करें: (N)
  - सत्यापित करें कि सभी पार्टीशन सफलतापूर्वक फ्लैश हो गए हैं।
    - यदि सफल हो, तो सिस्टम में रीबूट करना चुनें: (Y)
    - यदि त्रुटियाँ होती हैं, तो बूटलोडर में रीबूट करें और विफलता को संबोधित करने के बाद फिर से फ्लैश करें।

---

### V. बूटलोडर को फिर से लॉक करना 🔒

A. **पूर्वापेक्षाएँ**
  - **स्क्रीन लॉक/पिन/पासवर्ड और लॉग-इन खाते हटाएँ** (वैकल्पिक लेकिन अनुशंसित)।
  - [फ्लैशिंग गाइड](#iv-fastboot-का-उपयोग-करके-स्टॉक-रोम-फ्लैश-करना-) का पालन करते हुए **स्टॉक ROM** को क्लीन-फ्लैश करें। **स्टॉक फर्मवेयर फ्लैश किए बिना संशोधित पार्टीशन के साथ बूटलोडर को फिर से लॉक करने से डिवाइस ब्रिक हो सकता है!**
  - सभी डेटा का बैकअप लें (फिर से लॉक करने से **सब कुछ मिट जाएगा**)।
  - यदि पहले से सेट नहीं है तो **ADB और Fastboot टूल** और USB ड्राइवर इंस्टॉल करें।

B. **फिर से लॉक करने की प्रक्रिया**
  - यदि आप सिस्टम में हैं, तो बूटलोडर में रीबूट करें:
    ```sh
    adb reboot bootloader
    ```

  - fastboot कनेक्शन सत्यापित करें:
    ```sh
    fastboot devices
    ```

  - बूटलोडर को फिर से लॉक करना शुरू करें:
    ```sh
    fastboot flashing lock
    ```

  - अपने फ़ोन पर पुष्टि करें:
    - नेविगेट करने के लिए **वॉल्यूम कुंजियों** का उपयोग करें और पुष्टि करने के लिए **पावर बटन** का उपयोग करें।
    - डिवाइस स्वरूपित हो जाएगा और लॉक किए गए बूटलोडर के साथ रीबूट होगा।

C. **फिर से लॉक करने के बाद**
  - अपने डिवाइस को फिर से सेट करें।
  - बूटलोडर अब लॉक हो गया है!

---

## स्वीकृतियाँ 🤝

इन योगदानकर्ताओं को उनके अमूल्य कार्य और समर्थन के लिए विशेष धन्यवाद:
- **[luk1337](https://github.com/luk1337/oplus_archive)** – AOSP के OTA एक्सट्रैक्शन टूल के उपयोग का बीड़ा उठाया, जिससे वृद्धिशील OTA अपडेट का निष्कर्षण संभव हुआ।
- **[arter97](https://github.com/arter97/nothing_archive)** – उपरोक्त परियोजना को **Nothing Phone (2)** के लिए अनुकूलित किया।
- **[LukeSkyD](https://github.com/LukeSkyD)** – [Nothing Phone (1) Repo](https://xdaforums.com/t/nothing-phone-1-repo-nos-ota-img-guide-root.4464039/) का रखरखाव करता है, जो पहले के बिल्ड के लिए एक प्रमुख संदर्भ के रूप में कार्य करता था।
- **[XelXen](https://github.com/XelXen)** - परियोजना की ब्रांडिंग के लिए लोगो और बैनर डिजाइन किया।
- उन व्यक्तियों ने जो स्थानीयकरण प्रयासों में योगदान दिया, जिससे इस परियोजना को व्यापक दर्शकों के लिए सुलभ बनाया जा सका।

---

## परियोजना का समर्थन करें ⭐

यदि यह संग्रह सहायक रहा है, तो कृपया **[रिपॉजिटरी को स्टार देने](https://github.com/spike0en/nothing_archive/stargazers)** पर विचार करें। आपका समर्थन परियोजना को खोजने योग्य और सक्रिय रखने में मदद करता है!

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://api.star-history.com/svg?repos=spike0en/nothing_archive&type=Date&theme=dark" />
  <source media="(prefers-color-scheme: light)" srcset="https://api.star-history.com/svg?repos=spike0en/nothing_archive&type=Date" />
  <img alt="स्टार इतिहास चार्ट" src="https://api.star-history.com/svg?repos=spike0en/nothing_archive&type=Date" />
</picture>

---