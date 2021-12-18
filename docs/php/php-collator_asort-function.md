# PHP | collator_asort()函数

> 原文:[https://www.geeksforgeeks.org/php-collator_asort-function/](https://www.geeksforgeeks.org/php-collator_asort-function/)

collator_asort()函数是 PHP 中的一个内置函数，用于对维护索引关联的数组进行排序。此函数对数组进行排序，使数组索引保持与关联数组元素的相关性。数组元素根据当前的区域设置规则进行排序。

**语法:**

*   **Program style:**

    ```php
    bool collator_asort( $coll, &$arr, $sort_flag )
    ```

*   **Object-oriented style:**

    ```php
    public bool Collator::asort( &$arr, $sort_flag )
    ```

**参数:**该函数接受三个参数，如上所述，如下所述:

*   **$ coll:** This parameter is used as a sorter object.
*   **$ arr:** This parameter contains an array of strings to be sorted.
*   **$ sort _ flag:** is an optional parameter used to define the sort method, one of the following:
    *   **Sorter:: sort _ regular:** Normal comparison items. This is the default sort.
    *   **Sorter:: sort _ numeric:** It compares items with numbers.
    *   **Sorter:: sort _ string:** It compares items as strings.

**返回值:**该函数成功返回真，失败返回假。

下面的程序说明了 PHP 中的 collator_asort()函数:

**程序 1:**

```php
<?php
$coll = collator_create( 'en_US' );
$arr = array(
     'A' => '30',
     'B' => '48',
     'C' => '9',
     'D' => '60'
);

// Sort array according to its numeral value
collator_asort( $coll, $arr, Collator::SORT_NUMERIC );
var_export( $arr );
?>
```

**输出:**

```php
array (
  'C' => '9',
  'A' => '30',
  'B' => '48',
  'D' => '60',
)

```

**程序二:**

```php
<?php
$coll = collator_create( 'en_US' );
$arr = array(
     'A' => '30',
     'B' => '48',
     'C' => '9',
     'D' => '60'
);

// Sort array according to its string value
collator_asort( $coll, $arr, Collator::SORT_STRING );
var_export( $arr );
?>
```

**输出:**

```php
array (
  'A' => '30',
  'B' => '48',
  'D' => '60',
  'C' => '9',
)

```

**相关文章:**

*   [PHP | uasort()魏冄](https://www.geeksforgeeks.org/php-uasort-function/)
*   [PHP | rsort()989](https://www.geeksforgeeks.org/php-rsort-function/)

**参考:**T2】http://php.net/manual/en/collator.asort.php