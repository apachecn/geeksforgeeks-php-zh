# PHP|ReflectionExtension getDependency()函数

> Original: [https://www.geeksforgeeks.org/php-reflectionextension-getdependencies-function/](https://www.geeksforgeeks.org/php-reflectionextension-getdependencies-function/)

**ReflectionExtension：：getDependency()函数**是 PHP 中的一个内置函数，用于返回一个数组，该数组以依赖项作为键，以必需、可选或冲突作为值。

**语法：**

```
*array* ReflectionExtension::getDependencies( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回一个关联数组，该数组包含作为键的依赖项，以及作为值的 Required、Optional 或 Conflicts。

下面的程序演示了 PHP 中的 ReflectionExtension：：getDependency()函数：

**程序 1：**

```
<?php

// Defining an extension
$A = 'DOM';

// Using ReflectionExtension() over the 
// specified extension
$extension = new ReflectionExtension($A);

// Calling the getDependencies() function
$B = $extension->getDependencies();

// Getting an array with dependencies as keys
// and either Required, Optional or 
// Conflicts as the values.
var_dump($B);
?>
```

**输出：**

```
array(2) {
  ["libxml"]=>
  string(8) "Required"
  ["domxml"]=>
  string(9) "Conflicts"
}

```

**程序 2：**

```
<?php

// Using ReflectionExtension() over 
// an extension xml
$extension = new ReflectionExtension('xml');

// Calling the getDependencies() function and
// Getting an array with dependencies as keys
// and either Required, Optional or 
// Conflicts as the values.
var_dump($extension->getDependencies());
?>
```

**输出：**

```
array(1) {
  ["libxml"]=>
  string(8) "Required"
}

```

**引用：**[https://www.php.net/manual/en/reflectionextension.getdependencies.php](https://www.php.net/manual/en/reflectionextension.getdependencies.php)