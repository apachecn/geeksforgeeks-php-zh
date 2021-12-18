# CSS 和 PHP 的区别

> 原文:[https://www . geeksforgeeks . org/differences-CSS 和-php/](https://www.geeksforgeeks.org/differences-between-css-and-php/)

[**CSS**](https://www.geeksforgeeks.org/css-tutorials/) **:** CSS 代表层叠样式表，它是一种样式表语言，用于塑造将作为网页显示在浏览器中的 HTML 元素。通过使用 CSS，使用 HTML 创建的网站看起来会很有吸引力。基本上，CSS 为任何 HTML 元素提供了外壳。如果你认为 HTML 是网页的骨架，那么 CSS 就是骨架的皮肤。CSS 的互联网媒体类型(MIME 类型)是文本/CSS。

**示例**:这个示例描述了简单 CSS 的使用。CSS 已经在样式标签中使用了 HTML。

## 超文本标记语言

```
<!DOCTYPE >
<html>
    <head>
        <style>
            h1 {
                color: white;
                background-color: red;
            }
            p {
                color: blue;
            }
        </style>
    </head>
    <body>
        <h1>Geeksforgeeks</h1>

<p>A computer science portal for geeks</p>

    </body>
</html>
```

**输出:**

![](img/899bb5c8837dacbece71cbd2386a6856.png)

[**PHP**](https://www.geeksforgeeks.org/php/) **:** PHP 代表超文本预处理器。PHP 是一种服务器端脚本语言(一种基于脚本的程序)，用于开发网络应用程序。它可以嵌入到 HTML 中，适合创建动态网页和数据库应用程序。它被视为一种仁慈的语言，能够有效地与 MySQL、Oracle 和不同的数据库进行交互。PHP 的主要目标是允许 web 开发人员快速创建动态生成的页面。

**示例:**

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```
<?php 

// Here echo command is
// used to display content
echo "Welcome to GFG!"; 
?> 
```

**输出:**

```
Welcome to GFG!

```

**CSS 与 PHP 的区别:**

<figure class="table">

| **先生。否〔t1〕** | CSS | PHP |
| 1。 | CSS represents the style and appearance of fonts, colors, margins, padding, etc. | For PHP server-side programming, server-side programming will interact with the database, carry out information retrieval, storage and mail delivery, and provide the content to HTML pages for display on the screen. |
| 2。 | Developed by Hakon Wium Lie, bert bos. | It was developed in Rasmus Lerdorf. |
| 3。 | It is easy to learn. | PHP is easy to learn but not as good as CSS. |
| 4。 | No response page or website is provided. | A page or website that provides a response. |
| 5。 | Its code is static. | Its code is dynamic. |
| 6。 | Used for front-end development | Used for server-side development. |
| 7。 | Can be used in a PHP file. | It cannot be used in CSS files. |
| 8。 | Currently, the latest version of CSS3 is being developed. | Currently working on PHP7.0, which is the latest version of PHP. |
| 9。 | It is very useful in the appearance of the website. | It adds dynamic content to the website and makes it look good. |
| 10。 | The extension of CSS is. The extension of PHP is. php、. php3、. php4、. PHP 7 . |

</figure>