# PHP 中如何保护数据库密码？

> 原文:[https://www . geesforgeks . org/如何保护数据库安全-php 中的密码/](https://www.geeksforgeeks.org/how-to-secure-database-passwords-in-php/)

大多数网站都为用户提供了注册和登录功能。用户必须创建一个密码，并使用它登录网站。但是保护用户的密码是非常重要的。 [**password_hash()**](https://www.geeksforgeeks.org/php-crypt-password_hash-functions/) 功能提供了将用户密码安全存储到数据库的功能。

**语法**

```php
password_hash(Password, PASSWORD_DEFAULT)
```

**示例:**第一个参数 Password 将包含正常密码。第二个参数将包含 PASSWORD_BCRYPT 以确保安全，否则它包含 PASSWORD_DEFAULT 作为默认值。让我们看看例子来正确理解。

*   **dbconn.php**

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```php
<?php 
  $db_host = "localhost";
  $db_name = "secure_pass";
  $db_pass = "";
  $db_user = "root";

  $conn = mysqli_connect($db_host, $db_user, $db_pass, $db_name);

  if (!$conn){
    die ('Failed to connect with server');
  }   
?>
```

*   **报名表格:**

## 超文本标记语言

```php
<form action="index.php" method="POST">
  <label for="username">Username</label>
  <input type="text" name="username" required><br><br>

  <label for="password">Password</label>
  <input type="password" name="password" required><br><br>
  <input type="submit" name="submit" value="submit">   
</form>
```