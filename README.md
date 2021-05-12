# Incremental Search Traffic Dataset

The Incremental Search Traffic Dataset (**ISTD**) is a collection of 32.4k traffic samples in `pcap` format. Each sample contains network traffic captured when an English or Chinese query is typed into the search box of an incremental search website.

* Incremental search websites include Google, Tmall, Facebook, Baidu, Yahoo, Wikipedia, Csdn, Twitch, and Bing (9 in total).
* English and Chinese queries are randomly selected from the [AOL search dataset](https://jeffhuang.com/search_query_logs.html) and the [THU Open Chinese Lexicon](http://thuocl.thunlp.org/) (THUOCL), respectively.
* Each language contains 1.8k queries with lengths ranging from 10 to 40 characters (60 queries per length).
* User's typing rhythm is simulated using the timing model trained on the [136M keystroke dataset](https://userinterfaces.aalto.fi/136Mkeystrokes/).

The traffic capture process ran from September 23 to October 4, 2020, lasted about 12 days.

***Note:*** This dataset is for NON-COMMERCIAL RESEARCH USE ONLY!


## Getting the dataset

The dataset is available here:

* [ISTD](https://mega.nz/file/0I4SQCjJ#Wzqp1v7XvnBzhn3jcCC2hcQdcT3k6jzzOmxBvAhOnTc) (10.15 GB, SHA1: C3089F76E952A8218881B6D8A11E214CF091604E)


## Content

ISTD consists of the following two parts:

* Lists of randomly selected queries from the AOL and THUOCL query sets.

```
- query/
  - AOL/
    - l[xx]_n60.csv          list of 60 English queries with a length of [xx] characters.
  - THUOCL/
    - l[xx]_n60.csv          list of 60 Chinese queries with a Pinyin syllable length of [xx] characters.
```

* Traffic samples captured when typing queries in incremental search websites.

```
- pcap/[yy]/
  - AOL/
  - THUOCL/
    - l[xx]_n60/[zz].pcap    traffic sample captured while typing query [zz] in website [yy].
```


## Related repository

* [QAIS](https://github.com/incremental-search/qais): the data collection tool that captures network traffic while an English or Chinese query is typed into an incremental search website.
