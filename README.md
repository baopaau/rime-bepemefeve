
# rime-bepemefeve

「老國音」注音字表兼RIME輸入方案整合

以《校改國音字典》《國音新詩韻》《國語留聲片課本》爲準，
其餘字音推導自《學生字典》（校改前）《康熙字典》（包含《廣韻》《集韻》等韻書）

#### 注音字音表格式

以**聲調符號**表示聲調，不使用四聲點法

##### 具體字符

 | 聲調 | 符號 | 碼位 |
 | :- | :- | :- |
 | 陰平聲 | `ˉ` | `U+02C9 MODIFIER LETTER MACRON` |
 | 陽平聲 | `ˊ` | `U+02CA MODIFIER LETTER ACUTE ACCENT` |
 | 上聲 | `ˇ` | `U+02C7 CARON` |
 | 去聲 | `ˋ` | `U+02CB MODIFIER LETTER GRAVE ACCENT` |
 | 入聲 | `˙` | `U+02D9 DOT ABOVE` |
 | 輕音/無固定聲調 | `·` | `U+00B7 MIDDLE DOT` |

- 陰平聲`ˉ`實際上不標出
- 輕音符號`·`需要加在字頭，而非加在字尾
- 輕音符號使用中點`·`表示，而不使用目前通行的上點`˙`，上點`˙`僅表示入聲
- 輕音和聲調可能同時標出，例如：子 `·ㄗˇ`

[「老國音」字音表 `bepemefeve.dict.yaml`](bepemefeve.dict.yaml)\
[「老國音」字音表（國語羅馬字版） `guoqlo.dict.yaml`](guoqlo.dict.yaml)\
[「老國音」注音／各式羅馬拼音對照](bepemefeve_syllables.md)


### 目前支援的輸入方案
- [國語羅馬字](#gr)
  - `./bepemefeve_gr.schema.yaml`
  - `./guoqlo.schema.yaml`
- [威翟式拼音（Wade–Giles）](#wg)
  - `./bepemefeve_wg.schema.yaml`
- [國語注音符號第二式](#mps2)
  - `./bepemefeve_mps2.schema.yaml`
- [勝爲士：趙音拼音](#zhauping)
  - `./bepemefeve_zhauping.schema.yaml`
- [iacobvs：iac轉寫](#iac)
  - `./bepemefeve_iac_im.schema.yaml`
  - `./bepemefeve_iac_lt.schema.yaml`
- [綺檐淸露：國音用漢語拼音](#tsinglou)
  - `./bepemefeve_tsinglou.schema.yaml`
- [Ruenn式國音拼音方案](#ruenn)
  - `./bepemefeve_tsinglou.schema.yaml`
- [注音 大千兼容式](#stdext)
  -  `./bepemefeve_stdext.schema.yaml`
- [注音 順位式](#shuennwey)
  -  `./bepemefeve_shuennwey.schema.yaml`
- [注音 倚天兼容式](#eten26ext)
  -  `./bepemefeve_eten26ext.schema.yaml`
- [注音 許氏鍵盤改](#hsukeymod)
  -  `./bepemefeve_hsukeymod.schema.yaml`



## 羅馬拼音形式的輸入方案

<a name="gr"></a>
### 國語羅馬字（Gwoyeu Romatzyh）
*別名：國音字母第二式 (1928~)、譯音符號 (1940~)*

輸入法說明：
- 以`x`鍵 或 大寫`E`鍵 輸入`è`（ㄝ）
- 以`q`鍵 輸入 `·`（輕聲）
- `tz`可簡作`z`
  - 因爲`z`字母在G.R.中僅用於拼寫`tz`聲母
  - 上屏爲`ᵗz`
- `ch`可簡作`c`
  - 因爲`c`字母在G.R.中僅用於拼寫`ch`聲母
  - 上屏爲`cʰ`

配方位置：`./bepemefeve_gr.schema.yaml`\
碼表位置：`./bepemefeve.dict.yaml`

**獨立碼表與輸入方案：**\
配方位置：`./guoqlo.schema.yaml`\
碼表位置：`./guoqlo.dict.yaml`


<a name="wg"></a>
### 威翟式拼音（Wade–Giles）
*別名：威妥瑪拼音、韋翟式拼音、韋傑士羅馬拼音、韋氏拼音*

輸入法說明：
- `ㄬ`母以 `ʻn` 表示
- 字母 `ü` 需要以 ⇧`U` 鍵入；其餘的 `ê`、`ŭ` 用基本字母代替，不會混淆
- 符號 `ʻ` 以 `'` (或 `q` 或 `x`) 鍵入，不可省略
- 隔音符用 `-`
- 以數字鍵`6`、`7`、`8`、`9`、`0`輸入聲調：`¹`陰、`²`陽、`³`上、`⁴`去、`⁵`入

配方位置：`./bepemefeve_wg.schema.yaml`\
碼表位置：`./bepemefeve.dict.yaml`


<a name="mps2"></a>
### 國語注音符號第二式
*英文：Mandarin Phonetic Symbols II (MPS II)*

拼音方案詳見 [國語注音符號第二式 介紹](https://language.moe.gov.tw/001/Upload/files/site_content/M0001/er/cmain.htm)

注音二式「以原先制訂公布之譯音符號聲母韻母基本拼法為準，略作修訂」，文件中未提及的「ㄪ」「ㄫ」「ㄬ」三母，直接沿用國語羅馬字的`v`、`ng`、`gn`即可

輸入法說明：
- 以`x`鍵 或 大寫`E`鍵 輸入`ê`（ㄝ）
- `ch`可簡作`c`
  - 因爲`c`字母在注音二式中僅用於拼寫`ch`聲母
  - 上屏爲`cʰ`
- 分別以數字鍵`6`、`7`、`8`、`9`、`0`輸入聲調：`ˉ`陰、`ˊ`陽、`ˇ`上、`ˋ`去、`˙`入
- `q`鍵 表示輕聲

配方位置：`./bepemefeve_mps2.schema.yaml`\
碼表位置：`./bepemefeve.dict.yaml`


<a name="zhauping"></a>

### 勝爲士：趙音拼音（趙拼）
*全稱：老國音趙音拼音*

拼音方案詳見 [維基學院：老國音趙音拼音方案](https://zh.wikiversity.org/wiki/原創老國音拼音方案/老國音趙音拼音方案)

輸入法說明：
- 分別以數字鍵`6`、`7`、`8`、`9`、`0`輸入聲調：`1`陰、`2`陽、`3`上、`4`去、`5`入


配方位置：`./bepemefeve_zhauping.schema.yaml`\
碼表位置：`./bepemefeve.dict.yaml`

<a name="iac"></a>

### iacobvs：iac轉寫
拼音方案詳見：
* [維基學院：iac轉寫](https://zh.wikiversity.org/wiki/原創老國音拼音方案/iac轉寫)
* [知乎：iac老國音輸入方案](https://zhuanlan.zhihu.com/p/21674298)

輸入法說明：
- 分別以數字鍵`7`、`8`、`9`、`0`輸入聲調：`1`陰、`2`陽、`3`上、`4`去
- 入聲用`-q`

特用於輸入法的簡寫形式\
配方位置：`./bepemefeve_iac_im.schema.yaml`\
碼表位置：`./bepemefeve.dict.yaml`

與注音符號一一對應的形式\
配方位置：`./bepemefeve_iac_lt.schema.yaml`\
碼表位置：`./bepemefeve.dict.yaml`

<a name="tsinglou"></a>

### 綺檐淸露：國音用漢語拼音
*別名：混合式拼音*

拼音方案詳見 [維基學院：國音用漢語拼音](https://zh.wikiversity.org/wiki/原創老國音拼音方案/國音用漢語拼音)

輸入法說明：
- 分別以數字鍵`6`、`7`、`8`、`9`、`0`輸入聲調：`ˉ`陰、`ˊ`陽、`ˇ`上、`ˋ`去、`˙`入
- 以 `+`鍵（⇧`=`）輸入 符號`+`（表示輕音）

配方位置：`./bepemefeve_tsinglou.schema.yaml`\
碼表位置：`./bepemefeve.dict.yaml`

<a name="ruenn"></a>

### Ruenn式國音拼音方案

提出者：[Ruenn_L（哔哩哔哩）](https://space.bilibili.com/23285950)

根據漢語拼音方案修改定制的拼音方案：
- ㄫ、ㄬ 定爲 `ng`、`nj`
- 入聲以 `ˆ` 表示
- ㄝ 定爲 `ee`，不用漢語拼音的 `ê`
- ㄗㄧ、ㄘㄧ、ㄙㄧ 定爲 `zii` `cii` `sii`

輸入法說明：
- 分別以數字鍵`6`、`7`、`8`、`9`、`0`輸入聲調：`ˉ`陰、`ˊ`陽、`ˇ`上、`ˋ`去、`ˆ`入
- 以 大寫`U`鍵 輸入 `ü`

配方位置：`./bepemefeve_ruenn.schema.yaml`\
碼表位置：`./bepemefeve.dict.yaml`


## 基於注音字母的輸入方案

「老國音」需要使用「ㄪ」「ㄫ」「ㄬ」這三個在1932年後被廢棄的聲母，而且多了一個入聲聲調，
現有的注音鍵盤並不能滿足老國音的錄入需要，因此有了以下的替代排列：

<a name="stdext"></a>
### 大千兼容式
不增加按鍵，兼容現有大千式軟鍵盤：
- 合併按鍵：ㄪ/ㄫ/ㄬ <-> ㄒ/ㄑ/ㄖ <-> `V`/`F`/`B`鍵
- 輕聲鍵（數字鍵7）同時兼任入聲鍵：標在字頭爲輕音，標在字尾爲入聲

![](assets/keyboard-layout-bepemefeve-stdext.png)\
*「大千兼容式」鍵盤排列（高亮的按鍵不同於標準「大千式」）*

配方位置：`./bepemefeve_stdext.schema.yaml`\
碼表位置：`./bepemefeve.dict.yaml`


<a name="shuennwey"></a>
### 順位式
鍵盤根據1920年的舊注音字母表順序（ㄪ、ㄦ兩母除外）重新排列：

    1QAZ ㄅㄆㄇㄈ
    2WSX ㄉㄊㄋㄌ
    3EDC ㄍㄎㄫㄏ
    4RFV ㄐㄑㄬㄒ
    5TGB ㄓㄔㄕㄖ
    6YHN ㄗㄘㄙㄦ /* 「ㄦ」跟「ㄖ」在各種拼音方案中經常會共用同字母R，所以放在相鄰位置 */
    7UJM ㄧㄨㄩㄪ /* 「ㄪ」雖然不算介母，但只與「ㄟ」相拼，與「ㄨ」有關，所以放在同一列 */
    8IK, ㄚㄛㄜㄝ
    9OL. ㄞㄟㄠㄡ
    0P;/ ㄢㄣㄤㄥ
    /* ㄪ、ㄦ兩母不依照字母表順序排列 */

    '[-=] 陰陽上去入 /* 按鍵位置如「四聲點法」*/
    /* 陰平聲與輕音共用按鍵`'`，標在字尾爲陰平聲，標在字頭爲輕音 */

![](assets/keyboard-layout-bepemefeve-shuennwey.png)\
*「順位式」鍵盤排列（高亮的按鍵不同於標準「大千式」）*

不同於通常的注音輸入法，本輸入方案以【空格鍵】或 `QWERTYUIOP` 選詞，以`]`和`\`鍵換頁，
而【回車鍵】用於直接輸入拉丁字母、數字等ASCII字符（毋須切換模式）


配方位置：`./bepemefeve_shuennwey.schema.yaml`\
碼表位置：`./bepemefeve.dict.yaml`


<a name="eten26ext"></a>
### 倚天兼容式
基於倚天26鍵修改，在不增加任何按鍵、盡量不影響現有操作習慣的前提下支援老國音使用的舊式注音符號

* ㄪ - ㄔ - Y
* ㄫ - ㄜ - R
* ㄬ - ㄞ - I
* 入聲 - ㄙ - S

![](assets/keyboard-layout-bepemefeve-eten26ext.png)\
*「倚天兼容式」鍵盤排列（高亮的按鍵不同於標準「倚天26鍵」）*

配方位置：`./bepemefeve_eten26ext.schema.yaml`\
碼表位置：`./bepemefeve.dict.yaml`


<a name="hsukeymod"></a>
### 許氏鍵盤改
基於[許氏鍵盤](https://web.archive.org/web/20070214130835/http://www.iis.sinica.edu.tw/IASL/products/going5/chap-ad.html)修改，在盡量不影響現有操作習慣的前提下支援老國音使用的舊式注音符號

* `U` ㄪ ㄪ通常羅馬化V，而V與U之間關係接近
* `Q` ㄫ Q的常見發音/k/的位置同ㄫ。在趙元任的羅馬字設計中，ㄫ亦常常轉寫成Q
* `R` ㄬ ㄬ與ㄖ之間關係接近

用原版許氏鍵盤輸入老國音，ㄓㄝ、ㄔㄝ、ㄕㄝ 會與 ㄐㄧ、ㄑㄧ、ㄒㄧ相混，
因此**ㄧ和ㄝ不再共用E鍵。ㄝ會移到ㄫ的位置，共用Q鍵。**

![](assets/keyboard-layout-bepemefeve-hsukeymod.png)\
*「許氏鍵盤改」鍵盤排列（高亮的按鍵不同於標準「許氏鍵盤」）*

配方位置：`./bepemefeve_hsukeymod.schema.yaml`\
碼表位置：`./bepemefeve.dict.yaml`

## 鳴謝

### 字音/詞庫數據來源
- [電子化《校改國音字典》](https://zhuanlan.zhihu.com/p/22056043)
  - [iacobvstsok（耶箍步）](https://www.zhihu.com/people/0ff167dfc98216d1064c3abd28d3d999)
  - [李鶱棹](https://www.zhihu.com/people/3de247f4d4bb222ccfbfb48a76b36aea)
  - [曹潔萍](https://www.zhihu.com/people/b7e5d56f3544d1510d2d247a6d5f93b1)
  - [王子軒](https://www.zhihu.com/people/7798ab97b6c988c0982bcbde108141cf)
  - [馬從之](https://www.zhihu.com/people/7798ab97b6c988c0982bcbde108141cf)
- [電子化《學生字典》](http://fgwang.blogspot.com/2021/07/blog-post_13.html)
  - [電脳瓦崗寨](http://wagang.econ.hc.keio.ac.jp/)
  - [漢字データベース](http://kanji-database.sourceforge.net/dict/xszd)
  - [WFG](http://fgwang.blogspot.com)
- [維基學院：整合《國音新詩韻》字彙](https://zh.wikiversity.org/wiki/整合老國音熟字彙)
- [維基學院：老國音審音字庫](https://zh.wikiversity.org/wiki/Category:老國音審音)
- [校改國音字典整理會](https://zhuanlan.zhihu.com/Jiaoq-gais-guoh-iny-ziq-dians)
  - [勝爲士](https://www.zhihu.com/people/ff123b1d3fcdab2a70675df1245a9eeb)
  - [HANCVS韓](https://www.zhihu.com/people/7b106d7c1f31a47d8ba6cdbcb0e11316)
- [qieyun-data](https://github.com/nk2028/tshet-uinh-data)
- [康熙字典 Kangxi Dictionary TXT](https://github.com/7468696e6b/kangxiDictText)
- [趙元任 國語留聲片課本](https://upload.wikimedia.org/wikipedia/commons/c/c0/NLC416-07jh011263-4826_%E5%9C%8B%E8%AA%9E%E7%95%99%E8%81%B2%E7%89%87%E8%AA%B2%E6%9C%AC.pdf)
- [RIME 地球拼音](https://github.com/rime/rime-terra-pinyin)

