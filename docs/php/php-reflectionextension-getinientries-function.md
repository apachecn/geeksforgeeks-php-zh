# PHP|ReflectionExtension getINIEntries()函数

> Original: [https://www.geeksforgeeks.org/php-reflectionextension-getinientries-function/](https://www.geeksforgeeks.org/php-reflectionextension-getinientries-function/)

**ReflectionExtension：：getINIEntries()函数**是 PHP 中的一个内置函数，用于返回一个数组，其中 ini 条目作为键，它们定义的值作为值。

**语法：**

```
*Array* ReflectionExtension::getINIEntries( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回一个数组，其中 ini 条目作为键，它们定义的值作为值。

下面的程序演示了 PHP 中的 ReflectionExtension：：getINIEntries()函数：

**程序 _1：**

```
<?php

// Defining an extension
$A = 'DOM';

// Using ReflectionExtension() over the 
// specified extension
$extension = new ReflectionExtension($A);

// Calling the getINIEntries() function
$B = $extension->getINIEntries();

// Getting an array with the ini
// entries as keys and their 
// defined values as values.
var_dump($B);
?>
```

**输出：**

```
array(0) {
}

```

**程序 _2：**

```
<?php

// Using ReflectionExtension() over 
// a extension pcre
$extension = new ReflectionExtension("pcre");

// Calling the getINIEntries() function and
// Getting an array with the ini
// entries as keys and their 
// defined values as values.
var_dump($extension->getINIEntries());
?>
```

**输出：**

```
array(3) {
  ["pcre.backtrack_limit"]=>
  string(7) "1000000"
  ["pcre.recursion_limit"]=>
  string(6) "100000"
  ["pcre.jit"]=>
  string(1) "1"
}

```

**引用：**[https://www.php.net/manual/en/reflectionextension.getinientries.php](https://www.php.net/manual/en/reflectionextension.getinientries.php)