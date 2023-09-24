# DictionaryData

高质量英语字典，包括各种单词书，小学、中学、高中、考研、考博、出国（GRE、托福等等）等等，都已经分类好了

```python
import pandas as pd
book = pd.read_csv('book.csv', sep=">")
word = pd.read_csv('word.csv', sep=">")
relation_book_word = pd.read_csv('relation_book_word.csv', sep=">")
word_translation = pd.read_csv('word_translation.csv')
```

## 文件说明

- word.csv 单词
- word_translation.csv 单词及其中文翻译
- book.csv 单词书、词汇书
- relation_book_word.csv 单词和词汇书的关系数据

## word.csv 单词

|       字段名        |  类型  | 说明       | 示例                       |
| :-----------------: | :----: | :--------- | :------------------------- |
|        vc_id        | string | 单词id     | `57067c89a172044907c6698e` |
|    vc_vocabulary    | string | 单词       | `superspecies`             |
|   vc_phonetic_uk    | string | uk英音音标 | `[su:pərsˈpi:ʃi:z]`        |
|   vc_phonetic_us    | string | us美音音标 | `[supɚsˈpiʃiz]`            |
|    vc_frequency     | float  | 词频       | `0.000000`                 |
|    vc_difficulty    |  int   | 难度       | `1`                        |
| vc_acknowledge_rate | float  | 认识率     | `0.664122`                 |

## word_translation.csv 单词及其中文翻译

|       字段名        |  类型  | 说明       | 示例            |
| :-----------------: | :----: | :--------- | :------------ |
|       word        | string | 单词          | `brain`      |
|  translation      | string | 单词的中文翻译  | `n.脑,头脑`   |


## book.csv 单词书

|       字段名       |  类型  | 说明                      | 示例                                                                                                                     |
| :----------------: | :----: | :------------------------ | :----------------------------------------------------------------------------------------------------------------------- |
|       bk_id        | string | 单词书id                  | `d645920e395fedad7bbbed0e`                                                                                               |
|    bk_parent_id    | string | 单词书父分类id（无则为0） | `6512bd43d9caa6e02c990b0a`                                                                                               |
|      bk_level      |  int   | 等级                      | `2`                                                                                                                      |
|      bk_order      | float  | 排序                      | `2.000000`                                                                                                               |
|      bk_name       | string | 书名                      | `人教版高中英语1 - 必修`                                                                                                 |
|    bk_item_num     |  int   | 单词个数                  | `315`                                                                                                                    |
| bk_direct_item_num |  int   | 单词个数                  | `315`                                                                                                                    |
|     bk_author      | string | 作者                      | `刘道义`                                                                                                                 |
|      bk_book       | string | 完整书名                  | `人教版普通高中课程标准实验教科书 英语 1 必修`                                                                           |
|     bk_comment     | string | 描述                      | `黑体：本单元重点词汇和短语；无“△”：课标词汇，要求掌握；有“△”：不要求掌握（会出现大量缩写、人名、地名和短语，请选背）。` |
|   bk_orgnization   | string | 组织                      | `人民教育出版社 课程教材研究所；英语课程教材研究开发中心`                                                                |
|    bk_publisher    | string | 出版社                    | `人民教育出版社`                                                                                                         |
|     bk_version     | string | 版本                      | `2007年1月第2版`                                                                                                         |
|      bk_flag       | string | 标记                      | `默认：152;黑体：97;前△：66`                                                                                             |


## relation_book_word.csv 单词书-单词

|   字段名   |  类型  | 说明     | 示例                       |
| :--------: | :----: | :------- | :------------------------- |
|   bv_id    | string | 关系id   | `58450c828958a37d5c10f763` |
| bv_book_id | string | 单词书id | `d645920e395fedad7bbbed0e` |
| bv_voc_id  | string | 单词id   | `57067b9ca172044907c615d7` |
|  bv_flag   | string | 分组     | `4`                        |
|   bv_tag   | string | 分组名   | `Unit 1`                   |
|  bv_order  |  int   | 排序     | `1`                        |


