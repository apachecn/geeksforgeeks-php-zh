# 如何使用 ajax 通过 POST 向 PHP 后端发送按钮值？

> 原文:[https://www . geesforgeks . org/how-send-button-value-to-PHP-后端-via-post-use-Ajax/](https://www.geeksforgeeks.org/how-to-send-button-value-to-php-backend-via-post-using-ajax/)

本文的目的是在 HTML 文档中使用 AJAX 将按钮的值发送到 PHP 后端。

**方法:**在 HTML 文档中创建一个按钮，并为其分配一个 Id。在 JavaScript 文件中，给按钮添加一个事件监听器，即点击。然后使用 jQuery Ajax 向 PHP 文件发出请求。

**HTML 代码:**

## HTML

```html
<!-- HTML Code -->
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content=
        "width=device-width, initial-scale=1.0">

    <!-- JavaScript file -->
    <script src="script.js"></script>

    <!-- jQuery Ajax CDN -->
    <script src=
"https://ajax.googleapis.com/ajax/libs/jquery/3.5.1/jquery.min.js">
    </script>
</head>

<body>

    <!-- Button -->
    <button id="btn" value="hello world">
        Click On me!
    </button>
</body>

</html>
```