Installable font resources and webfont files can be found under their corresponding directories.

本目錄包含可安裝的桌面字型和網頁字型。

otf
===

This directory contains the OpenType/CFF (OTF) font resources in seven weights. This is the configuration for the desktop environment.

本目錄包含七個字重的 OpenType/CFF (OTF) 格式字型。可供桌面裝置使用。

webfont
=======

The `webfont` directory contains the webfont build (in `WOFF2` format) of Chiron Sans HK Pro. The family name of this configuration is **Chiron Sans HK Pro WS**. To start using it, copy the `webfont/css` and `webfont/woff2` directories to your project location and include the corresponding CSS files.

It covers all characters in the Big5 and HKSCS character sets. In addition, characters that are found in the KangXi dictionary and those exclusive to written Cantonese are included. As the webfont targets Traditional Chinese usages, Simplified Chinese characters, Hangul etc. are excluded from this build.

The webfont is optimized with [Unicode-range subsetting](https://web.dev/reduce-webfont-size/#unicode-range-subsetting). The font is broken into smaller pieces, resulting in around 140 tiny subset files per weight (most of them are less than 50KB). Instead of downloading one single and large font file, the browser only needs to download the subset files that contain the glyphs required for rendering the text on a page.

The subsetting strategy mostly follows the one employed by Google Font's [Noto Sans HK](https://fonts.google.com/specimen/Noto+Sans+HK), with Simplified Chinese characters excluded.

For usage example, please check the HTML files named after each font weight in the `webfont/demo` directory which prints all supported characters on a single page.

Due to the limitations of CSS support in existing browsers, the same font weight value 400 is used for both **Normal** and **Regular**. You cannot use both weights in the same page.

`webfont` 目錄內載有昭源黑體的網頁字型版 **Chiron Sans HK Pro WS**，以 `WOFF2` 格式封裝。將 `webfont/css` 和 `webfont/woff2` 目錄複裝到你的專案位置然後載入相關的 CSS 檔就即可使用。

網頁字型是 OTF 檔的子集版，涵蓋整個 Big5/HKSCS 字集，其餘為《康熙字典》字頭、粵語專用字等。網頁字型針對繁體中文用途，沒有收錄簡體中文、諺文等文字。

為改善效能，字型採用了 [Unicode-range subsetting](https://web.dev/reduce-webfont-size/#unicode-range-subsetting) 技術，將每個字重的單一字型檔拆分成大約 140 個細小檔案（多數檔案小於 50KB，非常用字子集小於 150KB），並在 CSS 指明該檔案所涵蓋的字碼。瀏覽器只會在網頁有用到該字碼時才會載入相關字型檔。這樣做的好處是大大減低須下載字型檔案的大小。收字方式如下：

1. 先以 Google Fonts 服務中 [Noto Sans HK](https://fonts.google.com/specimen/Noto+Sans+HK) 的拆分方式為基礎。據知 Google Fonts 在日、韓兩種語言利用了 machine learning 產生 subset，務求在最小下載檔案數之下得到最多的常用字元。雖然未知繁體中文是否也是如此，但最終應該也會用上，所以決定先跟隨 Google Fonts 的 subsetting 方法。不過，Google Fonts 的繁體子集會包含一些不在 Big5/HKSCS 的簡化字，處理時會予以過濾。
2. 本網頁字型會補上一些香港常用字符。
3. 最後，補充 Big5/HKSCS 字集和字集外、本字體有收的非常用漢字（多屬《康熙字典》字頭，也有一些粵語用字）。雖然為數不少，但由於採用了 Unicode-range subsetting，加入這些字符對一般使用者相信影響不大。

目錄內另包含以字重命名的 HTML 檔案，會印出所有網頁字型的覆蓋字元，作為應用示範。

注意：由於目前瀏覽器的 CSS 支援所限，**Normal** 和 **Regular** 的字重數字均設定為 400，同一頁面不能同時使用這兩種字重。
