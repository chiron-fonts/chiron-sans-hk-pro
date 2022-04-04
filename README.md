Chiron Sans HK Pro (昭源黑體 Pro)
==================

### ⚠️ Important Notice ⚠️

**This project is superseded by [Chiron Hei HK](https://github.com/chiron-fonts/chiron-hei-hk), and will no longer be maintained. Check out the [Chiron Font website](https://chiron-fonts.github.io/technical-details/chiron-sans-fonts-differences/) (in Chinese) for the details behind this move.**

---

[中文版說明 Chinese README](README.zh.md)

## Overview

> TL;DR: Chiron Sans HK + Source Sans 3 = Chiron Sans HK Pro

_Chiron Sans HK Pro_ (昭源黑體 Pro) is a sans-serif CJK typeface. Build upon [Chiron Sans HK (昭源黑體)](https://github.com/chiron-fonts/chiron-sans-hk), it incorporates the entire character set found in [Source Sans Pro](https://github.com/adobe-fonts/source-sans-pro/).

_Chiron Sans HK_ is modified from the Traditional Chinese – Hong Kong variant of _Source Han Sans_. It aims to provide a modern, region-agnostic glyph set adopting the “written” style that is similar to the prevailing, usually commercial, typefaces such that it is suitable for use in a Traditional Chinese environment. While the Latin, Latin-like, Greek, and Cyrillic (LGC) glyphs of _Source Han Sans_ (and thus _Chiron Sans HK_, they are mostly identical in terms of non-ideographic characters) are derived from _Source Sans Pro_, it has a fairly limited coverage due to the technical limitation on the maximum number of glyphs allowed in a single font file. Not much space can be reserved for non-CJK characters because of the multi-language and pan-CJK nature of _Source Han Sans_. Thus, it is possible for characters covered by _Source Sans Pro_ to be found missing in _Source Han Sans_, as shown in the following sample:

![Sample text in Source Sans Pro](doc/source-sans-pro-sample.png "Sample text in Source Sans Pro")

![Missing characters in Source Han Sans](doc/source-han-sans-missing-chars-sample.png "Missing characters in Source Han Sans")

Unfortunately, using _Source Sans Pro_ as a fallback to _Source Han Sans_ is not a solution. This is because the LGC glyphs in _Source Sans Pro_ have been manipulated to harmonize with the other parts of _Source Han Sans_ before integration. The glyphs are scaled and interpolated differently, so mixing the two fonts will not yield any good result:

![Source Han Sans with Source Sans Pro as fallback](doc/source-sans-fallback-sample.png "Source Han Sans with Source Sans Pro as fallback")

As _Chiron Sans HK_ aims to provide an opinionated version of CJK Ideographs via remapping and redesigning of existing glyphs, non-default CJK glyphs in the font can be removed. This results in around 16,900 glyph spaces (CIDs) being freed up for other uses. _Chiron Sans HK Pro_ takes this opportunity to include the entire glyph set of _Source Sans Pro_ into it.

![Chiron Sans HK Pro Sample](doc/chiron-sans-hk-pro-sample.png "Chiron Sans HK Pro Sample")

## Features

_Chiron Sans HK Pro_ offers the following features:

* The following features found in _Chiron Sans HK_ are included:
  - More than 2,700 remapped ideographs.
  - More than 1,600 redesigned ideographs.
  - More than 1,000 ideographs uncovered by the original _Source Han Sans_.
  - The proportional variant of U+2018 (‘), U+2019 (’), U+201C (“) and U+201D (”) are served by default.
  - `halt`, `vhal`, `palt`, and `vpal` instructions for full-width punctuations have been removed.
* The entire character set covered by the latest version of _Source Sans Pro_ (version 3).
* OpenType features in the original _Source Sans Pro_ font.

## Installation

Installable font resources can be found in the `build/` directory. It contains the OpenType/CFF (OTF) font resources in 7 weights and a OpenType/CFF2 variable font version for desktop use. There is also a webfont build for use on websites.

Note that the _ExtraLight_ instance of the font has been renamed to _ExtraLt_ to circumvent the font menu name character limit on Windows.

## Integration Details

This section provides some information on the integration of _Source Sans Pro_'s glyph set into _Chiron Sans HK_ to produce _Chiron Sans HK Pro_. Note that the situation in _Chiron Sans HK_ also applies to its upstream, _Source Han Sans_.

### LGC Glyphs

Just like _Source Han Sans_, the LGC glyphs from _Source Sans Pro_ have been manipulated so that they can be adapted for use in _Chiron Sans HK Pro_. However, the scaling and interpolation ratio are different from that of _Source Han Sans_.

First, I do not know the exact configuration that is used to build the customized _Source Sans Pro_ for use in _Source Han Sans_, and due to the difference of the integration workflow I probably cannot reproduce the exact settings. Second, for each weight I have intentionally picked a smaller scaling ratio than that is adopted by _Source Han Sans_.

This means that the building process of _Chiron Sans HK Pro_ is not only about filling the missing glyphs with those found in _Source Sans Pro_. It also replaces existing LGC glyphs that already exist in _Chiron Sans HK_ with those in the processed _Source Sans Pro_ glyph set.

Therefore, the metrics of the LGC characters in _Chiron Sans HK Pro_ are different from _Chiron Sans HK_ and _Source Han Sans_. One should not see _Chiron Sans HK Pro_ as a drop-in replacement of _Chiron Sans HK_ or _Source Han Sans_.

### Features

_Source Sans Pro_ is very rich in OpenType features. This includes alternate letterforms and rules that are essential for correct rendering of characters. These have been preseved in _Chiron Sans HK Pro_ with best effort. They supercedes the same features defined in the _Chiron Sans HK_ or _Source Han Sans_.

### Additional Stylistic Alternates

While it is mentioned that existing LGC glyphs in _Chiron Sans HK Pro_ are replaced by those in _Source Sans Pro_, special cases do exist. A small number of characters, which are mostly symbols like ▲, ♠, ←, etc., are proportional in _Source Sans Pro_ but appear full-width in _Chiron Sans HK_ or _Source Han Sans_ because people using a Chinese typeface would mostly prefer these glyphs be rendered in full-width. For these glyphs it would be inappropriate to blindly replacing them with the proportional version. Thus the following arrangements:

#### Full-width as Default

For the following characters, the full-width version in _Chiron Sans HK_ will be served as the default. Their corresponding proportional version from _Source Sans Pro_ can still be accessed via language-tagging (`locl` feature) or through OpenType's Stylistic Set (`ss11`) / Character Variants (`cv20`) features.

> ←, ↑, →, ↓, ↖, ↗, ↘, ↙, ⇐, ⇒, ↔, ↕, ●, ○, ■, □, ◆, ▲, △, ▶, ▷, ▼, ▽, ◀, ◁, ◉, ♥, ♣, ♦, ♠, ♀, ♁, ♂

#### Proportional as Default

For the following characters, the proportional version in _Source Sans Pro_ will be served as the default. The full-width version found in _Chiron Sans HK_ can be accessed via OpenType's Stylistic Set (`ss12`) / Character Variants (`cv21`) features.

> ·, •, ×, ÷, ◦, ▪, ▫, †, ‡, §, ¶, ‖, ∕, ≤, ≥, ±, ≠, ≈, ∩, ∟, ∞, ‵, √, ∀, ∃, ∶, ∷, ∑, ∏, ℅.

### Numeric Characters 

_Source Han Sans_ offers an alternate set of punctuations and digits that is better suited for CJK typesetting. For numeric characters U+0030 (0) to U+0039 (9), the CJK-optimized version is served by default, and the corresponding Western forms can be activated by language tagging (`locl` feature). The CJK-optimized version is not available in _Source Sans Pro_.

On the other hand, in _Source Sans Pro_, the height of numerals are a bit lower than that of capital letters by default. Cap-height numerals can be accessed via OpenType's `case` feature.

In _Chiron Sans HK Pro_, the cap-height version becomes the default and is always served. In addition, the `locl` feature to switch between CJK-optimized and Western forms in _Source Han Sans_ / _Chiron Sans HK_ is removed.

### Other changes

The following changes are applied for my personal preference:

1. The single storey version of U+0067 (g) has been made the default form, and the original double storey U+0067 (g) is provided as an alternate form through `ss04` / `cv03`.
2. The foot of U+0031 (1) has been removed.
3. The em-centered versions of U+203C (‼), U+2047 (⁇), U+2048 (⁈) and U+2049 (⁉) have been modified such that they now occupy the full-em width, and are served as default. Proportional forms from _Source Sans Pro_ can be accessed via Opentype feature `ss11` or `cv20`.
4. For U+2E3A (⸺) and U+2E3B (⸻), the Western version will be served by default in _Source Han Sans_ and _Chiron Sans HK_, and the CJK-optimized glyphs can only be accessed via language tagging. Certain applications (like Microsoft Word) does not support language tagging for these codepoints very well. In _Chiron Sans HK Pro_, the CJK-optimized version becomes the default, and their corresponding Western form can be accessed via Opentype feature `ss11` or `cv20`.

## License

Chiron Sans HK Pro is licensed under the SIL Open Font License, Version 1.1. The full text of the license is available at [https://scripts.sil.org/OFL_web](https://scripts.sil.org/OFL_web).
