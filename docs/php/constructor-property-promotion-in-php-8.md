# PHP 8 中的构造函数属性提升

> 原文:[https://www . geesforgeks . org/constructor-property-promotion-in-PHP-8/](https://www.geeksforgeeks.org/constructor-property-promotion-in-php-8/)

构造函数属性提升是一种简单的简写语法，用于从构造函数中声明和分配类属性。构造函数属性提升是 PHP 8 新版本中提供的一种新语法，它允许从构造函数进行类属性声明和构造函数赋值，而无需进入样板代码的状态。

在计算机编程中，样板代码是在多个地方重复的代码段，很少或没有变化，这使得代码重复、复杂且不易看到。在 PHP 新的更新之前，我们必须在构造函数中重复变量，如下所示。

**例 1:**

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```php
<?php

class GFG {
    public $name;
    public $university;

    // Boilerplate code
    function __construct($name, $university) {
        $this->name = $name;
        $this->university = $university;
    }
    function get_name() {
        return $this->name;
    }
    function get_university() {
        return $this->university;
    }
}

$a = new GFG("Atul Sisodiya", "JECRC");
echo $a->get_name();
echo "<br>";
echo $a->get_university();

?>
```

**输出:**

```php
Atul Sisodiya
JECRC
```

**例 2:**PHP 8 版本最新更新后，提供了更简单语法的构造函数属性提升。

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```php

<?php

class GFG {
    public function __construct(
        public string $name, 
        public string $university) {
           $this->name = $name;
           $this->university = $university;
        }

    function get_name() {
        return $this->name;
    }

    function get_university() {
        return $this->university;
    }
}

$a = new GFG("Atul Sisodiya", "JECRC");
echo $a->get_name();
echo "<br>";
echo  $a->get_university();

?>
```

**输出:**

```php
Atul Sisodiya
JECRC
```