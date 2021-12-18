# PHP | Collator __construct()函数

> 原文:[https://www . geesforgeks . org/PHP-collator-_ _ construct-function/](https://www.geeksforgeeks.org/php-collator-__construct-function/)

**排序器::__construct()函数**是 PHP 中的一个内置函数，用于创建排序器的新实例。

**语法:**

```
*public* Collator::__construct( string $locale )
```

**参数:**该函数接受保存排序规则的单个参数 **$locale** 。如果为区域设置传递空值，将使用默认的区域设置排序规则。如果在区域设置中传递空字符串("")或“根”，则将使用 UCA 规则。

**返回值:**该函数返回排序器实例。

下面的程序说明了 PHP 中的 Collator::__construct()函数:

**程序 1:**

```
<?php
$coll = new Collator( 'en_CA' );

var_dump($coll);
?>
```

**输出:**

```
object(Collator)#1 (0) {
}

```

**程序二:**

```
<?php
$coll = new Collator( 'en_CA' );

// Declare array and initialize it 
$arr = array( 'geek', 'geeK', 'Geek', 'geeks' ); 

// Sort array 
collator_sort( $coll, $arr ); 

// Display array content 
var_export( $arr ); 
?> 
```

**输出:**

```
array (
  0 => 'geek',
  1 => 'geeK',
  2 => 'Geek',
  3 => 'geeks',
)

```

**参考:**T2】https://www.php.net/manual/en/collator.construct.php