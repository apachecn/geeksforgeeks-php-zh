# PHP 中如何像数字一样递增字母？

> 原文:[https://www . geesforgeks . org/如何在 php 中增加类似数字的字母/](https://www.geeksforgeeks.org/how-to-increment-letters-like-numbers-in-php/)

给定一些字母，任务就是像我们增加数字一样增加字母。我们将遇到各种情况并确定结果。

**示例:**

*   递增后的数字

    ```php
    0 1 2 3...
    ```

*   递增后的字母

    ```php
    a b c d...
    ```

还有一件有趣的事情需要注意，就像数字以 9 个字母后的两位数开头一样，遇到“z”后也是如此

*   **数字:**

    ```php
    0 1 2 3 ... 9 10 11 12 .. . 99 100 101 ...
    ```

*   **字母:**

    ```php
    a b c d ... z aa ab ac ... zz aaa aab ...
    ```

这可以像在数字中一样，使用简单的增量(++)运算符来实现。唯一不同的是，减量(–)运算符在字母中的作用不同于在数字中的作用。

**例 1:** 程序递增各种字母并打印。

```php
<?php
$i = 'a';
print(++$i . " ");

$j = 'aa';
print(++$j . " ");

$k = 'aaa';
print(++$k . " ");

$l = 'aaaa';
print(++$l);
?>
```

**输出:**

```php
b ab aab aaab
```

**例 2:** 打印‘a’到‘y’之间所有字母的程序。

```php
<?php
$i = 'a';

for( $i; $i < 'z'; $i++ )
    print($i);
?>
```

**输出:**本例循环至‘y’，因为如果在达到‘z’之前设置了的限制，则要求的结果是不同的。循环执行，直到遇到“z”

```php
abcdefghijklmnopqrstuvwxy
```

**注意:**减量对字母不起作用

**程序 3:** 显示减量对字母不起作用的程序。

```php
<?php
$i = 'd';

for( $i; $i > 'a'; $i-- )
    print($i);
?>
```

**输出:**

```php
The following program produces an infinite loop of letter 'd'
```