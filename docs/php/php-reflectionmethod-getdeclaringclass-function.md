# PHP|ReflectionMethod getDeclaringClass()函数

> Original: [https://www.geeksforgeeks.org/php-reflectionmethod-getdeclaringclass-function/](https://www.geeksforgeeks.org/php-reflectionmethod-getdeclaringclass-function/)

**ReflectionMethod：：getDeclaringClass()**函数是 PHP 中的内置函数，用于返回声明的类的名称。

**语法：**

```php
 *ReflectionClass* ReflectionMethod::getDeclaringClass ( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回反射方法的声明类的名称。

以下程序说明了**ReflectionMethod：：getDeclaringClass()**函数：

**程序 1：**

```php
<?php

// Declaring a class
class GeeksforGeeks {

    // Declaring a protected function
    protected function CSportal($name) {

        // Displays output
        return 'Geeks ' . $name;
    }

}

// Creating an object of ReflectionMethod
$reflectionMethod = new ReflectionMethod(new GeeksforGeeks(), 'CSportal');

// Calling getDeclaringClass function
var_dump($reflectionMethod->getDeclaringClass());
?>
```

发帖主题：Re：Колибри0.7.8.0

**程序 2：**

```php
<?php

// Declaring a class
class NidhiSingh {

    // Declaring a protected function
    protected function Author($name) {

        // Displays output
        return 'Nidhi ' . $name;
    }

}

// Creating an object of ReflectionMethod
$reflectionMethod = new ReflectionMethod(new NidhiSingh(), 'Author');

// Calling getDeclaringClass function
var_dump($reflectionMethod->getDeclaringClass());
?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://www.php.net/manual/en/reflectionmethod.getdeclaringclass.php](https://www.php.net/manual/en/reflectionmethod.getdeclaringclass.php)。