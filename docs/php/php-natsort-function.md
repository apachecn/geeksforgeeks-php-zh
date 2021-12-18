# PHP|natort()函数

> Original: [https://www.geeksforgeeks.org/php-natsort-function/](https://www.geeksforgeeks.org/php-natsort-function/)

Natort()函数是 PHP 中的一个内置函数，用于使用“自然顺序”算法对数组进行排序。 自然秩序告诉我们，秩序应该像普通人一样使用。 也就是说，它不检查要比较的值的类型。 例如，根据标准排序算法，字符串表示 30 小于 7，因为 3 在字典顺序上在 7 之前。 但在自然顺序中，30 大于 7。

**语法：**

```php
*bool* natsort(array)
```

**参数：**此函数接受单个参数*$array*。 它是 natort()函数将要排序的数组。

**返回值**：返回布尔值，成功时返回 TRUE，失败时返回 FALSE。

下面的程序演示了 PHP 中的 natort()函数：

**程序 1：**

```php
<?php

// input array
$arr1 = array("12.jpeg", "10.jpeg", "2.jpeg", "1.jpeg");
$arr2 = $arr1;

// sorting using sort function.
sort($arr1);

// printing sorted element.
echo "Standard sorting\n";
print_r($arr1);

// sorting using natsort() function.
natsort($arr2);

// printing sorted element.
echo "\nNatural order sorting\n";
print_r($arr2);

?>
```

产出：

```php
Standard sorting
Array
(
    [3] => 1.jpeg
    [1] => 10.jpeg
    [0] => 12.jpeg
    [2] => 2.jpeg
)

Natural order sorting
Array
(
    [3] => 1.jpeg
    [2] => 2.jpeg
    [1] => 10.jpeg
    [0] => 12.jpeg
)

```

**程序 2：**

```php
<?php

// input array
$arr = array("gfg15.jpeg", "gfg10.jpeg", "gfg1.jpeg",
                           "gfg22.jpeg", "gfg2.jpeg");

// sorting using natsort() function.
natsort($arr);

// printing sorted element.
echo "\nNatural order sorting\n";
print_r($arr);

?>
```

产出：

```php
Natural order sorting
Array
(
    [2] => gfg1.jpeg
    [4] => gfg2.jpeg
    [1] => gfg10.jpeg
    [0] => gfg15.jpeg
    [3] => gfg22.jpeg
)

```

**引用：**
[http://php.net/manual/en/function.natsort.php](http://php.net/manual/en/function.natsort.php)