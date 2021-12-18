# PHP|内爆爆炸

> Original: [https://www.geeksforgeeks.org/php-imploding-exploding/](https://www.geeksforgeeks.org/php-imploding-exploding/)

内爆和爆炸是 PHP 的两个重要函数，可以应用于字符串或数组。 PHP 为我们提供了两个重要的内置函数[implode()](https://www.geeksforgeeks.org/php-implode-function/)和[explode()](https://www.geeksforgeeks.org/php-explode-function/)来执行这些操作。 顾名思义，**implode/implode()**方法将数组元素与用作粘合剂的字符串段连接在一起，类似的**EXPLODE/EXPLODE()**方法做的恰恰相反，即给定一个字符串和一个分隔符，它在分隔符的帮助下创建一个字符串数组。

**内爆()方法**

**语法：**

```php
string implode (glue ,pieces)

```

或,

```php
string implode (pieces)

```

**参数**：该函数接受两个参数，如下所述。

*   **glue(可选)：**此参数需要一个用作连接数组片段的粘合剂的字符串段。 这是一个可选参数，默认值为空字符串。
*   **片段：**此参数需要一个数组，该数组的元素将连接在一起以构造最终的内爆字符串。

**返回类型**：此函数遍历输入数组，并用一个粘合段将每个元素连接起来，以构造并返回最终的内爆字符串。

下面的程序演示了 PHP 中的 implode()的工作原理：

```php
<?php
// PHP code to illustrate the working of implode()

$array1 = array('www', 'geeksforgeeks', 'org');
echo(implode('.',$array1)."<br>"); 

$array2 = array('H', 'E', 'L', 'L', 'O');
echo(implode($array2));
?>
```

产出：

```php
www.geeksforgeeks.org
HELLO

```

您可以参考关于[PHP|implode()函数](https://www.geeksforgeeks.org/php-implode-function/)的文章来详细了解 implode()。

**EXPLODE()方法**

**语法：**

```php
array explode (delimiter, string, limit)

```

**参数**：该函数接受三个参数，如下所述。

*   **分隔符：**此参数需要可用作分隔符的字符串段。 如果字符串中不存在分隔符本身，则结果将是包含该字符串作为其唯一元素的数组。
*   **字符串：**此参数需要一个要分解的字符串。
*   **限制：**此参数需要一个整数(正负)。 这是一个可选参数，默认值为 PHP_INT_MAX。 该限制指的是要对输入字符串进行的最大划分数。

**返回类型**：此函数返回包含分隔段的字符串数组。

下面的程序演示了在 PHP 中 EXPLODE()的工作原理：

```php
<?php
// PHP code to illustrate the working of explode()

$str1 = '1,2,3,4,5';
$arr = explode(',',$str1);
foreach($arr as $i)
echo($i.'<br>');
?>
```

产出：

```php
1
2
3
4
5

```

您可以参考关于[PHP|EXPLODE()函数](https://www.geeksforgeeks.org/php-explode-function/)的文章来详细了解 EXPLODE()。

**注意要点**：

*   函数的作用是：对数组中的元素进行内爆运算，并返回结果字符串。
*   尽管不建议这样做，但是 implode()函数可以接受参数，而不考虑它们的顺序
*   函数[PHP|Join()函数](https://www.geeksforgeeks.org/php-join-function/)是 implode()函数的别名。