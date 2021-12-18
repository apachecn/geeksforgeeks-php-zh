# PHP 中 bindParam 和 bindValue 的区别

> 原文:[https://www . geesforgeks . org/bind param-和-bindvalue-in-php 之间的区别/](https://www.geeksforgeeks.org/difference-between-bindparam-and-bindvalue-in-php/)

**PDOStatement::bindParam()函数**

PDOStatement::bindParam()函数是 PHP 中的内置函数，用于将参数绑定到指定的变量名。该函数绑定变量，将它们的值作为输入传递，并接收相关参数标记的输出值(如果有)。

**语法:**

```
*bool* PDOStatement::bindParam
( $parameter, $variable, $data_type, $length, $driver_options )
```

**参数:**该功能接受五个参数，如上所述，描述如下:

*   **$parameter:** 是一个参数标识符，用于使用名称占位符准备语句。它是表单的参数名:name。
*   **$variable:** 此参数用于保存要绑定到 SQL 语句参数的变量名称。
*   **$data_type:** 它是使用 PDO::PARAM_*常量的参数的显式数据类型。
*   **$length:** 此参数用于保存数据类型的长度。
*   **$driver_options:** 该参数保存需要执行的操作。

**返回值:**该函数成功返回真，失败返回假。
T3】程序:T5】

```
<?php  

// setup PDO connection
$db = new PDO('mysql:host=localhost;dbname=geeks','root',''); 

// Get username
$username = 'geesforgeeks';

$stmt = $db->prepare("SELECT * FROM users WHERE user = :username");

// Use bindParam function
$stmt->bindParam(':username', $username);

 $username = 'g4g';

 $stmt->execute();
?>
```

**注意:**SQL 语句将使用‘g4g’作为用户名执行，因为:用户名在执行时会搜索$username，而$username 的最后一个已知值是‘g4g’。

**PDOStatement::bindValue()函数**

PDOStatement::bindValue()函数是 PHP 中的内置函数，用于将值绑定到参数。此函数将一个值绑定到用于准备语句的 SQL 中相应的命名或问号占位符。

**语法:**

```
*bool* PDOStatement::bindValue( $parameter, $value, $data_type )
```

**参数:**该功能接受三个参数，如上所述，描述如下:

*   **$parameter:** 是一个参数标识符，用于使用名称占位符准备语句。它是表单的参数名:name。
*   **$value:** 此参数用于保存绑定参数的值。
*   **$data_type:** 它是使用 PDO::PARAM_*常量的参数的显式数据类型。

**返回值:**该函数成功返回真，失败返回假。
T3】节目:

```
<?php  

// setup PDO connection
$db = new PDO('mysql:host=localhost;dbname=geeks','root',''); 

// Get username
$username = 'geeksforgeeks';

$stmt = $db->prepare("SELECT * FROM users WHERE user = :username");

// Use bindValue function
$stmt->bindValue(':username', $username);

$username = 'g4g';

$stmt->execute();
?>
```

**注意:**SQL 语句将使用‘geesforgeks’作为用户名执行，因为文字值“geesforgeks”在 bindValue()函数之前已经绑定到:username。对$username 的进一步更改将不会反映在准备好的声明中。

【bindParam()和 bindValue()的区别:

1.  **bindParam():**
    1.  函数**将参数**绑定到 SQL 语句中的命名或问号占位符。
    2.  bindParam()函数用于**传递变量而不是值**。
2.  **绑定区域():T1**
    1.  bindValue()函数**将一个值**绑定到 SQL 语句中的命名或问号。
    2.  bindValue()函数用于**传递值和变量**。