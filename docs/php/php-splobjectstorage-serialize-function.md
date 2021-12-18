# PHP|SplObjectStorage Serialize()函数

> Original: [https://www.geeksforgeeks.org/php-splobjectstorage-serialize-function/](https://www.geeksforgeeks.org/php-splobjectstorage-serialize-function/)

**SplObjectStorage：：Serialize()**函数是 PHP 中的内置函数，用于序列化存储结果。

**语法：**

```php
*string* SplObjectStorage::serialize()
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回表示存储的字符串。

下面的程序说明了 PHP 中的**SplObjectStorage：：Serialize()**函数：

**程序 1：**

```php
<?php

// Create new storage class
$str = new SplObjectStorage;
$obj = new StdClass;

$str->attach($obj, "GeeksforGeeks");

// Print serialize result 
echo $str->serialize();
?>
```

**输出：**

```php
x:i:1;O:8:"stdClass":0:{}, s:13:"GeeksforGeeks";;m:a:0:{}

```

**程序 2：**

```php
<?php

$obj1 = new StdClass;
$obj2 = new StdClass;

// Create new storage class
$gfg1 = new SplObjectStorage();
$gfg1[$obj1] = "Geeks";

// Create new storage class
$gfg2 = new SplObjectStorage();
$gfg2[$obj1] = "GFG";
$gfg2[$obj2] = "GeeksClasses";

print_r( $gfg1->serialize(). "\n");
echo( $gfg2->serialize()."\n");

?>
```

**输出：**

```php
x:i:1;O:8:"stdClass":0:{}, s:5:"Geeks";;m:a:0:{}
x:i:2;O:8:"stdClass":0:{}, s:3:"GFG";;O:8:"stdClass":0:{}, s:12:"GeeksClasses";;m:a:0:{}

```

**引用：**[https://www.php.net/manual/en/splobjectstorage.serialize.php](https://www.php.net/manual/en/splobjectstorage.serialize.php)