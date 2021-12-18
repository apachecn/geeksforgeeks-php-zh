# 用&符号启动一个 PHP 函数是什么意思？

> 原文:[https://www . geesforgeks . org/用&符号启动一个 php 函数意味着什么/](https://www.geeksforgeeks.org/what-does-it-mean-to-start-a-php-function-with-an-ampersand/)

函数名前的&符号将返回对变量的引用，而不是返回值。当您想要使用函数来查找引用应该绑定到哪个变量时，按引用返回非常有用。不要使用按引用返回来提高性能。在 PHP 4 中，对象是按值分配的，就像任何其他值一样。这是非常反直觉的，与大多数其他语言的工作方式相反。

**示例:**这个示例演示了放一个&符号来启动一个 PHP 函数背后的概念。

由 **getValue()函数**返回的对象的属性将被设置，而不是像没有使用引用语法那样被设置。与参数传递不同，这里你必须在两个地方都使用&符号来表示你想通过引用而不是副本返回，并表示引用绑定，而不是通常的赋值，应该为 **$myValue** 完成。

```
<?php
class student
{
    public $value = 42;

    public function &getValue()
    {
        return $this->value;
    }
}

$obj = new student;

// $myValue is a reference to 
// $obj->value, which is 42.
$myValue = & $obj->getValue(); 
$obj->value = 2;

// Prints the new value of 
// $obj->value, i.e. 2.
echo $myValue; 

?>
```

**输出:**

```
2
```