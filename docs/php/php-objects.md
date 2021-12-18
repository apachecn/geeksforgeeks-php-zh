# PHP|对象

> Original: [https://www.geeksforgeeks.org/php-objects/](https://www.geeksforgeeks.org/php-objects/)

**对象**是由类定义的数据结构的单个实例。 我们定义一个类一次，然后创建许多属于它的对象。 对象也称为实例。

**创建对象：**
下面是如何使用**new**运算符创建对象的示例。

```php
class Books {
   // Members of class Books
}

// Creating three objects of Books
$physics = new Books;
$maths = new Books;
$chemistry = new Books;

```

**成员函数：**
创建对象后，我们可以调用与该对象相关的成员函数。 成员函数通常只访问当前对象的成员。

示例：

```php
$physics->setTitle( "Physics for High School" );
$chemistry->setTitle( "Advanced Chemistry" );
$maths->setTitle( "Algebra" );

$physics->setPrice( 10 );
$chemistry->setPrice( 15 );
$maths->setPrice( 7 );
```

以下语法用于下面给出的示例中详细说明的以下程序：

示例：

```php
<?php
   class Books {

      /* Member variables */
      var $price;
      var $title;

      /* Member functions */
      function setPrice($par){
         $this->price = $par;
      }

      function getPrice(){
         echo $this->price."<br>";
      }

      function setTitle($par){
         $this->title = $par;
      }

      function getTitle(){
         echo $this->title."<br>" ;
      }
   }

   /* Creating New object using "new" operator */
   $maths = new Books;

   /* Setting title and prices for the object */
   $maths->setTitle( "Algebra" );
   $maths->setPrice( 7 );

   /* Calling Member Functions */  
   $maths->getTitle();
   $maths->getPrice();
?>
```

**构造函数：**
构造函数是 PHP 中面向对象编程中的一个关键概念。 PHP 中的构造函数是类的特殊类型的函数，在创建或实例化该类的任何对象时自动执行。
构造函数也称为魔术函数，因为在 PHP 中，魔术方法通常以两个下划线字符开头。

以下是实现构造函数的示例代码：
**构造函数程序：**

```php
<?php
class GeeksforGeeks
{    
    public $Geek_name = "GeeksforGeeks";

    // Constructor is being implemented.
    public function __construct($Geek_name)
    {
        $this->Geek_name = $Geek_name;
    }
}

// now constructor is called automatically 
// because we have initialized the object
// or class Bird.
$Geek = new GeeksforGeeks("GeeksforGeeks"); 
echo $Geek->Geek_name;
?>
```

发帖主题：Re：Колибри0.7.0

```php
GeeksforGeeks
```