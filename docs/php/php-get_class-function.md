# PHP|get_class()函数

> Original: [https://www.geeksforgeeks.org/php-get_class-function/](https://www.geeksforgeeks.org/php-get_class-function/)

Get_class()函数是 PHP 中的内置函数，用于返回对象的类名。

**语法：**

```
*string* get_class( *object* $object )
```

**参数：**此函数接受单个参数**$object**，该参数保存需要测试的对象。 此参数的值可以在类中省略。

**返回值：**此函数返回对象为实例的类名。 如果对象不是对象，则返回 False。 如果在类中省略对象，则返回类名。

下面的程序演示了 PHP 中的 get_class()函数：

**程序 1：**

```
<?php

// Create a class
class GFG {

    public function Geeks() {
        echo "Class name: " . get_class($this);
    }
}

// Create an object
$obj = new GFG();

$obj->Geeks();

?>
```

**输出：**

```
Class name: GFG

```

**程序 2：**

```
<?php

// Creating class 
class GFG { 
    public $data1; 
    public $data2; 
    public $data3; 
}

if(class_exists('GFG')) {

    $obj = new GFG();

    echo "Class name: " . get_class($obj);
}
else {
    echo "Class does not exist";
}

?>
```

**输出：**

```
Class name: GFG

```

**引用：**[https://www.php.net/manual/en/function.get-class.php](https://www.php.net/manual/en/function.get-class.php)