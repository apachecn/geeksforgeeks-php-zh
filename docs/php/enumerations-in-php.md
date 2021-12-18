# PHP 中的枚举

> 原文:[https://www.geeksforgeeks.org/enumerations-in-php/](https://www.geeksforgeeks.org/enumerations-in-php/)

枚举(或 enum)主要用于给整型常量赋值，这些名字使程序易于阅读和维护。在 PHP 中，枚举数据类型可以使用和扩展抽象类来实现。

**方法 1:** 使用简单的抽象类来进行数据成员封装。

**例:**

```php
<?php
// PHP program to show use of enumerations

// Encapsulating constants
abstract class gfg {
    const dummy_string = "geeksforgeeks";
    const dummy_int    = 1;
    const dummy_array  = array('a' => 1, 'b' => 2);
}

$a = gfg::dummy_string;
$b = gfg::dummy_int;
$c = gfg::dummy_array;

var_dump($a);
var_dump($b);
var_dump($c);

?>
```

**输出:**

```php
string(13) "geeksforgeeks"
int(1)
array(2) {
  ["a"]=>
  int(1)
  ["b"]=>
  int(2)
}

```

**方法 2:** 扩展一个抽象类，作为封装常量的枚举容器。

**例:**

```php
<?php
// PHP program to show use of enumerations

// Base enumeration class
abstract class enum {

    // Enumeration constructor
    final public function __construct($value) {
        $this->value = $value;
    }

    // String representation
    final public function __toString() {
        return $this->value;
    }
}

// Encapsulating enumerated constants
class gfg extends enum {
    const dummy_string = "geeksforgeeks";
    const dummy_int    = 1;
    const dummy_array  = array('a' => 1, 'b' => 2);
}

$a = new gfg(gfg::dummy_string);
$b = new gfg(gfg::dummy_int);
$c = new gfg(gfg::dummy_array);

var_dump($a);
var_dump($b);
var_dump($c);

?>
```

**输出:**

```php
object(gfg)#1 (1) {
  ["value"]=>
  string(13) "geeksforgeeks"
}
object(gfg)#2 (1) {
  ["value"]=>
  int(1)
}
object(gfg)#3 (1) {
  ["value"]=>
  array(2) {
    ["a"]=>
    int(1)
    ["b"]=>
    int(2)
  }
}

```

**方法 3:** 前面方法中提到的枚举可以通过添加有效性检查和异常处理来专门化，以便更灵活地使用枚举数据类型。

**例:**

```php
<?php
// PHP program to show use of enumerations

// Base enumeration class
abstract class enum {

    // Enumeration constructor
    final public function __construct($value) {
        try {
            $c = new ReflectionClass($this);

            // Content validation
            if(!in_array($value, $c->getConstants())) {
                try {
                    throw new 
                    Exception("IllegalArgumentException");
                }
                catch (Exception $k) {
                    echo $k->getMessage();
                }
            }
            $this->value = $value;
        }
        catch (Exception $k){
            echo $k->getMessage();
        }
    }

    // String representation
    final public function __toString() {
        return $this->value;
    }
}

// Encapsulating enumerated constants
class gfg extends enum {
    const dummy_string = "geeksforgeeks";
    const dummy_int    = 1;
    const dummy_array  = array('a' => 1, 'b' => 2);
}

$a = new gfg(gfg::dummy_string);
$b = new gfg(gfg::dummy_int);
$c = new gfg(gfg::dummy_array);
$d = new gfg(3.14);

var_dump($a);
var_dump($b);
var_dump($c);
var_dump($d);
?>
```

**输出:**

```php
IllegalArgumentExceptionobject(gfg)#1 (1) {
  ["value"]=>
  string(13) "geeksforgeeks"
}
object(gfg)#2 (1) {
  ["value"]=>
  int(1)
}
object(gfg)#3 (1) {
  ["value"]=>
  array(2) {
    ["a"]=>
    int(1)
    ["b"]=>
    int(2)
  }
}
object(gfg)#4 (1) {
  ["value"]=>
  float(3.14)
}

```

**注意:** PHP 有[脾](http://php.net/manual/en/class.splenum.php)类，可以用于枚举，虽然实现并不是在 PHP 的所有稳定版本中都可用。