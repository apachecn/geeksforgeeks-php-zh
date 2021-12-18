# PHP | class_exists()函数

> 原文:[https://www.geeksforgeeks.org/php-class_exists-function/](https://www.geeksforgeeks.org/php-class_exists-function/)

**class_exists()** 函数是 PHP 中的一个内置函数，用于检查给定的类是否被定义。

**语法:**

```
bool class_exists( string $class_name, bool $autoload = TRUE )
```

**参数:**这个函数接受两个参数，如上所述，如下所述:

*   **$ class _ name:** It holds the class names that need to be checked for their existence.
*   **$ auto-load:** By default, check whether _ _ auto-load is called.

**返回值:**如果定义了类名，该函数返回真，否则返回假。

下面的程序说明了 PHP 中的 **class_exists()** 函数:

**程序 1:**

```
<?php

// Create a class
class GFG {
    public $Geek_name = "Welcome to GeeksforGeeks"; 
} 

// Check class name exist or not
if(class_exists('GFG')) {
    echo "Class name exists";
}
else {
    echo "Class name does not exist";
}

?>
```

**输出:**

```
Class name exists

```

**程序二:**

```
<?php

// Creating class 
class GFG { 
    public $data1; 
    public $data2; 
    public $data3; 
}

if(class_exists('GFG')) {

    // Creating an object 
    $obj = new GFG();

    // Set values of $obj object 
    $obj->data1 = "Geeks"; 
    $obj->data2 = "for"; 
    $obj->data3 = "Geeks"; 

    // Print values of $obj object 
    echo "$obj->data1  \n$obj->data2  \n$obj->data3"; 
}
else {
    echo "Class does not exist";
}

?>
```

**输出:**

```
Geeks  
for  
Geeks

```

**参考:**T2】https://www.php.net/manual/en/function.class-exists.php