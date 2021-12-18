# PHP |访问说明符

> 原文:[https://www.geeksforgeeks.org/php-access-specifiers/](https://www.geeksforgeeks.org/php-access-specifiers/)

在 [**PHP**](https://www.geeksforgeeks.org/php/) 中，一个类的每个属性都必须有三个可见性级别中的一个，称为**公共**、**私有**、**受保护**。

*   **Public:** 任何代码都可以访问公共属性，无论该代码是在类内部还是类外部。如果一个属性被声明为公共的，它的值可以从脚本中的任何地方读取或更改。
*   **Private:** 类的私有属性只能由类内部的代码访问。因此，如果我们创建一个声明为私有的属性，那么只有同一个类中的方法和对象才能访问它的内容。
*   **Protected:** Protected 类属性有点像私有属性，因为它们不能被类外的代码访问，但是任何从类继承的类都有一点不同，即基类也可以访问属性。

一般来说，尽可能避免创造公共财产是个好主意。相反，更安全的做法是创建私有属性，然后创建允许类外代码访问这些属性的方法。这意味着我们可以精确地控制如何访问类的属性。
**注意:**如果我们试图访问类外的属性，PHP 会产生一个致命错误。
**PHP 访问说明符对类、子类和外部世界的可行性:**

<figure class="table">

| Class access specifier | Access from your own class | Access from a derived class | Access through object |
| privately own | be | no | no |
|  |

</figure>

下面的例子说明了 PHP 的访问说明符:

*   **示例 1:** 在本例中，我们将看到公共访问说明符。

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```
<?php 
class GeeksForGeeks
{ 
public $x = 100 ;  # public attributes
public $y = 50 ; 
    function add() 
{ 
echo $a = $this->x + $this->y ;
echo " ";
} 
    }    
class child extends GeeksForGeeks
{ 
function sub() 
{ 
echo $s = $this->x - $this->y ; 
} 

}   

$obj = new child; 

// It will return the addition result
$obj->add() ; 

// It's a derived class of the main class,
// which has a public object and therefore can be
// accessed, returning the subtracted result.
$obj->sub() ;

?> 
```

*   **输出:**

```
150 50
```

*   **示例 2:** 在本例中，我们将看到私有访问说明符

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```
<?php 
class GeeksForGeeks
{ 
private $a = 75 ;  # private attributes
private $b = 5 ; 
    private function div()  # private member function
{ 
echo $d = $this->a / $this->b ;
echo " ";
} 
    }    
class child extends GeeksForGeeks
{ 
function mul() 
{ 
echo $m = $this->a * $this->b ; 
} 

}   

$obj= new child; 

// It's supposed to return the division result
// but since the data and function are private
// they can't be accessed by a derived class
// which will lead to fatal error .
$obj->div();

// It's a derived class of the main class,
// which's accessing the private data
// which again will lead to fatal error .
$obj->mul();
?> 
```

*   **输出:**

```
PHP Fatal error:  Uncaught Error: Call to private method 
GeeksForGeeks::div() from context '' in /home/cg/root/8030907/
main.php:22 Stack trace:#0 {main} thrown in /home/cg/root/8030907/
main.php on line 22
```

*   **示例 3:** 在本例中，我们将看到受保护访问说明符。

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```
<?php
class GeeksForGeeks
{
protected $x = 1000 ; # protected attributes
protected $y = 100 ;
    function div()
{
echo $d = $this->x / $this->y ;
echo " ";
}
    }    
class child extends GeeksForGeeks
{
function sub()
{
echo $s = $this->x - $this->y ;
}

}
class derived # Outside Class
{
function mul()
{
echo $m = $this->x * $this->y ;
}

}
$obj= new child;

// It will return the division result
$obj->div();

// Since it's a derived class of the main class,
$obj->sub();

// Since it's an outside class, therefore it
// will produce a fatal error .
$obj->mul();

?>
```

*   **输出:**

```
10
900
Fatal error:  Uncaught Error: Call to undefined method 
child::mul() in /home/cg/root/8030907/main.php:32
```