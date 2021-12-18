# PHP|unset()函数

> Original: [https://www.geeksforgeeks.org/php-unset-function/](https://www.geeksforgeeks.org/php-unset-function/)

Unset()函数是 PHP 中的内置函数，用于取消设置指定的变量。 此函数的行为取决于不同的内容。 如果该函数是从任何用户定义的函数内部调用的，则它取消设置与其内部变量相关联的值，而将初始化的值留在其外部。

这意味着该函数仅取消设置局部变量。 如果要取消设置函数内部的全局变量，则必须使用[$GLOBALS](http://php.net/manual/en/reserved.variables.globals.php)数组来执行此操作。

**语法**

```php
unset($variable)
```

**参数**

*   **$Variable：**此参数为必填项，是需要取消设置的变量

**返回值：**此函数不返回任何值。

下面的程序演示了 PHP 中的 unset()函数：

**程序 1：**

```php
<?php

      $var = "hello";

      // No change would be reflected outside
      function unset_value()
      {
          unset($var);
      }

      unset_value();
      echo $var;
?>
```

外部：

```php
hello

```

**程序 2：**

```php
<?php

      $var = "hello";

      // Change would be reflected outside the function 
      function unset_value()
      {
          unset($GLOBALS['var']);
      }

      unset_value();
      echo $var;
?>
```

产出：

```php
No Output

```

**程序 3：**

```php
<?php

      // user-defined function
      function unset_value()
      {
          static $var = 0;
          $var++;

          echo "Before unset:".$var." ";

          unset($var);

          // This will create a new variable with
          // existing name
          $var = 5;

          echo "After unset:".$var."\n";          
      }

      unset_value();
      unset_value();
      unset_value();
      unset_value();

?>
```

产出：

```php
Before unset:1 After unset:5
Before unset:2 After unset:5
Before unset:3 After unset:5
Before unset:4 After unset:5

```

**注意：**如果变量声明为静态，并且在函数内部未设置，则只在函数的其余上下文中受影响。 上述函数外部调用将恢复该值。

**参考**：
[http://php.net/manual/en/function.unset.php](http://php.net/manual/en/function.unset.php)