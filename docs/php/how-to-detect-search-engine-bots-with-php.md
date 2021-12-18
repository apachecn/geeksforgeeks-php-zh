# 如何用 PHP 检测搜索引擎机器人？

> 原文:[https://www . geesforgeks . org/how-detect-search-engine-bots-with-PHP/](https://www.geeksforgeeks.org/how-to-detect-search-engine-bots-with-php/)

搜索引擎机器人(有时称为蜘蛛或爬虫)是抓取网页的计算机程序(机器人)。换句话说，他们访问网页，找到更多网页的链接，然后访问它们。通常，他们会映射找到的内容，以便以后用于搜索目的(索引)。他们还帮助开发者诊断他们网站的问题。
众所周知，web 上 JavaScript 的使用量不断增长，对用户来说肯定是有好处的，但是渲染 JS 对搜索引擎来说是一个挑战。如果你的网站没有被僵尸工具正确处理，或者你的内容经常变化，你应该动态地呈现你的页面，并向爬虫提供呈现的 HTML，而不是 JavaScript 代码。因此，为了做到这一点，您必须知道请求是由真实用户发出的，还是由爬虫(搜索引擎机器人)发出的。
PHP 没有任何检测搜索引擎僵尸工具的内置功能。但是，以下功能可用于此目的。

**示例:**

```
<?php

function is_bot($system) {

    // Bots list 
    $bot_list = array(
        'Googlebot', 'Baiduspider', 'ia_archiver',
        'R6_FeedFetcher', 'NetcraftSurveyAgent',
        'Sogou web spider', 'bingbot', 'Yahoo! Slurp',
        'facebookexternalhit', 'PrintfulBot', 'msnbot',
        'Twitterbot', 'UnwindFetchor', 'urlresolver'
    );

    // If it is search engine bot
    // returns true, else returns false
    foreach($bot_list as $bl) {
        if( stripos( $system, $bl ) !== false )
            return true;
    }

    return false;
}

echo is_bot('Googlebot');

?>
```

**输出:**

```
1
```

这个函数将 PHP 用户代理与来自搜索引擎、180 多个机器人、蜘蛛和爬虫的常见蜘蛛列表进行比较。

当给出“Googlebot”作为输入时，该函数返回 true(1)，因为提供的输入是搜索引擎 bot 的名称。