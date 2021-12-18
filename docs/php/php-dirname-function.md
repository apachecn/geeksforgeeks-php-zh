# PHP|dirname()函数

> Original: [https://www.geeksforgeeks.org/php-dirname-function/](https://www.geeksforgeeks.org/php-dirname-function/)

PHP 中的 dirname()函数是一个内置函数，用于返回给定路径的目录名。 函数的作用是：将目录的路径设置为父目录，即从当前目录向上。

函数的作用是：返回包含点(‘.’)的父目录的路径。 如果路径没有斜杠，则表示当前目录。

**语法：**

```
string dirname ( $path )
```

**参数：**PHP 中的 dirname()函数只接受一个参数，即$path。 此参数指定要检查的路径。

**返回值：**返回父目录的路径。

**错误和异常**：

1.  在指定路径时，正斜杠(/)和反斜杠(\)在 Windows 环境中用作目录分隔符，而在其他环境中，它只用作正斜杠(/)。
2.  Dirname()函数对输入字符串进行操作，因此它不知道实际的文件系统或路径组件(如“..”)。

**示例：**

```
Input : dirname("user01/geeksforgeeks/gfg.txt")
Output : user01/geeksforgeeks

Input : dirname("/geeksforgeeks/gfg.txt");
Output : /geeksforgeeks

```

下面的程序说明了 dirname()函数：

**程序 1**：

```
<?php

// specifying path to the dirname() function
echo dirname("user01/geeksforgeeks/gfg.txt")

?>
```

产出：

```
user01/geeksforgeeks
```

**程序 2**：

```
<?php

// specifying path to the dirname() function
echo dirname("/geeksforgeeks/gfg.txt");

?>
```

产出：

```
/geeksforgeeks
```

**引用：**
[http://php.net/manual/en/function.dirname.php](http://php.net/manual/en/function.dirname.php)