# PHP|get_call_class()函数

> Original: [https://www.geeksforgeeks.org/php-get_called_class-function/](https://www.geeksforgeeks.org/php-get_called_class-function/)

**get_call_class()函数**是 PHP 中的一个内置函数，用于获取调用静态方法的类名。

**语法：**

```
string get_called_class( void )
```

**参数：**此方法不接受任何参数。

**返回值：**此函数成功时返回类名，如果从类外部调用则返回 False。

下面的程序演示了 PHP 中的 get_call_class()函数：

**程序 1：**

```
<?php

// Create a class
class GFG {
    public $Geek_name = "Welcome to GeeksforGeeks"; 

    public function Geeks() {
        var_dump(get_called_class());
    }
}

GFG::Geeks();

?>
```

**输出：**

```
string(3) "GFG"

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
}

GFG::Geeks();
GFG::GeeksforGeeks();

class_alias('GFG', 'GeeksforGeeks');

GeeksforGeeks::Geeks();
GeeksforGeeks::GeeksforGeeks();

?>
```

**输出：**

```
string(3) "GFG"
string(3) "GFG"
string(3) "GFG"
string(3) "GFG"

```

**引用：**[https://www.php.net/manual/en/function.get-called-class.php](https://www.php.net/manual/en/function.get-called-class.php)