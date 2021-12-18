# PHP|反射 getModifierNames()函数

> Original: [https://www.geeksforgeeks.org/php-reflection-getmodifiernames-function/](https://www.geeksforgeeks.org/php-reflection-getmodifiernames-function/)

**Reflation：：getModifierNames()函数**是 PHP 中的内置函数，用于返回指定修饰符名称的数组。

**语法：**

```
*array* Reflection::getModifierNames( *int* $modifiers )
```

**参数：**此函数接受单个参数**$修饰符**，它是修饰符的位域。 这里，位字段是由多个相邻的计算机存储器位置组成的数据结构。
**返回值：**此函数返回指定修饰符名称的数组。
下面的程序说明 PHP：
**程序 1：**中的反射：：getModifierNames()函数

## PHP

```
<?php

// Declaring a class Testing
class Testing
{

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

// Calling the getModifierNames() function and printing
// an array of modifier names
echo implode(' ', Reflection::getModifierNames($GeeksforGeeks->getModifiers()));
?>
```

**Output:** 

```
public static
```

**程序 2：**

## PHP

```
<?php

// Declaring a class Testing
class Testing
{

    // Calling a function GFG() with
    // two modifier named as public and static
    final public function GFG()
    {
        return;
    }
}

// ReflectionMethod is called on the class Testing and
// their member as function GFG()
$GFG = new ReflectionMethod('Testing', 'GFG');

// Calling the getModifierNames() function and printing
// an array of modifier names
echo implode(' ', Reflection::getModifierNames($GFG->getModifiers()));
?>
```

**Output:** 

```
final public
```

**引用：**[https://www.php.net/manual/en/reflection.getmodifiernames.php](https://www.php.net/manual/en/reflection.getmodifiernames.php)