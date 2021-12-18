# PHP|ReflectionMethod export()函数

> Original: [https://www.geeksforgeeks.org/php-reflectionmethod-export-function/](https://www.geeksforgeeks.org/php-reflectionmethod-export-function/)

**ReflectionMethod：：Export()函数**是 PHP 中的一个内置函数，用于在返回参数设置为 true 时以字符串形式返回导出，否则返回 NULL。

**语法：**

```
*string* ReflectionMethod::export ( *$class, $name, $return* )
```

**参数：**此函数接受上述三个参数，如下所述：

*   **class：**这是初始化的类的名称。
*   **名称：**这是方法的名称。
*   **返回：**其值为 TRUE 或 FALSE。 使用 TRUE 将返回导出，而使用 FALSE 则相反。

**返回值：**如果返回参数已设置为 true，则此函数以字符串形式返回导出，否则返回 NULL。

以下程序说明 PHP：
**Program_1：**中的**ReflectionMethod：：Export()函数**

```
<?php

// Initializing a user-defined class
class Company {

    protected function GeeksforGeeks($name) {
        return 'GFG' . $name;
    }
}

// Using ReflectionMethod() over the class Company
$A = new ReflectionMethod(new Company(), 'GeeksforGeeks');

// Calling the export() function
$B = $A->export( 'Company', 'GeeksforGeeks', $return = TRUE );

// Getting the the export as a string if the 
// return parameter has been set to TRUE, 
// otherwise NULL is returned.
var_dump($B);
?>
```

发帖主题：Re：Колибри0.7.0

```
string(171) "Method [ <user> protected method GeeksforGeeks ] {
  @@ /home/cd1a603457d3beda20350155354b4363.php 6 - 8

  - Parameters [1] {
    Parameter #0 [ <required> $name ]
  }
}
"
```

**程序 _2：**

```
<?php

// Initializing some user-defined classes
class Department1 {

    protected function HR($name) {
        return 'hr' . $name;
    }
}
class Department2 {

    protected function Coding($name) {
        return 'coding' . $name;
    }
}
class Department3 {

    protected function Marketing($name) {
        return 'marketing' . $name;
    }
}

// Using ReflectionMethod() over the above classes
$A = new ReflectionMethod(new Department1(), 'HR');
$B = new ReflectionMethod(new Department2(), 'Coding');
$C = new ReflectionMethod(new Department3(), 'Marketing');

// Calling the export() function and 
// Getting the the export as a string if the 
// return parameter has been set to TRUE, 
// otherwise NULL is returned.
var_dump($A->export( 'Department1', 'HR', $return = TRUE ));
var_dump($B->export( 'Department2', 'Coding', $return = FALSE ));
var_dump($C->export( 'Department3', 'Marketing', $return = FALSE ));
?>
```

发帖主题：Re：Колибри0.7.0

```
string(160) "Method [ <user> protected method HR ] {
  @@ /home/b1fa43e2f382f32d60abd4370db4a4f6.php 6 - 8

  - Parameters [1] {
    Parameter #0 [ <required> $name ]
  }
}
"
Method [ <user> protected method Coding ] {
  @@ /home/b1fa43e2f382f32d60abd4370db4a4f6.php 12 - 14

  - Parameters [1] {
    Parameter #0 [ <required> $name ]
  }
}

NULL
Method [ <user> protected method Marketing ] {
  @@ /home/b1fa43e2f382f32d60abd4370db4a4f6.php 18 - 20

  - Parameters [1] {
    Parameter #0 [ <required> $name ]
  }
}

NULL

```

**引用：**[https://www.php.net/manual/en/reflectionmethod.export.php](https://www.php.net/manual/en/reflectionmethod.export.php)