# PHP|反射 getModifier()函数

> Original: [https://www.geeksforgeeks.org/php-reflection-getmodifiers-function/](https://www.geeksforgeeks.org/php-reflection-getmodifiers-function/)

函数是 PHP 中的内置函数，用于返回指定修饰符名称的数组。

**语法：**

```
*int* Reflection::getModifiers( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回指定类的访问修饰符的位域。

下面的程序说明了 PHP 中的 Reflation：：getModifier()函数：

**程序 1：**

```
<?php

// Declaring a class Testing
class Testing { 

    // Calling a function GeeksforGeeks() with
    // two modifier named as public and static
    public static function GeeksforGeeks()
    {
        return;
    }
}

// ReflectionMethod is called on the class Testing and
// their member as function GeeksforGeeks()
$GeeksforGeeks = new ReflectionMethod('Testing', 'GeeksforGeeks');

// Calling the getModifiers() function and printing
// an array of modifiers
echo implode(' ', Reflection::getModifierNames(
                $GeeksforGeeks->getModifiers()));
?>
```

**输出：**

```
public static

```

**程序 2：**

```
<?php

// Declaring a class Departments
class Departments { 

    // Calling some function with
    // different modifiers
    public function IT() {
        return;
    }
    final public function CSE() {
        return;
    }
    private function ECE() {
        return;
    }
}

// ReflectionMethod is called on the above class
// with their members
$A = new ReflectionMethod('Departments', 'IT');
$B = new ReflectionMethod('Departments', 'CSE');
$C = new ReflectionMethod('Departments', 'ECE');

// Calling the getModifiers() function and printing
// an array of modifiers
echo implode(' ', Reflection::getModifierNames(
                  $A->getModifiers())). "\n";
echo implode(' ', Reflection::getModifierNames(
                  $B->getModifiers())). "\n";
echo implode(' ', Reflection::getModifierNames(
                  $C->getModifiers())). "\n";
?>
```

**输出：**

```
public
final public
private

```

**引用：**[https://secure.php.net/manual/en/reflectionclass.getmodifiers.php](https://www.php.net/manual/en/reflectionclass.getmodifiers.php)