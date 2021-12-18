# PHP 程序输出|第三集

> 原文:[https://www.geeksforgeeks.org/output-php-programs-set-3/](https://www.geeksforgeeks.org/output-php-programs-set-3/)

预测以下 PHP 程序的输出:

**问题 1**

```
<?php
    $number = array(0, 1, one, two, three, 5);
    $num = preg_grep("/[0-5]/", $number);
    print_r($num);
?>
```

选项:

1.  数组([0]=>0 [1]=>1 [2]= >一[3]= >二[4]= >三[5]=>5)
2.  数组([2]= >一[3]= >二[4]= >三)
3.  数组([1]=> 1)
4.  数组([0]=>0 [1]=>1 [5]=>5)

输出:

```
Array([0]=>0 [1]=>1 [5]=>5)

```

**解释:**preg _ grep()函数用于在数组中搜索特定的模式，然后根据该过滤返回一个新的数组。

**问题 2**

```
<?php
    $number = array(0, 1, one, two, three, 5);
    $num = preg_grep("/[0-5]/", $number, PREG_GREP_INVERT);
    print_r($num);
?>
```

选项:

1.  数组([0]=>0 [1]=>1 [2]= >一[3]= >二[4]= >三[5]=>5)
2.  数组([2]= >一[3]= >二[4]= >三)
3.  数组([1]=> 1)
4.  数组([0]=>0 [1]=>1 [5]=>5)

输出:

```
Array([2]=>one [3]=>two [4]=>three)

```

**解释:**当我们包含 PREG _ GREP _ INVERT 时，这将反转我们的数据，因此它将输出我们的非数值，而不是输出数字。

**问题 3**

```
<?php
    $name = "I am intern at GeeksforGeeks.";
    if (preg_match("/at/",$name))
    echo "My name is Sagar Shukla";
    else
    echo "My name is not Sagar Shukla";
?>
```

选项:

1.  我叫萨加尔·舒克拉
2.  我不叫萨加尔·舒克拉
3.  错误
4.  无输出

输出:

```
My name is Sagar Shukla

```

**说明:**代码使用 preg_match()检查关键字，并根据它是真(1)还是假(0)进行回复。

**问题 4**

```
<?php
    $name = "I am intern at GeeksforGeeks.";
    if (preg_match("/was/",$name))
    echo "My name is Sagar Shukla";
    else
    echo "My name is not Sagar Shukla";
?>
```

选项:

1.  我叫萨加尔·舒克拉
2.  我不叫萨加尔·舒克拉
3.  错误
4.  无输出

输出:

```
My name is not Sagar Shukla

```

**说明:**代码使用 preg_match 检查某个关键字，并根据它是真(1)还是假(0)进行回复。

**问题 5**

```
<?php
    $str = "I am intern at GeeksforGeeks";
    $find = array('/am/');
    $replace = array('was');
    echo preg_replace ($find, $replace, $str);
?>
```

选项:

1.  我是极客公司的实习生
2.  我在极客公司实习
3.  错误

5.  无输出

输出:

```
I was intern at GeeksforGeeks

```

**说明:**在上面的程序中，am 替换为 was 作为 preg PHP 函数用于对字符串或数组进行查找和替换。

**问题 6**

```
<?php
    $str = "I am intern at GeeksforGeeks";
    $find = array('/geeksforgeeks/');
    $replace = array('GEEKSFORGEEKS');
    echo preg_replace ($find, $replace, $str);
?>
```

选项:

1.  我是极客公司的实习生
2.  我是极客公司的实习生
3.  错误
4.  无输出

输出:

```
I am intern at GeeksforGeeks

```

**解释:** GeeksforGeeks 未被替换，因为 preg_replace 函数区分大小写。因此，它对极客和极客有不同的待遇。

**问题 7**

```
<?php
    $line = "Hello. Welcome to GeeksforGeeks!";
    $sen = preg_split('/\./', $line);
    print_r($sen);
?>
```

选项:

1.  你好。欢迎来到极客乐园！
2.  数组([0]= >你好。欢迎来到极客乐园！)
3.  数组([0]= >你好[1]= >欢迎来到 GeeksforGeeks！)
4.  Error

    输出:

    ```
    Array([0]=> Hello [1]=> Welcome to GeeksforGeeks! )

    ```

    **解释:**我们用一个“.”句点来分割数据，因此给每个句子一个自己的数组条目。