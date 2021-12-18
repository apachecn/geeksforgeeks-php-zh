# PHP|parse_str()函数

> Original: [https://www.geeksforgeeks.org/php-parse_str-function/](https://www.geeksforgeeks.org/php-parse_str-function/)

Parse_str()函数是 PHP 中的一个内置函数，用于将查询字符串解析为变量。 传递给此函数进行解析的字符串采用通过 URL 传递的查询字符串的格式。

**语法：**

```
parse_str($string, $array)
```

**参数：**此函数接受上述语法中所示的两个参数，其中第一个参数必须提供，第二个参数是可选的。 所有这些参数如下所述：

*   **$string：**它指定要解析的字符串。
*   **$array：**这是一个可选参数，指定存储变量的数组名称。 此参数指示变量将存储在数组中。

例如：

```
Input : "name=Richik&age=20"
Output :  $name = Richik
          $age = 20

Input : "roll_no=2&year=2nd&gpa=8.3"
Output : $roll_no = 2
         $year = 2nd
         $gpa = 8.3

```

下面的程序演示了 PHP 中的 parse_str()函数：

**程序 1：**

```
<?php

    parse_str("name=Richik&age=20");
    echo $name."\n".$age;
?>
```

产出：

```
Richik
20

```

**程序 2：**在此程序中，我们将变量存储在数组中，然后使用 print_r()函数显示该数组。

```
<?php

    parse_str("roll_no=2&year=2nd&gpa=8.3", $array);
    print_r($array);

?>
```

产出：

```
Array
(
    [roll_no] => 2
    [year] => 2nd
    [gpa] => 8.3
)

```

**引用：**
[http://php.net/manual/en/function.parse-str.php](http://php.net/manual/en/function.parse-str.php)