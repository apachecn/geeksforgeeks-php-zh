# PHP|var_dump()函数

> Original: [https://www.geeksforgeeks.org/php-var_dump-function/](https://www.geeksforgeeks.org/php-var_dump-function/)

在开发领域中，调试与编码同等重要。 当开发人员需要检查变量的信息时，可能会出现这种情况，例如，如果函数返回数组，最好检查返回类型和返回值的内容。 开发人员可以回显所有内容，但是 PHP 本身提供了一个方法来执行相同的操作并检查数据类型。

函数的作用是：转储有关变量的信息。 此函数显示给定变量的类型和值等结构化信息。 数组和对象以递归方式浏览，值缩进以显示结构。 此函数对表达式也有效。

**语法：**

```
*void* var_dump ($expsn)

```

**参数**：该函数接受单个参数$expsn，该参数可以是单个变量，也可以是包含多个任意类型的空格分隔变量的表达式。

**返回类型**：此函数没有返回类型。
示例：

```
Input :  $expsn = 2.7;   
Output : float(2.7)

Input : $expsn = array(1, 2, array(3, 4, 5));
Output : array(3) { 
            [0]=> int(1) 
            [1]=> int(2) 
            [2]=> array(3) { 
                    [0]=> int(3) 
                    [1]=> int(4) 
                    [2]=> int(5) 
             } 
          }        

```

下面的程序演示了 PHP 中 var_dump()的工作原理：

```
<?php

// PHP code to illustrate the working
//  of var_dump() Function 

var_dump(var_dump(2, 2.1, TRUE, array(1, 2, 3, 4)));

?>
```

产出：

```
int(2) 
float(2.1) 
bool(true) 
array(4) { 
  [0]=> int(1) 
  [1]=> int(2) 
  [2]=> int(3) 
  [3]=> int(4) 
}
NULL

```

**需要注意的重要事项**：

*   对象的所有属性(无论是公共的、私有的还是受保护的)都将在输出中返回，除非该对象实现 __debugInfo()方法。