# 如何在 PHP 中创建默认函数参数？

> 原文:[https://www . geesforgeks . org/how-create-default-function-parameter-in-PHP/](https://www.geeksforgeeks.org/how-to-create-default-function-parameter-in-php/)

默认参数的概念来自 C++风格的默认参数值，与 PHP 中相同，您可以提供默认参数，以便当参数没有传递给函数时。那么它在具有预定义值的函数中仍然可用。该功能也可称为 **[可选参数](https://www.geeksforgeeks.org/how-to-create-optional-arguments-in-php/)** 。

**语法:**

```php
function greeting($name=" parameter_value ")
```

**参数:**这个函数接受一个参数，这里是 **$name** ，保存参数值。

以下示例说明了创建和使用默认函数参数的过程:
**示例 1:**

```php
<?php  
    function greeting($name="GeeksforGeeks")
    {  
        echo "Welcome to $name ";  
        echo("\n");
    }  
    greeting("Gfg"); 

    // Passing no value 
    greeting(); 
    greeting("A Computer Science Portal");  
?>  
```

**输出:**

```php
Welcome to Gfg 
Welcome to GeeksforGeeks 
Welcome to A Computer Science Portal 
```

**例 2:**

```php
<?php    
    function welcome($first="GeeksforGeeks",
                     $last="A Computer Science Portal for Geeks")
                     {    
                        echo "Greeting: $first $last";   
                        echo("\n");
    }    
    welcome();  
    welcome("night_fury");  
    welcome("night_fury","Contributer");  
?>    
```

**输出:**

```php
Greeting: GeeksforGeeks A Computer Science Portal for Geeks
Greeting: night_fury A Computer Science Portal for Geeks
Greeting: night_fury Contributer
```