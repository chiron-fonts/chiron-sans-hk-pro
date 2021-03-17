Chiron Sans HK Pro Webfont
==========================

## About

This package provides the webfont version of [Chiron Sans HK Pro (昭源黑體 Pro)](https://github.com/chiron-fonts/chiron-sans-hk-pro) that can be used in webpages.

Similar to Chiron Sans HK, Chiron Sans HK Pro is a CJK typeface derived from the Source Han Sans / Noto Sans CJK font family. Its goal is to provide a modern, region-agnostic glyph set adopting the “written” style that is similar to the prevailing, usually commercial, typefaces such that it is suitable for use in a Traditional Chinese environment. While Chiron Sans HK provides exactly the same amount of Latin, Greek and Cyrillic (LGC) characters as in Source Han Sans, Chiron Sans HK Pro integrates the entire glyph set of Source Sans 3 into it, thus providing an even richer coverage of LGC characters and symbols.   

Chiron Sans HK Pro comes with two configurations: OpenType/CFF (OTF) and webfont version in WOFF File Format 2.0 (WOFF2) format. The webfont version utilizes Unicode-range subsetting technology which allows the browser to only download the subset(s) of the font it needs on a page. This means reduced download sizes and improved loading performance. This package contains only the webfont configuration (i.e. the CSS files and WOFF 2.0 font resources) for easy self-hosting.

## Usage

First, install this package:

```bash
npm install chiron-sans-hk-pro-webfont 
```

To use the font, import the CSS file of the desired font weights in the `css/` directory. For instance, if you use [webpack](https://webpack.js.org/), you would import the font's CSS files with the following statements (just import the weights you want to use): 

```css
@import '~chiron-sans-hk-pro-webfont/css/ExtraLight.css';
@import '~chiron-sans-hk-pro-webfont/css/Light.css';
@import '~chiron-sans-hk-pro-webfont/css/Normal.css';
@import '~chiron-sans-hk-pro-webfont/css/Regular.css';
@import '~chiron-sans-hk-pro-webfont/css/Medium.css';
@import '~chiron-sans-hk-pro-webfont/css/Bold.css';
@import '~chiron-sans-hk-pro-webfont/css/Heavy.css';
```

Now you can access this font by specifying the `Chiron Sans HK Pro WS` font family in your stylesheet. For instance:

```css
body {
    font-family: "Chiron Sans HK Pro WS", sans-serif;
}
```

Please refer to the following table for the CSS `font-weight` values of different font weights:

| Font Weight | CSS font-weight Value |
|---|---|
| ExtraLight | 100 |
| Light | 300 |
| Normal | 370 |
| Regular | 400 |
| Medium | 500 |
| Bold | 700 |
| Heavy | 900 |


## Licensing

Chiron Sans Pro HK is licensed under the SIL Open Font License, Version 1.1. The full text of the license is available at [https://scripts.sil.org/OFL_web](https://scripts.sil.org/OFL_web).
