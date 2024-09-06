
## rime-bepemefeve

以注音字母記錄的「老國音」音碼表，通過RIME輸入法引擎支援多種漢字輸入方案。

以1926年的第三十八版《校改國音字典》爲主要參考，兼收《學生字典》（陸爾奎、方毅，1915）與《國音新詩韻》（趙元任，1922），每條字音均附有出處。

此字表中注音字母使用聲調符號表示聲調（不使用四聲點法），在字頭加上`·`表示輕音。可能同時寫出原聲調，例如「子」`·ㄗˇ`

### 基於注音字母的輸入方案

#### 類大千式
TODO：未設計

聲調符號全部移到鍵盤右上角

輕音符號依照標準寫法標在字頭

配方文件名：~~`bepemefeve_5jup.schema.yaml`~~

#### 類許氏鍵盤
TODO：未設計
配方文件名：~~`bepemefeve_hsus.schema.yaml`~~

#### 雙拼
TODO：未設計
配方文件名：~~`bepemefeve_double.schema.yaml`~~

#### 三拼
TODO：未設計
配方文件名：~~`bepemefeve_triple.schema.yaml`~~

### 羅馬拼音形式的輸入方案
#### 國語羅馬字（G.R.／Gwoyeu Romatzyh）
__別名：國音字母第二式、譯音符號__

中國史上第一套官定羅馬拼音標準，主要爲新國音而設計，亦可用於拼寫老國音。

需要注意的是，韻母ㄝ`è`在老國音中可以與聲母相拼，因此需要單獨編碼。G.R.用於拼寫老國音時，`X`是唯一不用的基本字母，因此此輸入方案以`X`鍵表示`è`（但在非入聲字中亦可用`E`鍵）
- `z`字母在國羅中僅用於拼寫`tz`聲母，因此`tz`可簡作`z`
- `c`字母在國羅中僅用於拼寫`ch`聲母，因此`ch`可簡作`c`

配方文件名：`bepemefeve_gr.schema.yaml`

僅用G.R.的基本形式（不帶聲調）\
配方文件名：`bepemefeve_gr_atonal.schema.yaml`

除入聲外不帶聲調的基本形式（入聲可視作一種韻尾）\
配方文件名：~~`bepemefeve_gr_ruqsheng.schema.yaml`~~

#### 威妥瑪拼音
__別名：Wade-Giles (W.G.)、威翟式拼音、韋式拼音__

近代最流行的官話拼音系統，見於一些早期的老國音字典。

TODO

配方文件名：~~`bepemefeve_wg.schema.yaml`~~


### 當代原創老國音拼音方案
《漢語拼音方案》是當代最通行的拼音方案，但《漢語拼音》無法拼寫老國音（未有定義老國音需要的`ㄫ`、`ㄬ`兩個聲母，入聲，`ㄗㄧ`、`ㄘㄧ`、`ㄙㄧ`的拼法）。因此，當代的老國音學習者爲了方便錄入或拼讀，又在漢語拼音的基礎上，提出了多種用於老國音的拼音系統：

#### 勝爲士：老國音趙音拼音（趙拼）
詳見 [維基學院：老國音趙音拼音方案](https://zh.wikiversity.org/wiki/原創老國音拼音方案/老國音趙音拼音方案)

配方文件名：`bepemefeve_zhauping.schema.yaml`

#### iacobvs：iac轉寫
##### 用於輸入法的簡寫形式
詳見 [知乎：iac老國音輸入方案](https://zhuanlan.zhihu.com/p/21674298)

配方文件名：`bepemefeve_iac_im.schema.yaml`

##### 與注音符號一一對應的形式
詳見 [維基學院：iac轉寫](https://zh.wikiversity.org/wiki/原創老國音拼音方案/iac轉寫)

配方文件名：`bepemefeve_iac_lt.schema.yaml`

#### 綺檐淸露：國音用漢語拼音（混合式拼音）
TODO
詳見 [維基學院：國音用漢語拼音](https://zh.wikiversity.org/wiki/原創老國音拼音方案/國音用漢語拼音)

配方文件名：~~`bepemefeve_huenhoshi.schema.yaml`~~

#### 水光水：胡拼
TODO

配方文件名：~~`bepemefeve_huping.schema.yaml`~~
