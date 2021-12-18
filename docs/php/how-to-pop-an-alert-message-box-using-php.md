# 如何用 PHP 弹出提醒消息框？

> 原文:[https://www . geesforgeks . org/how-pop-a-alert-message-box-use-PHP/](https://www.geeksforgeeks.org/how-to-pop-an-alert-message-box-using-php/)

网站中使用了一个警告框，向用户显示警告消息，提示他们输入了错误的值，而不是填写该位置所需的值。警告框仍然可以用于更友好的消息。警告框只给出一个按钮“确定”来选择和继续。

警报消息就像屏幕上的弹出窗口。使用这个你可以提醒用户一些信息和消息。PHP 不支持**提醒消息框**，因为它是一种服务器端语言，但是您可以使用 **PHP** 主体内的 JavaScript 代码来提醒屏幕上的消息框。

**语法:**

```
alert("Message")
```

**程序 1:** PHP 程序在屏幕上弹出一个提醒框。

## PHP

```
<?php
// PHP program to pop an alert
// message box on the screen

// Display the alert box 
echo '<script>alert("Welcome to Geeks for Geeks")</script>';

?>
```