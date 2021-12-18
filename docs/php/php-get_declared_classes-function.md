# PHP|GET_DECLARATED_CLASS()函数

> Original: [https://www.geeksforgeeks.org/php-get_declared_classes-function/](https://www.geeksforgeeks.org/php-get_declared_classes-function/)

GET_DECLARATED_CLASS()函数是 PHP 中的一个内置函数，用于返回具有已定义类名称的数组。 包含当前脚本中所有系统定义类(例如，PDO、XML 阅读器等)和用户定义类的列表的用户数组。 此函数未指定任何参数。

```php
<?php
class gfg {

    function add () {
        $a = 9 + 2 ;
    }
}

class gfg1 {
    function tr() {
        echo (4);
    }
}

print_r(get_declared_classes());
?>
```

**输出：**

```php
Array
(
    [0] => stdClass
    [1] => Exception
    [2] => ErrorException
    [3] => Error
    [4] => ParseError
    . . .
    [155] => Ds\PriorityQueue
    [156] => Ds\Pair
    [157] => gfg
    [158] => gfg1
)

```

**对列表进行排序：**在这么大的列表中找到特定的类可能很困难。 但是，如果按字母顺序对列表进行排序，可能会更容易。 可以通过函数`sort()`对其进行排序。

```php
<?php
$sorted = get_declared_classes();

sort($sorted);

print_r($sorted);
?>
```

**输出：**

```php
Array
(
    [0] => AppendIterator
    [1] => ArithmeticError
    [2] => ArrayIterator
    [3] => ArrayObject
    [4] => AssertionError
    . . .
    [152] => XMLWriter
    [153] => __PHP_Incomplete_Class
    [154] => finfo
    [155] => php_user_filter
    [156] => stdClass
)

```

**引用：**[https://www.php.net/manual/en/function.get-declared-classes.php](https://www.php.net/manual/en/function.get-declared-classes.php)