# PHP|ReflectionMethod Invoke()函数

> Original: [https://www.geeksforgeeks.org/php-reflectionmethod-invoke-function/](https://www.geeksforgeeks.org/php-reflectionmethod-invoke-function/)

**ReflectionMethod：：Invoke()函数**是 PHP 中的内置函数，用于调用指定的反射方法并返回该方法的结果。
**语法：**和

```
*public mixed* ReflectionMethod::invoke ( *$object*, *$parameter* )
```

**参数：**此函数接受两个参数，如下图所示：

*   **对象：**这是已初始化的类对象。
*   **参数：**这是要传递给方法的零个或多个参数。

**返回值：**此函数返回调用的方法的结果。
以下程序说明 PHP 中的**ReflectionMethod：：Invoke()函数**：
**Program_1：**和

## PHP

```
<?php

// Initializing a user-defined class
class Company {

    public function GFG($name) {
        return 'GeeksforGeeks' . $name;
    }
}

// Using ReflectionMethod() over the class Company
$A = new ReflectionMethod('Company', 'GFG');

// Calling the invoke() function
$B = $A->invoke(new Company(),
          ' is a Computer Science Portal.');

// Getting the result of the invoked method.
echo $B;
?>
```

**Output:** 

```
GeeksforGeeks is a Computer Science Portal.
```

**程序 _2：**

## PHP

```
<?php

// Initializing some user-defined classes
class Department1 {

    public function hr($name) {
        return 'HR' . $name;
    }
}
class Department2 {

    public function coding($name) {
        return 'Coding' . $name;
    }
}
class Department3 {

    public function marketing($name) {
        return 'Marketing' . $name;
    }
}

// Using ReflectionMethod() over the above classes
$A = new ReflectionMethod('Department1', 'hR');
$B = new ReflectionMethod('Department2', 'coding');
$C = new ReflectionMethod('Department3', 'marketing');

// Calling the invoke() function and
// getting the result of the invoked method.
echo $A->invoke(new Department1(), ' is a Department.');
echo "\n";
echo $B->invoke(new Department2(), ' is also a Department.');
echo "\n";
echo $C->invoke(new Department3(), ' too.');
?>
```

**Output:** 

```
HR is a Department.
Coding is also a Department.
Marketing too.
```

**引用：**[https://www.php.net/manual/en/reflectionmethod.invoke.php](https://www.php.net/manual/en/reflectionmethod.invoke.php)，