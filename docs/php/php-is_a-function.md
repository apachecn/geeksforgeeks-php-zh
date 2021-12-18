# PHP|is_a()函数

> Original: [https://www.geeksforgeeks.org/php-is_a-function/](https://www.geeksforgeeks.org/php-is_a-function/)

Is_a()是 PHP 中的内置函数，用于检查给定对象是否属于给定的类。 它还检查给定的类是否为给定对象的父类之一。

**语法**：

```php
*boolean* is_a($object, $class)

```

**参数**：此函数接受上述语法中的两个参数，解释如下：

*   **$OBJECT：**要测试的给定对象。
*   **$class：**类的名称。

**返回类型**：如果参数*$OBJECT*给出的对象属于*$CLASS*或将此*$CLASS*作为其父对象，则返回 TRUE，否则返回 FALSE。

下面的程序说明了 is_a()函数：

**程序 1**：

```php
<?php
// PHP program to illustrate the 
// is_a() function

// sample class
class GeeksforGeeks
{
    var $store = 'geek';
}

// create a new object
$geek = new GeeksforGeeks();

// checks if $geek is an object
// of class GeeksforGeeks
if (is_a($geek, 'GeeksforGeeks')) 
{
    echo "YES";
}

?>
```

产出：

```php
YES

```

**程序 2**：

```php
<?php
// PHP program to illustrate the 
// is_a() function

interface parentClass 
{
    public function A();
}

class childClass implements parentClass 
{
    public function A () 
    {
        print "A";
    }
}

$object = new childClass();

if(is_a($object, 'parentClass'))
{
    echo "YES";
}
else
{
    echo "NO";
}

?>
```

产出：

```php
YES

```

**参考**：
[http://php.net/manual/en/function.is-a.php](http://php.net/manual/en/function.is-a.php)