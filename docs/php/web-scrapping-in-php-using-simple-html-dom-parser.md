# 使用简单 HTML DOM 解析器的 PHP 网页报废

> 原文:[https://www . geesforgeks . org/web-warning-in-PHP-using-simple-html-DOM-parser/](https://www.geeksforgeeks.org/web-scrapping-in-php-using-simple-html-dom-parser/)

网页抓取是一种用于从网站中提取大量数据的技术，这些数据被提取并保存到计算机的本地文件或数据库中，或者可以用作应用编程接口。大多数网站显示的数据只能通过网络浏览器查看。它们不提供保存该数据副本以供使用的功能。因此，唯一的选择是复制和粘贴所需的选定数据，这实际上是一项非常繁琐的工作，可能需要几个小时才能完成。换句话说，网页抓取是自动化这种过程的技术，代替人工工作，网页抓取软件在几秒钟内执行相同的任务。网页抓取可以通过以选定的 DOM 组件为目标，然后处理或存储网页的 DOM 元素之间的文本来完成。为了在 PHP 中做到这一点，有一个分析整个页面并在 DOM 中查找所需元素的应用编程接口。它就是简单的超文本标记语言解析器。要了解更多关于[网页抓取](https://www.geeksforgeeks.org/introduction-to-web-scraping/)的信息，请访问本文。

可以通过点击[这个](https://sourceforge.net/projects/simplehtmldom/)链接下载。

**示例 1:** 下面给出的示例显示了这个应用编程接口的使用，在本地主机上显示谷歌搜索。

*   **HTML 代码:**

    ```php
    <!DOCTYPE html>
    <html lang="en">

    <head>
        <meta charset="UTF-8">

        <meta name="viewport" content=
            "width=device-width, initial-scale=1.0">

        <meta http-equiv="X-UA-Compatible" content="ie=edge">

        <title>Document</title>
    </head>

    <body>
        <form action="GoogleSearch.php" method="POST">
            <input type="text" name="search">

            <br><br>

            <button>
                Search
            </button>
        </form>
    </body>

    </html>
    ```

*   **PHP code:**

    ```php
    <?php

    // In case the File is in the API directory 
    include('simple_html_dom.php');

    // Extracting DOM
    $html = file_get_html(
    'http://www.google.com/search?q='.$_POST["search"]);

    // Displaying DOM
    echo $html;

    ?>
    ```

    **输出:**本地服务器上的输出为
    ![](img/7218853741bef80e17ad2a453eaa5530.png)

    **示例 2:** 这里我们将尝试访问 google 第一个搜索结果上的文本。为此，我们首先获取 DOM 组件，该组件具有向谷歌请求的查询的第一个结果。在这里，我们从 DOM 中获取具有类“kCrYT”的 span 标记，其中有所有搜索到的详细信息的列表，但是我们只需要第一个，所以循环只迭代一次。

    *   **PHP 代码:**如果你已经在谷歌搜索引擎上搜索过任何东西，这个代码可以工作。

        ```php
        <?php

        include('simple_html_dom.php');

        $html = file_get_html(
        'http://www.google.com/search?q='.$_POST["search"]);

        foreach($html->find('div.kCrYT') as $elements) {
            echo $elements->plaintext;
            break;
        }
        ?>
        ```

    *   **输出:**

        ```php
        GeeksforGeeks is a very fast-growing community among programmers
        and have a reach of around 10 million+ readers globally. Writing will
        surely enhance your knowledge of the subject as before writing any
         topic, you need to be very crisp and clear about it.
        ```