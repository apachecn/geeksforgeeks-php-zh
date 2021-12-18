# 如何用 PHP 制作排行榜？

> 原文:[https://www . geeksforgeeks . org/如何使用-php 制作排行榜/](https://www.geeksforgeeks.org/how-to-make-a-leaderboard-using-php/)

本文的目的是制作一个简单的程序，使用 PHP 创建一个排行榜。下面是使用 PHP 的实现。本主题的前提是 [PHP](https://www.geeksforgeeks.org/php/) / [MySQL](https://www.geeksforgeeks.org/mysql-database-current_user-functions/) 和在你的电脑上安装 [Apache](https://www.apachefriends.org/index.html) 服务器。

**进场:**

**步骤 1:** 首先我们将使用 [<表格>](https://www.geeksforgeeks.org/html-tables/) 标签创建一个 HTML 表格，该标签由< tr >标签定义，用于创建行。它只是一个简单的 HTML/CSS 文件。唯一值得注意的是，我们正在使用 Bootstrap 4 CSS 框架为我们的页面赋予风格。如果你愿意，你可以使用你选择的任何其他样式框架或者编写你自己的 CSS。

## HTML

```html
<!DOCTYPE html>
<html>
    <head>
        <title>LeaderBoard Using PHP</title>
    </head>

    <body>
        <h2>Welcome To GFG</h2>
        <table>
            <tr>
                <td>Ranking</td>
                <td>UserName</td>
                <td>Marks</td>
            </tr>
```