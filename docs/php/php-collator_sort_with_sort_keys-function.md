# PHP | collator _ sort _ with _ sort _ keys()函数

> 原文:[https://www . geeksforgeeks . org/PHP-collator _ sort _ with _ sort _ keys-function/](https://www.geeksforgeeks.org/php-collator_sort_with_sort_keys-function/)

collator_sort_with_sort_keys()函数是 PHP 中的一个内置函数，用于使用指定的排序器和排序键对数组进行排序。

**语法:**

*   **Program style:**

    ```php
    *bool* collator_sort_with_sort_keys( $coll, $arr )
    ```

*   **Object-oriented style:**

    ```php
    *bool* Collator::sortWithSortKeys( $arr )
    ```

**参数:**该函数接受两个参数，如上所述，如下所述:

*   **$ coll:** This parameter is used as a sorter object. It provides the comparison function, and supports the proper sorting of distinguishing regions.
*   **$ arr:** This parameter is used to store the strings to be sorted.

**返回值:**该函数成功返回真，失败返回假。

下面的程序说明了 PHP 中的排序函数。

**程序 1:**

```php
<?php

// Declare an array which need to sort
$arr  = array( 'Geeks', 'g4g', 'GeeksforGeeks', 'geek' );
$coll = collator_create( 'gs' );

// Sort the array with key value
collator_sort_with_sort_keys( $coll, $arr );

var_export( $arr );
?>
```

**输出:**

```php
array (
  0 => 'g4g',
  1 => 'geek',
  2 => 'Geeks',
  3 => 'GeeksforGeeks',
)

```

**程序二:**

```php
<?php

// Declare an array which need to sort
$arr  = array( 'Geeks123', 'GeeksABC', 'GeeksforGeeks', 'Geeks' );

// Create collector
$coll = collator_create( 'en_US' );

// Sort the array with key value
collator_sort_with_sort_keys( $coll, $arr );

var_export( $arr );
?>
```

**输出:**

```php
array (
  0 => 'Geeks',
  1 => 'Geeks123',
  2 => 'GeeksABC',
  3 => 'GeeksforGeeks',
)

```

**参考:**[http://PHP . net/manual/en/collator . sortwithsortkeys . PHP](http://php.net/manual/en/collator.sortwithsortkeys.php)