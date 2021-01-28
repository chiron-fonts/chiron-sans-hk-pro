Chiron Sans HK Pro Webfont
==========================

## About

This package contains the web font version of [Chiron Sans HK Pro (昭源黑體)](https://github.com/chiron-fonts/chiron-sans-hk-pro) that can be used with websites.

Similar to Chiron Sans HK, Chiron Sans HK Pro is a CJK typeface derived from the Source Han Sans / Noto Sans CJK font family. It aims to provide a modern, region-agnostic glyph set adopting the “written” style that is similar to the prevailing, usually commercial, typefaces such that it is suitable for use in a Traditional Chinese environment. The difference is that the Pro version has integrated the full character set in Source Sans 3 into it, thus providing a richer coverage of Latin, Greek and Cyrillic characters and symbols.   

Chiron Sans HK Pro is available in two configurations: OpenType/CFF (OTF) and webfont version in WOFF File Format 2.0 (WOFF2) format. The webfont version utilizes Unicode-range subsetting technology to reduce download size and improve loading performance. This package contains only the webfont configuration (i.e. the CSS and web font files) for easy self-hosting.

## Usage

First, install this package:

```bash
npm install chiron-sans-hk-pro-webfont 
```

To use this font in your web pages, import the CSS file of the desired font weights in the `css/` directory. For instance, if you use [webpack](https://webpack.js.org/), you would import the font's CSS files with the following statements (just import the weights you want to use): 

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
| Normal | 400 |
| Regular | 400 |
| Medium | 500 |
| Bold | 700 |
| Heavy | 900 |

Note that the CSS font weight value of _Normal_ and _Regular_ are identical, so you can only use either one on a webpage.

## Licensing

Chiron Sans Pro HK is licensed under the SIL Open Font License, Version 1.1. The full text of the license is available at [https://scripts.sil.org/OFL_web](https://scripts.sil.org/OFL_web).
