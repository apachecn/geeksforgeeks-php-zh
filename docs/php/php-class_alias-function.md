# PHP | class_alias()函数

> 原文:[https://www.geeksforgeeks.org/php-class_alias-function/](https://www.geeksforgeeks.org/php-class_alias-function/)

class_alias()函数是 PHP 中的一个内置函数，用于创建类的别名。别名类的功能类似于原始类。

**语法:**

```
*bool* class_alias( *string* $original, *string* $alias, *bool* $autoload = TRUE )
```

**参数:**该函数接受三个参数，如上所述，如下所述:

*   **$ original:** This parameter holds the original class name.
*   **$ Alias:** This parameter stores the alias class name.
*   **$ Auto-load:** Whether to load automatically if the original class cannot be found.

**返回值:**返回布尔值，即成功时为真，失败时为假。

下面的程序说明了 PHP 中的 class_alias()函数:

**程序 1:**

```
<?php

// Create a class
class GFG {

    public $Geek_name = "Welcome to GeeksforGeeks"; 

    // Constructor is being implemented. 
    public function __construct($Geek_name) { 
        $this->Geek_name = $Geek_name; 
    } 
} 

// Create the class name alias
class_alias('GFG', 'GeeksforGeeks');

// Create an object
$Geek = new GeeksforGeeks("GeeksforGeeks"); 

// Display result
echo $Geek->Geek_name; 
?>
```

**输出:**

```
GeeksforGeeks

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

// Create the class name alias
class_alias('GFG', 'Geeks');

// Creating an object 
$obj1 = new GFG(); 
$obj2 = new Geeks();

var_dump($obj1 === $obj2);

// Set values of $obj object 
$obj2->data1 = "Geeks"; 
$obj2->data2 = "for"; 
$obj2->data3 = "Geeks"; 

// Print values of $obj object 
echo "$obj2->data1  \n$obj2->data2  \n$obj2->data3"; 

?>
```

**输出:**

```
bool(false)
Geeks  
for  
Geeks

```

**参考:**T2】https://www.php.net/manual/en/function.class-alias.php