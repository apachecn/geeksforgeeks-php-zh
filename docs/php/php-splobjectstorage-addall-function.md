# PHP|SplObjectStorage addAll()函数

> Original: [https://www.geeksforgeeks.org/php-splobjectstorage-addall-function/](https://www.geeksforgeeks.org/php-splobjectstorage-addall-function/)

**SplObjectStorage：：addAll()**函数是 PHP 中的一个内置函数，用于从另一个存储添加元素。

**语法：**

```php
*void* SplObjectStorage::addAll( $value )
```

**参数：**此函数接受单个参数**$value**，该参数保存需要导入的存储。

**返回值：**不返回任何值。

下面的程序说明了 PHP 中的**SplObjectStorage：：addAll()**函数：

**程序 1：**

```php
<?php

// Declare an empty std class
$obj = new StdClass;

// Declare an empty SplObjectStorage
$gfg = new SplObjectStorage();

$gfg[$obj] = "GeeksforGeeks";

$gfg1 = new SplObjectStorage();
$gfg1->addAll($gfg);

// Print result added to storage object
echo $gfg1[$obj] . "\n";
?>
```

**输出：**

```php
GeeksforGeeks

```

**程序 2：**

```php
<?php

// Declare an empty std class
$obj = new StdClass;
$obj2 = new StdClass;

// Declare an empty SplObjectStorage
$gfg = new SplObjectStorage();
$gfg[$obj] = "GeeksforGeeks";
$gfg[$obj2] = "GeeksforGeeks2";

$gfg1 = new SplObjectStorage();
$gfg1->addAll($gfg);

// Print result with whole object
print_r($gfg1);
?>
```

**输出：**

```php
SplObjectStorage Object
(
    [storage:SplObjectStorage:private] => Array
        (
            [00000000219a7b260000000055def3bf] => Array
                (
                    [obj] => stdClass Object
                        (
                        )

                    [inf] => GeeksforGeeks
                )

            [00000000219a7b250000000055def3bf] => Array
                (
                    [obj] => stdClass Object
                        (
                        )

                    [inf] => GeeksforGeeks2
                )

        )

)

```

**引用：**[https://www.php.net/manual/en/splobjectstorage.addall.php](https://www.php.net/manual/en/splobjectstorage.addall.php)