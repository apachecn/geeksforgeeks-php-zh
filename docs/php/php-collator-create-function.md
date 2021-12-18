# PHP | Collator create()函数

> 原文:[https://www.geeksforgeeks.org/php-collator-create-function/](https://www.geeksforgeeks.org/php-collator-create-function/)

**Collator::create()函数**是 PHP 中的一个内置函数，用于创建一个新的收集器。

**语法:**

*   **Object-oriented style:**

    ```php
    *Collator* Collator::create( $locale )
    ```

*   **Program style:**

    ```php
    *Collator* collator_create( $locale )
    ```

**参数:**该函数接受单个参数 **$locale** ，该参数保存所需的排序规则。如果为区域设置传递空值，将使用默认的区域设置排序规则。如果在区域设置中传递空字符串("")或“根”，则将使用 UCA 规则。

**返回值:**该函数成功返回排序器对象的新实例，错误返回空值。

下面的程序说明了 PHP 中的 Collator::create()函数:

**程序 1:**

```php
<?php
$coll = collator_create( 'en_US' );

if(isset($coll)){
    echo "Collector created";
}
else {
    echo "Collector not created";
}
?>
```

**输出:**

```php
Collector created

```

**程序二:**

```php
<?php 
$coll = collator_create( 'en_US' ); 

// Declare array and initialize it 
$arr = array( 'geek', 'geeK', 'Geek', 'geeks' ); 

// Sort array 
collator_sort( $coll, $arr ); 

// Display array content 
var_export( $arr ); 
?> 
```

**输出:**

```php
array (
  0 => 'geek',
  1 => 'geeK',
  2 => 'Geek',
  3 => 'geeks',
)

```

**参考:**T2】https://www.php.net/manual/en/collator.create.php