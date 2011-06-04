﻿簡介
----

利用MediaWiki 作中文互換，支援不同地方中文用字上的分別(大陸、香港、台灣及新加坡)。

```
例子：

(簡 > 繁)

面包 > 麵包 (zh-tw)
寮国 > 老撾 (zh-hk)
中国人寿 > 中國人壽 (zh-hk)
罗纳尔多 > 朗拿度 (zh-hk)

(繁 > 簡)

記憶體 > 内存 (zh-cn)
布殊 > 布什 (zh-cn)
資料庫 > 数据库(zh-cn)
```

----
### 使用方法

1. 下載 MediaWiki: http://www.mediawiki.org/wiki/MediaWiki

2. 解壓在路徑如：/var/lib/mediawiki-1.13.3

3. 下載 mediawiki-zhconverter，解壓及把 mediawiki-zhconverter.inc.php 抄到你 PHP 程序當中

4. 在你的程序中設定 MediaWiki 路徑, 及引用 mediawiki-zhconverter


        define("MEDIAWIKI_PATH", "/var/lib/mediawiki-1.6.10/");
        require_once "mediawiki-zhconverter.inc.php";


4. 作出轉換

        /*
            MediaWikiZhConverter::convert( "字詞", "轉換目標");  
            轉換目標 = zh, zh-cn, zh-tw, zh-sg, zh-hk
        */
        
        echo MediaWikiZhConverter::convert("面包", "zh-tw");
        echo MediaWikiZhConverter::convert("記憶體", "zh-cn");
        echo MediaWikiZhConverter::convert("罗纳尔多", "zh-hk");



5. 完成


----
### 支援版本

下列MediaWiki 版本已證實可以兼容本程式 (http://download.wikimedia.org/mediawiki)：

 * PHP4: 1.6.10, 1.6.11
 * PHP5: 1.12.0, 1.13.3, 1.15.4

如非必要，請使用 *PHP5* 版本。

----
### 在線演示

http://labs.xddnet.com/mediawiki-zhconverter/example/example.html


----
### 聯絡

任可問題或建意歡迎電郵至 tszming at gmail dot com  