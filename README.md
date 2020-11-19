# Kurdish Language Processing Toolkit

<p align="center" width="100%">
    <img width="33%" src="https://raw.githubusercontent.com/sinaahmadi/klpt/master/docs/img/KLPT_logo.png"> 
</p>

<p align="center">
    <a href="">
        <img alt="Build" src="https://badges.frapsoft.com/os/v1/open-source.png?v=103">
    </a>
    <a href="https://github.com/sinaahmadi/KLPT/blob/master/LICENSE">
        <img alt="GitHub" src="https://img.shields.io/badge/license-CC%20BY--SA%204.0-blue">
    </a>
    <a href="https://sinaahmadi.github.io/klpt/">
        <img alt="Documentation" src="https://img.shields.io/website?down_color=green&down_message=online&up_color=orange&url=https%3A%2F%2Fsinaahmadi.github.io%2FKLPT%2F">
    </a>
    <a href="https://gitter.im/KurdishNLP/community?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge">
      <img alt="Documentation" src="https://badges.gitter.im/KurdishNLP/community.svg">
    </a>
</p>

<!--
[![Open Source Love](https://badges.frapsoft.com/os/v1/open-source.png?v=103)](https://github.com/sinaahmadi/KLPT) [![Awesome](https://awesome.re/badge.svg)](https://awesome.re) [![PyPI version fury.io](https://badge.fury.io/py/ansicolortags.svg)]() [![PyPI status](https://img.shields.io/pypi/status/ansicolortags.svg)](https://pypi.python.org/pypi/ansicolortags/) -->


### Welcome / *Hûn bi xêr hatin* / بە خێر بێن! 🙂


Kurdish Language Processing Toolkit--KLPT is a [natural language processing](https://en.wikipedia.org/wiki/Natural_language_processing) (NLP) toolkit in Python for the [Kurdish language](https://en.wikipedia.org/wiki/Kurdish_languages). The current version comes with four core modules, namely `preprocess`, `stem`, `transliterate` and `tokenize` and addresses basic language processing tasks such as text preprocessing, stemming, tokenization, spell-checking and morphological analysis for the [Sorani](https://en.wikipedia.org/wiki/Sorani) and the [Kurmanji](https://en.wikipedia.org/wiki/Kurmanji) dialects of Kurdish.


## Install KLPT

<!--For detailed installation instructions, see the [documentation]().-->

- **Operating system**: macOS / OS X · Linux · Windows (Cygwin, MinGW, Visual
  Studio)
- **Python version**: Python 3.5+ 
- **Package managers**: [pip](https://pypi.org/project/klpt/)

[pip]: https://pypi.org/project/spacy/
[conda]: https://anaconda.org/conda-forge/spacy

### pip

Using pip, KLPT releases are available as source packages and binary wheels. Please make sure that a compatible Python version is installed:

```bash
pip install klpt
```

All the data files including lexicons and morphological rules are also installed with the package. 

Although KLPT is not dependent on any NLP toolkit, there is one important requirement, particularly for the `stem` module. That is [`cyhunspell`](https://pypi.org/project/cyhunspell/) which should be installed with a version >= 2.0.1.

### About this version

Please note that KLPT is under development and some of the functionalities will appear in the future versions. You can find out regarding the progress of each task at the [Projects](https://github.com/sinaahmadi/KLPT/projects) section. In the current version, the following tasks are included:

<table>
<thead>
  <tr>
    <th>Modules<br></th>
    <th>Tasks</th>
    <th>Sorani (ckb)</th>
    <th>Kurmanji (kmr)</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td rowspan="3"><code>preprocess</code></td>
    <td>normalization</td>
    <td>&#10003; (v0.1.0)</td>
    <td>&#10003; (v0.1.0)</td>
  </tr>
  <tr>
    <td>standardization</td>
    <td>&#10003; (v0.1.0)</td>
    <td>&#10003; (v0.1.0)</td>
  </tr>
  <tr>
    <td>unification of numerals</td>
    <td>&#10003; (v0.1.0)</td>
    <td>&#10003; (v0.1.0)</td>
  </tr>
  <tr>
    <td rowspan="3"><code>tokenize</code></td>
    <td>word tokenization<br></td>
    <td>&#10003; (v0.1.0)</td>
    <td>&#10003; (v0.1.0)</td>
  </tr>
  <tr>
    <td>MWE tokenization<br></td>
    <td>&#10003; (v0.1.0)</td>
    <td>&#10003; (v0.1.0)</td>
  </tr>
  <tr>
    <td>sentence tokenization</td>
    <td>&#10003; (v0.1.0)</td>
    <td>&#10003; (v0.1.0)</td>
  </tr>
  <tr>
    <td rowspan="4"><code>transliterate</code></td>
    <td>Arabic to Latin</td>
    <td>&#10003; (v0.1.0)</td>
    <td>&#10003; (v0.1.0)</td>
  </tr>
  <tr>
    <td>Latin to Arabic</td>
    <td>&#10003; (v0.1.0)</td>
    <td>&#10003; (v0.1.0)</td>
  </tr>
  <tr>
    <td>Detection of u/w and î/y</td>
    <td>&#10003; (v0.1.0)</td>
    <td>&#10003; (v0.1.0)</td>
  </tr>
  <tr>
    <td>Detection of Bizroke ( <i>i</i> )</td>
    <td>&#x2717;</td>
    <td>&#x2717;</td>
  </tr>
  <tr>
    <td rowspan="5"><code>stem</code></td>
    <td>morphological analysis</td>
    <td>&#10003; (v0.1.0)</td>
    <td>&#10003; (v0.1.1) 🆕</td>
  </tr>
  <tr>
    <td>morphological generation</td>
    <td>&#10003; (v0.1.0)</td>
    <td>&#x2717;</td>
  </tr>
  <tr>
    <td>stemming</td>
    <td>&#x2717;</td>
    <td>&#x2717;</td>
  </tr>
  <tr>
    <td>lemmatization</td>
    <td>&#x2717;</td>
    <td>&#x2717;</td>
  </tr>
  <tr>
    <td>spell error detection and correction</td>
    <td>&#10003; (v0.1.0)</td>
    <td>&#x2717;</td>
  </tr>
</tbody>
</table>


## Basic usage

Once the package is installed, you can import the toolkit as follows:

```python
import klpt
```

In the following, a few examples are provided to work with various modules. Almost all the classes have three arguments in common:

- `dialect`: the name of the dialect as `Sorani` or `Kurmanji` (ISO 639-3 code will be also added)
- `script`: the script of your input text as "Arabic" or "Latin"
- `numeral`: the type of the numerals as
	- Arabic [١٢٣٤٥٦٧٨٩٠]
	- Farsi [۱۲۳۴۵۶۷۸۹۰]
	- Latin [1234567890]

### Preprocess

This module deals with normalizing scripts and orthographies by using writing conventions based on dialects and scripts. The goal is not to correct the orthography but to normalize the text in terms of the encoding and common writing rules. The input encoding should be in UTF-8 only. To this end, three functions are provided as follows:

- `normalize`: deals with different encodings and unifies characters based on dialects and scripts
- `standardize`: given a normalized text, it returns standardized text based on the Kurdish orthographies following recommendations for [Kurmanji](https://books.google.ie/books?id=Z7lDnwEACAAJ) and [Sorani](http://yageyziman.com/Renusi_Kurdi.htm)
- `unify_numerals`: conversion of the various types of numerals used in Kurdish texts

It is recommended that the output of this module be used as the input of subsequent tasks in an NLP pipeline.

```python
>>> from klpt.preprocess import Preprocess

>>> preprocessor_ckb = Preprocess("Sorani", "Arabic", numeral="Latin")
>>> preprocessor_ckb.normalize("لە ســـاڵەکانی ١٩٥٠دا")
'لە ساڵەکانی 1950دا'
>>> preprocessor_ckb.standardize("راستە لەو ووڵاتەدا")
'ڕاستە لەو وڵاتەدا'
>>> preprocessor_ckb.unify_numerals("٢٠٢٠")
'2020'

>>> preprocessor_kmr = Preprocess("Kurmanji", "Latin")
>>> preprocessor_kmr.standardize("di sala 2018-an")
'di sala 2018an'
>>> preprocessor_kmr.standardize("hêviya")
'hêvîya'
```

### Tokenization

This module focuses on the tokenization of both Kurmanji and Sorani dialects of Kurdish with the following functions:

- `word_tokenize`: tokenization of texts into tokens (both [multi-word expressions](https://aclweb.org/aclwiki/Multiword_Expressions) and single-word tokens).
- `mwe_tokenize`: tokenization of texts by only taking compound forms into account
- `sent_tokenize`: tokenization of texts into sentences

The module is based on the [Kurdish tokenization project](https://github.com/sinaahmadi/KurdishTokenization).

```python
>>> from klpt.tokenize import Tokenize

>>> tokenizer = Tokenize("Kurmanji", "Latin")
>>> tokenizer.word_tokenize("ji bo fortê xwe avêtin")
['▁ji▁', 'bo', '▁▁fortê‒xwe‒avêtin▁▁']
>>> tokenizer.mwe_tokenize("bi serokê hukûmeta herêma Kurdistanê Prof. Salih re saz kir.")
'bi serokê hukûmeta herêma Kurdistanê Prof . Salih re saz kir .'

>>> tokenizer_ckb = Tokenize("Sorani", "Arabic")
>>> tokenizer_ckb.word("بە هەموو هەمووانەوە ڕێک کەوتن")
['▁بە▁', '▁هەموو▁', 'هەمووانەوە', '▁▁ڕێک‒کەوتن▁▁']
```

### Transliteration

This module aims at transliterating one script of Kurdish into another one. Currently, only the Latin-based and the Arabic-based scripts of Sorani and Kurmanji are supported. The main function in this module is `transliterate()` which also takes care of detecting the correct form of double-usage graphemes, namely و ↔ w/u and ی ↔ î/y. In some specific occasions, it can also predict the placement of the missing *i* (also known as *Bizroke/بزرۆکە*).

The module is based on the [Kurdish transliteration project](https://github.com/sinaahmadi/wergor).

```python
>>> from klpt.transliterate import Transliterate
>>> transliterate = Transliterate("Kurmanji", "Latin", target_script="Arabic")
>>> transliterate.transliterate("rojhilata navîn")
'رۆژهلاتا ناڤین'

>>> transliterate_ckb = Transliterate("Sorani", "Arabic", target_script="Latin")
>>> transliterate_ckb.transliterate("لە وڵاتەکانی دیکەدا")
'le wiłatekanî dîkeda'
```

### Stem

The Stem module deals with various tasks, mainly through the following functions:
- `check_spelling`: spell error detection
- `correct_spelling`: spell error correction
- `analyze`: morphological analysis

Please note that only Sorani is supported in this version in this module. The module is based on the [Kurdish Hunspell project](https://github.com/sinaahmadi/KurdishHunspell).

```python
>>> from klpt.stem import Stem
>>> stemmer = Stem("Sorani", "Arabic")
>>> stemmer.check_spelling("سوتاندبووت")
False
>>> stemmer.correct_spelling("سوتاندبووت")
(False, ['ستاندبووت', 'سووتاندبووت', 'سووڕاندبووت', 'ڕووتاندبووت', 'فەوتاندبووت', 'بووژاندبووت'])
>>> stemmer.analyze("دیتبامن")
[{'pos': 'verb', 'description': 'past_stem_transitive_active', 'base': 'دیت', 'terminal_suffix': 'بامن'}]
```

📖 **Please note that a more complete documentation of the toolkit will be available soon.**

## Become a sponsor 

Please consider donating to the project. Data annotation and resource creation requires tremendous amount of time and linguistic expertise. Even a trivial donation will make a difference. You can do so by [becoming a sponsor](https://github.com/sponsors/sinaahmadi) to accompany me in this journey and help the Kurdish language have a better place within other natural languages on the Web. Depending on your support,

- You can be an official sponsor
- You will get a GitHub sponsor badge on your profile
- If you have any questions, I will focus on it
- If you want, I will add your name or company logo on the front page of your preferred project
- Your contribution will be acknowledged in one of my future papers in a field of your choice

**Number of sponsors**: ![Open Collective sponsors](https://img.shields.io/opencollective/sponsors/s) (You, be the first one! 🙂)



## Contribute

Are you interested in this project? Each task is addressed individually. Please check the following repositories to find which one you are more interested in:

- [Kurdish tokenization](https://github.com/sinaahmadi/KurdishTokenization)
- [Kurdish Hunspell](https://github.com/sinaahmadi/KurdishHunspell)
- [Kurdish transliteration](https://github.com/sinaahmadi/wergor)

In addition, our main objective is to extend the current toolkit to include more tasks, particularly part-of-speech tagging, named-entity recognition and syntactic analysis. Further instructions are provided at [https://sinaahmadi.github.io/klpt/about/contributing/](https://sinaahmadi.github.io/klpt/about/contributing/). You can also join us on [Gitter](https://gitter.im/KurdishNLP/community).

Don't forget, **open-source is fun!** 😊

#### Thanks to all the following contributors for their valuable contributions!
[![](https://sourcerer.io/fame/sinaahmadi/sinaahmadi/klpt/images/0)](https://sourcerer.io/fame/sinaahmadi/sinaahmadi/klpt/links/0)[![](https://sourcerer.io/fame/sinaahmadi/sinaahmadi/klpt/images/1)](https://sourcerer.io/fame/sinaahmadi/sinaahmadi/klpt/links/1)[![](https://sourcerer.io/fame/sinaahmadi/sinaahmadi/klpt/images/2)](https://sourcerer.io/fame/sinaahmadi/sinaahmadi/klpt/links/2)[![](https://sourcerer.io/fame/sinaahmadi/sinaahmadi/klpt/images/3)](https://sourcerer.io/fame/sinaahmadi/sinaahmadi/klpt/links/3)[![](https://sourcerer.io/fame/sinaahmadi/sinaahmadi/klpt/images/4)](https://sourcerer.io/fame/sinaahmadi/sinaahmadi/klpt/links/4)[![](https://sourcerer.io/fame/sinaahmadi/sinaahmadi/klpt/images/5)](https://sourcerer.io/fame/sinaahmadi/sinaahmadi/klpt/links/5)[![](https://sourcerer.io/fame/sinaahmadi/sinaahmadi/klpt/images/6)](https://sourcerer.io/fame/sinaahmadi/sinaahmadi/klpt/links/6)[![](https://sourcerer.io/fame/sinaahmadi/sinaahmadi/klpt/images/7)](https://sourcerer.io/fame/sinaahmadi/sinaahmadi/klpt/links/7)

## Requirements
- Python >=3.6
- [`cyhunspell`](https://pypi.org/project/cyhunspell/) >= 2.0.1

## Cite this paper
Please consider citing [this paper](https://sinaahmadi.github.io/docs/articles/ahmadi2020klpt.pdf), if you use any part of the data or the tool ([`bib` file](https://sinaahmadi.github.io/bibliography/ahmadi2020klpt.txt)):

	@inproceedings{ahmadi2020klpt,
	    title = "{KLPT--Kurdish Language Processing Toolkit}",
	    author = "Ahmadi, Sina",
	    booktitle = "Proceedings of the second Workshop for {NLP} Open Source Software ({NLP}-{OSS})",
	    month = nov,
	    year = "2020",
	    publisher = "Association for Computational Linguistics"
	}


## License 
<a rel="license" href="http://creativecommons.org/licenses/by-sa/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-sa/4.0/88x31.png" /></a><br /><span xmlns:dct="http://purl.org/dc/terms/" property="dct:title">Kurdish Language Processing Toolkit</span> by <a xmlns:cc="http://creativecommons.org/ns#" href="https://github.com/sinaahmadi/klpt" property="cc:attributionName" rel="cc:attributionURL">Sina Ahmadi</a> is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by-sa/4.0/">Creative Commons Attribution-ShareAlike 4.0 International License</a> which means:

- **You are free to share**, copy and redistribute the material in any medium or format and also adapt, remix, transform, and build upon the material
for any purpose, **even commercially**. 
- **You must give appropriate credit**, provide a link to the license, and indicate if changes were made. You may do so in any reasonable manner, but not in any way that suggests the licensor endorses you or your use.
- If you remix, transform, or build upon the material, **you must distribute your contributions under the same license as the original**. 



