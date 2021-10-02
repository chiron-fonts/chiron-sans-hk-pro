Installable font resources and webfont files can be found under their corresponding directories.

本目錄包含可安裝的桌面字型和網頁字型。

otf
===

This directory contains the OpenType/CFF (OTF) font resources in seven weights. This is a configuration for the desktop environment. The font family name is **Chiron Sans HK Pro**

本目錄包含七個字重的 OpenType/CFF (OTF) 格式字型。可供桌面裝置使用。安裝後的字型名稱是 **Chiron Sans HK Pro**。

variable
========

**⚠ WARNING: As of the date of this release, Windows 10/11 is still problematic in handling the CFF2 Variable Font format adopted by this typeface. Until this is fixed, DO NOT install the variable font format (ChironSansHKVF.otf) if you are using Windows 10/11. While you can install it, Windows font engine will crash whenever the font is accessed. A reboot is required when this happens.**

This directory contains the OpenType/CFF2 (OTF) variable font resource, users can select an arbitrary font weight between the ExtraLight and Heavy instances.

The font family name for this configuration is **Chiron Sans HK Pro VF**. It can be installed alongside the static OTF configuration.

Note that this configuration requires a system and/or application that supports OpenType/CFF2 variable font format.

**⚠️ 注意：Windows 10/11 目前不能正確處理本字體所使用的 CFF2 可變字型格式。在 Microsoft 修復此問題之前，使用者切勿在 Windows 10/11 安裝可變式可型版本（ChironSansHKVF.otf）。雖然字體能正常安裝，使用者存取字型時卻會導致系統字型引擎崩潰而必須重新開機。**

本目錄包含 OpenType/CFF2 (OTF) 可變式字型 (Variable Font)。使用者可任意揀選 ExtraLight 和 Heavy 之間的字重值。

安裝後的字體名稱是 **Chiron Sans HK Pro VF**，可與固定字重 OTF 版本同時安裝。

留意使用者的作業系統或應用程式必須支援可變式字型格式才能正常使用。

webfont
=======

The `webfont` directory contains the webfont build (in `WOFF2` format) of Chiron Sans HK Pro. The family name of this configuration is **Chiron Sans HK Pro WS**. To start using it, copy the `webfont/css` and `webfont/woff2` directories to your project location and include the corresponding CSS file. The webfont build is now available in variable font format, so you just need to include a single CSS file to access all possible font weights.

It covers all characters in the Big5 and HKSCS character sets. In addition, characters that are found in the KangXi dictionary and those exclusive to written Cantonese are included. As the webfont targets Traditional Chinese usages, Simplified Chinese characters, Hangul etc. are excluded from this build.

The webfont is optimized with [Unicode-range subsetting](https://web.dev/reduce-webfont-size/#unicode-range-subsetting). The font is broken into smaller pieces, resulting in around 140 tiny subset files per weight. Instead of downloading one single and large font file, the browser only needs to download the subset files that contain the glyphs required for rendering the text on a page.

The subsetting strategy mostly follows the one employed by Google Font's [Noto Sans HK](https://fonts.google.com/specimen/Noto+Sans+HK), with Simplified Chinese characters excluded.

For usage example, please check the HTML file in the `webfont/demo` directory which prints all supported characters on a single page.

`webfont` 目錄內載有昭源黑體的網頁字型版 **Chiron Sans HK Pro WS**，以 `WOFF2` 格式封裝。將 `webfont/css` 和 `webfont/woff2` 目錄複裝到你的專案位置然後載入相關的 CSS 檔就即可使用。網頁字型以「可變式字型」格式提供，只須載入一個 CSS 檔案就可以用到全部字重。

網頁字型是 OTF 檔的子集版，涵蓋整個 Big5/HKSCS 字集，其餘為《康熙字典》字頭、粵語專用字等。網頁字型針對繁體中文用途，沒有收錄簡體中文、諺文等文字。

為改善效能，字型採用了 [Unicode-range subsetting](https://web.dev/reduce-webfont-size/#unicode-range-subsetting) 技術，將每個字重的單一字型檔拆分成大約 140 個細小檔案，並在 CSS 指明該檔案所涵蓋的字碼。瀏覽器只會在網頁有用到該字碼時才會載入相關字型檔。這樣做的好處是大大減低須下載字型檔案的大小。收字方式如下：

1. 先以 Google Fonts 服務中 [Noto Sans HK](https://fonts.google.com/specimen/Noto+Sans+HK) 的拆分方式為基礎。據知 Google Fonts 在日、韓兩種語言利用了 machine learning 產生 subset，務求在最小下載檔案數之下得到最多的常用字元。雖然未知繁體中文是否也是如此，但最終應該也會用上，所以決定先跟隨 Google Fonts 的 subsetting 方法。不過，Google Fonts 的繁體子集會包含一些不在 Big5/HKSCS 的簡化字，處理時會予以過濾。
2. 本網頁字型會補上一些香港常用字符。
3. 最後，補充 Big5/HKSCS 字集和字集外、本字體有收的非常用漢字（多屬《康熙字典》字頭，也有一些粵語用字）。雖然為數不少，但由於採用了 Unicode-range subsetting，加入這些字符對一般使用者相信影響不大。

`webfont/demo` 目錄內包含一 HTML 檔，會印出所有網頁字型的覆蓋字元，作為應用示範。
