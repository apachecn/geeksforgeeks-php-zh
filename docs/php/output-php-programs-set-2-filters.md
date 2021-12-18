# PHP 程序输出|集 2(过滤器)

> 原文:[https://www . geesforgeks . org/output-PHP-programs-set-2-filters/](https://www.geeksforgeeks.org/output-php-programs-set-2-filters/)

预测以下 PHP 程序的输出:
**问题 1**

```
<?php
    $num = "123";
    if (!filter_var($num, FILTER_VALIDATE_INT))
        echo("Hello");
    else
        echo("Welcome to GeeksforGeeks");
?>
```

选项:

1.  不返回任何输出
2.  你好
3.  欢迎来到极客博客
4.  错误

输出:

```
Welcome to GeeksforGeeks

```

**解释:**filter _ var()–用指定的过滤器过滤单个变量。

**问题 2**

```
<?php
    $var=300;
    $int_options = array("options"=>array ("min_range"=>0, "max_range"=>256));
    if (!filter_var($var, FILTER_VALIDATE_INT, $int_options))
        echo("Hello");
    else
        echo("Welcome to GeeksforGeeks");
?>
```

选项:

1.  不返回任何输出
2.  你好
3.  欢迎来到极客博客
4.  错误

输出:

```
Hello

```

**说明:**由于整数是“300”，所以不在指定范围内，上面代码的输出会是:“整数无效”。

**问题 3**

```
<?php
    $string = "Welcomeêê to GeêêeksfoøørGeêêeks";
    $string = filter_var($string, FILTER_SANITIZE_EMAIL);
    echo $string;
?>
```

选项:

1.  欢迎光临寒舍
2.  欢迎来到 GeeeeksfooorGeeeeks
3.  欢迎来到 geêeksfoørgeêeks
4.  WelcometoGeeksforGeeks

输出:

```
WelcometoGeeksforGeeks

```

**解释:** Sanitize 只是带走无效字符或特殊字符，因此像ê和和空格这样的无效字符将被删除。

**问题 4**

```
<?php
    $value = 'GeeksforGeeks';
    $result = filter_var($value, FILTER_VALIDATE_BOOLEAN, FILTER_NULL_ON_FAILURE);
?>
```

选项:

1.  错误的
2.  真实的
3.  无输出
4.  错误

输出:

```
No Output

```

**解释:**FILTER _ VALIDATE _ BOOLEAN 有一个未记录的过滤标志。该文档暗示，如果值与允许的真/假值不匹配，它将返回空值。然而，这不会发生，除非你给它一个过滤器 _ 空 _ 开 _ 失败标志。因此，输出将是无输出。

**问题 5**

```
<?php
    function GeeksforGeeks($string)
    {
        return str_replace("_", " ", $string);
    }
    $string = "I_am_intern_at_GeeksforGeeks!";
    echo filter_var($string, FILTER_CALLBACK, array("options"=>"GeeksforGeeks"));
?>
```

选项:

1.  我是极客的实习生！
2.  IaminternatGeeksforGeeks！
3.  我是极客公司的实习生！
4.  错误

输出:

```
I am intern at GeeksforGeeks!

```

**说明:**上面的代码将所有“_”转换为空格。使用 FILTER_CALLBACK 筛选器和包含我们函数的数组调用 filter_var()函数。

**问题 6**

```
<?php
    $num = '123+abc-xyz*';
    $num = filter_var($num, FILTER_SANITIZE_NUMBER_INT);
    echo $num
?>
```

选项:

1.  123+abc-xyz*
2.  abc.xyz 公司
3.  123+-
4.  错误

输出:

```
123+-

```

**说明:**FILTER _ var()–使用 FILTER_SANITIZE_NUMBER_INT，删除除数字、+-和可选字符以外的所有字符。

**问题 7**

```
<?php
    $num = '123+-abc*';
    $res = filter_var($num, FILTER_SANITIZE_NUMBER_FLOAT);
    echo $res
?>
```

选项:

1.  123+abc-xyz*
2.  abc.xyz 公司
3.  123+-
4.  错误

输出:

```
123+-

```

**说明:**FILTER _ var()–使用 FILTER_SANITIZE_NUMBER_FLOAT，删除除数字、+-和可选字符以外的所有字符。