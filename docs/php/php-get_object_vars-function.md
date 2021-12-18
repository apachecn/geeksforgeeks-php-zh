# PHP|get_object_vars()函数

> Original: [https://www.geeksforgeeks.org/php-get_object_vars-function/](https://www.geeksforgeeks.org/php-get_object_vars-function/)

GET_OBJECT_vars()函数是 PHP 中的一个内置函数，用于获取给定对象的属性。 当一个对象被制作时，它具有一些属性。 该函数返回所述对象的属性的关联数组。 但如果没有该对象的属性，则返回 NULL。

**语法：**

```php
get_object_vars( $object )
```

**参数：**此函数接受如上所述的单个参数，如下所述：
**$Object：**此参数保存实例的对象。
**返回值：**此方法返回作用域中指定对象的可访问的关联数组对象的非静态属性。

下面的程序演示了 PHP 中的 get_object_vars()函数：

**程序 1：**

## PHP

```php
<?php

// Declare a class
class gfg {

    // Properties of an object
    // of this class
    private $geeks = 0.02;
    public $for = 1;
    public $Geeks = "php";
    private $GEEKS;
    static $e;

    public function example() {
        var_dump(get_object_vars($this));
    }
}

// Create an object of a class
$example = new gfg;

// Display properties of the
// newly created object
var_dump(get_object_vars($example));

$example->example();

?>
```

**Output:** 

```php
array(2) {
  ["for"]=>
  int(1)
  ["Geeks"]=>
  string(3) "php"
}
array(4) {
  ["geeks"]=>
  float(0.02)
  ["for"]=>
  int(1)
  ["Geeks"]=>
  string(3) "php"
  ["GEEKS"]=>
  NULL
}
```

**程序 2：**

## PHP

```php
<?php

// Create a class
   class coordinate {

        // The properties of the
        // object of this class
        var $x;
        var $y;
        var $z;
        var $labels;

        function coordinate($x, $y, $z) {
            $this->x = $x;
            $this->y = $y;
            $this->z = $z;
        }

        function to_set($labels) {
            $this->labels = $labels;
        }
    }

    $point1 = new coordinate(0.1, 0.2, 0.3);
    print_r(get_object_vars($point1));

    $point1->to_set("point 1");
    print_r(get_object_vars($point1));

?>
```

**Output:** 

```php
Array
(
    [x] => 0.1
    [y] => 0.2
    [z] => 0.3
    [labels] => 
)
Array
(
    [x] => 0.1
    [y] => 0.2
    [z] => 0.3
    [labels] => point 1
)
```

**引用：**[https://www.php.net/manual/en/function.get-object-vars.php](https://www.php.net/manual/en/function.get-object-vars.php)