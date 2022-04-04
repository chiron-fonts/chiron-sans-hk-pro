Chiron Sans HK Pro Webfont
==========================

## DEPRECATION NOTICE

**This project is superseded by [Chiron Hei HK](https://github.com/chiron-fonts/chiron-hei-hk) and is no longer maintained. New users are highly recommended to start with [Chiron Hei HK](https://github.com/chiron-fonts/chiron-hei-hk) instead. For the details behind this move, check out the [Chiron Font website](https://chiron-fonts.github.io/technical-details/chiron-sans-fonts-differences/) (in Chinese only). **

## About

This package provides the webfont version of [Chiron Sans HK Pro (昭源黑體 Pro)](https://github.com/chiron-fonts/chiron-sans-hk-pro) that can be used in webpages.

Similar to Chiron Sans HK, Chiron Sans HK Pro is a CJK typeface derived from the Source Han Sans / Noto Sans CJK font family. Its goal is to provide a modern, region-agnostic glyph set adopting the “written” style that is similar to the prevailing, usually commercial, typefaces such that it is suitable for use in a Traditional Chinese environment. While Chiron Sans HK provides exactly the same amount of Latin, Greek and Cyrillic (LGC) characters as in Source Han Sans, Chiron Sans HK Pro integrates the entire glyph set of Source Sans 3 into it, thus providing an even richer coverage of LGC characters and symbols.   

Chiron Sans HK Pro comes with three configurations: OpenType/CFF (OTF), OpenType/CFF2 (OTF) variable font, and webfont version in WOFF File Format 2.0 (WOFF2) format. The webfont version utilizes Unicode-range subsetting technology which allows the browser to only download the subset(s) of the font it needs on a page. This means reduced download sizes and improved loading performance. This package contains only the webfont configuration (i.e. the CSS file and WOFF 2.0 font resources) for easy self-hosting.

Check out the [official website (Chinese only)](https://chiron-fonts.github.io/sans/) for usage example.

## Usage

First, install this package:

```bash
npm install chiron-sans-hk-pro-webfont 
```

Include the `css/vf.css` file in your web page to start using it. You may also include `css/vf-italic.css` for the italic style of the typeface. For instance, if you use [webpack](https://webpack.js.org/), you would import the font's CSS files with the following statements:

```css
@import '~chiron-sans-hk-webfont/css/vf.css';
@import '~chiron-sans-hk-webfont/css/vf-italic.css';
```

Now you can access this font by specifying the `Chiron Sans HK Pro WS` font family in your stylesheet. For instance:

```css
body {
    font-family: "Chiron Sans HK Pro WS", sans-serif;
}
```

The table below shows the corresponding `font-weight` values of the default static font weights. Since this is a variable font, you can also specify any value between 250 and 900 to the `font-weight` property.

| Font Weight | CSS font-weight Value |
|---|---|
| ExtraLight | 250 |
| Light | 300 |
| Normal | 350 |
| Regular | 400 |
| Medium | 500 |
| Bold | 700 |
| Heavy | 900 |


## Licensing

Chiron Sans Pro HK is licensed under the SIL Open Font License, Version 1.1. The full text of the license is available at [https://scripts.sil.org/OFL_web](https://scripts.sil.org/OFL_web).
