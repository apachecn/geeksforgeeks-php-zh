# PHP|get_class_method()函数

> Original: [https://www.geeksforgeeks.org/php-get_class_methods-function/](https://www.geeksforgeeks.org/php-get_class_methods-function/)

GET_CLASS_METHOD()函数是 PHP 中的一个内置函数，用于获取类方法名称。

**语法：**

```
*array* get_class_methods( *mixed* $class_name )
```

**参数：**此函数接受单个参数**$class_name**，该参数保存类名或对象实例。

**返回值：**此函数在成功时返回为类定义的方法名称数组，在出错时返回 NULL。

下面的程序演示了 PHP 中的 get_class_method()函数：

**程序 1：**

```
<?php

// Create a class
class GFG {

    public function Geeks() {
        var_dump(get_called_class());
    }

    public function GeeksforGeeks() {
        var_dump(get_called_class());
    }
}

$getClassMethod = get_class_methods('GFG');

foreach ($getClassMethod as $method) {
    echo "$method\n";
}

?>
```

**输出：**

```
Geeks
GeeksforGeeks

```

**程序 2：**

```
<?php

// Create a class
class GFG {

    public function Geeks() {
        var_dump(get_called_class());
    }

    public function GeeksforGeeks() {
        var_dump(get_called_class());
    }

    public function G4G() {
        // Empty method
    }
}

class_alias('GFG', 'GeeksforGeeks');

$getClassMethod = get_class_methods('GeeksforGeeks');

foreach ($getClassMethod as $method) {
    echo "$method\n";
}

?>
```

**输出：**

```
Geeks
GeeksforGeeks
G4G

```

**引用：**[https://www.php.net/manual/en/function.get-class-methods.php](https://www.php.net/manual/en/function.get-class-methods.php)