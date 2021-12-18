# 如何用 PHP 从邮件 ID 中提取用户名？

> 原文:[https://www . geesforgeks . org/如何从电子邮件中提取用户名-id-using-php/](https://www.geeksforgeeks.org/how-to-extract-the-user-name-from-the-email-id-using-php/)

给定一个字符串电子邮件地址，提取用户名。

```
Input: ‘priyank@geeks.com’
Output: priyank

Input: ‘princepriyank@gfg.com’
Output: princepriyank

```

**方法 1:** **使用 PHP**[**strtr()**](https://www.geeksforgeeks.org/php-strstr-function/)**从电子邮件地址中提取用户名。**

在本例中，“@”符号是电子邮件地址的域名和用户名的分隔符。**strtr()**PHP 函数用于在另一个字符串(即电子邮件地址)中搜索第一个出现的字符串(即“@”)以获得用户名。

*   **第 1 步:**定义一个变量，并在其中存储电子邮件地址的值。

    ```
    $email= 'priyank@geeks.com';
    ```

*   **第 2 步:**通过使用这一行对字符串进行切分直到第一次出现“@”来获取用户名

    ```
    $username=strstr($email,'@',true);
    ```

*   **第 3 步:**使用 [*回显*](https://www.geeksforgeeks.org/php-echo-print/) 语句显示用户名。

    ```
    echo $username."\n";
    ```

**例:**

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```
<?php
  // Define Email Address
  $email  = 'priyank@geeks.com';

  // Get the username by slicing string
  $username = strstr($email, '@', true);

  // Display the username
  echo $username."\n";
?>
```

**Output**

```
priyank
```

**方法二:使用 PHP** [**爆()**](https://www.geeksforgeeks.org/php-explode-function/) **功能。**

在这里，我们利用了“@”符号是电子邮件地址的域名和用户名的分隔符这一事实。所以 **explode()** 是用来通过分隔符“@”将字符串分解成数组的。

*   **第一步:**定义一个变量*邮箱*并在里面存储邮箱地址的值。

    ```
    $email= 'princepriyank@geeks.com';
    ```

*   **第 2 步:**通过使用“@”作为分隔符分解(分割)字符串来获取用户名，并将第一部分存储在变量*用户名中。*

    ```
    $parts = explode("@",$email);
    $username = $parts[0];
    ```

*   **第 3 步:**使用该代码显示用户名。

    ```
    echo $username."\n";
    ```

**例:**

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```
<?php
// Define Email Address
$email  = 'princepriyank@geeks.com';

// Get the username by dividing mailid using'@' as separator
$parts = explode("@",$email);
$username = $parts[0];

// Display the username
echo $username."\n";
?>
```

**Output**

```
princepriyank
```