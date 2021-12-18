# PHP|使用 unset()函数

从数组中删除元素的程序

> Original: [https://www.geeksforgeeks.org/php-program-delete-element-array-using-unset-function/](https://www.geeksforgeeks.org/php-program-delete-element-array-using-unset-function/)

给定一个元素数组，我们必须使用**[unset()](https://www.geeksforgeeks.org/php-unset-function/)**函数从数组中删除一个元素。

示例：

```php
Input : $arr = array("Harsh", "Nishant", "Bikash", "Barun");
        unset($arr[3]);
Output : Array
         (
           [0] => Harsh
           [1] => Nishant
           [2] => Bikash
         )

Input : $arr = array(1, 2, 6, 7, 8, 9);
        unset($arr[3]);
Output : Array
         (
           [0] => 1
           [1] => 2
           [2] => 6
           [4] => 8
           [5] => 9
         )

```

**[unset()函数](https://www.geeksforgeeks.org/php-unset-function/)**：该函数接受变量名作为参数，并销毁或取消设置该变量。

**方法：**使用 unset 函数解决此问题的想法是将要从数组中删除的各个元素的数组键作为参数传递给此函数，从而删除与其关联的值，即该索引处的数组元素。

以下程序说明了上述方法：

**程序 1：**

```php
<?php

    $a = array("Harsh", "Bikash", "Nishant", "Barun", "Deep");

    // unset command accepts 3rd index and
    // thus removes the array element at
    // that position
    unset($a[3]);

    print_r ($a);

?>
```

帖子主题：Re：Колибри

**程序 2：**

```php
<?php

    $a = array(1, 8, 9, 7, 3, 5, 4, );

    // unset command accepts 3rd index and
    // thus removes the array element
    // at that position
    unset($a[5]);

    print_r ($a);

?>
```

帖子主题：Re：Колибри

**注意**：使用 unset()函数后，数组键不会重新排序。