# PHP|SplObjectStorage unSerialize()函数

> Original: [https://www.geeksforgeeks.org/php-splobjectstorage-unserialize-function/](https://www.geeksforgeeks.org/php-splobjectstorage-unserialize-function/)

**SplObjectStorage：：UnSerialize()**函数是 PHP 中的一个内置函数，用于将存储从其序列化字符串表示中反序列化。

**语法：**

```php
*void* SplObjectStorage::unserialize( $serilize )
```

**参数：**此函数接受单个参数**$Serialize**，该参数指定存储的字符串序列化。

**返回值：**此函数不返回任何值。

下面的程序说明了 PHP 中的**SplObjectStorage：：UnSerialize()**函数：

**程序 1：**

```php
<?php

$obj1 = new StdClass;

// Create an empty SplObjectStorage
$gfg1 = new SplObjectStorage();
$gfg1[$obj1] = "Geeks";

// Use unserialize() function
$gfg1->unserialize($gfg1->serialize());
print_r($gfg1);

?>
```

**输出：**

```php
SplObjectStorage Object
(
    [storage:SplObjectStorage:private] => Array
        (
            [00000000494fcd4d000000001f544823] => Array
                (
                    [obj] => stdClass Object
                        (
                        )

                    [inf] => Geeks
                )

            [00000000494fcd4f000000001f544823] => Array
                (
                    [obj] => stdClass Object
                        (
                        )

                    [inf] => Geeks
                )

        )

)

```

**程序 2：**

```php
<?php

$obj1 = new StdClass;
$obj2 = new StdClass;

// Create an empty SplObjectStorage
$gfg1 = new SplObjectStorage();
$gfg1[$obj1] = "Geeks";

// Create an empty SplObjectStorage
$gfg2 = new SplObjectStorage();
$gfg2[$obj1] = "GFG";
$gfg2[$obj2] = "GeeksClasses";

// Use unserialize() function
$gfg1->unserialize($gfg2->serialize());
var_dump(count($gfg1));

// Use unserialize() function
$gfg2->unserialize($gfg1->serialize());
var_dump(count($gfg2));
?>
```

**输出：**

```php
int(3)
int(5)

```

**引用：**[https://www.php.net/manual/en/splobjectstorage.unserialize.php](https://www.php.net/manual/en/splobjectstorage.unserialize.php)