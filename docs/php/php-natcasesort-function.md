# PHP|natcasesort()函数

> Original: [https://www.geeksforgeeks.org/php-natcasesort-function/](https://www.geeksforgeeks.org/php-natcasesort-function/)

Natcasesort()函数是 PHP 中的一个内置函数，用于使用“自然顺序”算法对数组进行排序。 自然秩序告诉我们，秩序应该像普通人一样使用。 也就是说，它不检查要比较的值的类型。 例如，根据标准排序算法，字符串表示 30 小于 7，因为 3 在字典顺序上在 7 之前。 但在自然顺序中，30 大于 7。此外，natcasesort()函数不区分大小写。

**语法：**

```php
*bool* natcasesort($array )
```

**参数：**此函数接受单个参数*$array*。 它是 natcasesort()函数将要排序的数组。

**返回值**它返回一个布尔值，即成功时返回 TRUE，失败时返回 FALSE。

下面的程序演示了 PHP 中的 natcasesort()函数：

**程序 1**：

```php
<?php

// input array
$arr1 = array("Gfg12.jpeg", "gfg10.jpeg", "Gfg2.jpeg", "gfg1.jpeg");
$arr2 = $arr1;

// sorting using sort function.
sort($arr1);
echo "Standard sorting\n";
print_r($arr1);

// Sorting using natcasesort() function.
natcasesort($arr2);
echo "Natural order case insensitve: ";
print_r($arr2);

?>
```

产出：

```php
Standard sorting:
Array
(
    [0] => Gfg12.jpeg
    [2] => Gfg2.jpeg
    [3] => gfg1.jpeg
    [1] => gfg10.jpeg
)

Natural order case insensitve: 
Array
(
    [3] => gfg1.jpeg
    [2] => Gfg2.jpeg
    [1] => gfg10.jpeg
    [0] => Gfg12.jpeg
)

```

**程序 2**：

```php
<?php

// input array
$arr = array("Gfg15.jpeg", "gfg10.jpeg", "Gfg1.jpeg", 
                        "gfg22.jpeg", "Gfg2.jpeg");

// Sorting using natcasesort() function.
natcasesort($arr);

print_r($arr);

?>
```

产出：

```php
Array
(
    [2] => Gfg1.jpeg
    [4] => Gfg2.jpeg
    [1] => gfg10.jpeg
    [0] => Gfg15.jpeg
    [3] => gfg22.jpeg
)

```

**引用：**
[http://php.net/manual/en/function.natcasesort.php](http://php.net/manual/en/function.natcasesort.php)