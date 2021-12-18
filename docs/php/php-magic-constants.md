# PHP|魔术常数

> Original: [https://www.geeksforgeeks.org/php-magic-constants/](https://www.geeksforgeeks.org/php-magic-constants/)

**幻常量：**幻常量是 PHP 中的预定义常量，根据使用情况使用。 这些常量由各种扩展创建。 PHP 中有九个神奇常量，所有常量都是在编译时解析的，与在运行时解析的常规常量不同。 有八个以双下划线(__)开头和结尾的魔术常量。
下面列出了所有常量，示例代码如下：

**1.__line__：**这个魔术常量返回文件的当前行号。 如果您在程序文件中的某个地方使用了这个神奇常量，那么这个常量将在编译时显示行号。

**语法：**

```php
.__line__
```

**示例：**

## PHP

```php
<?php

echo "The Line number is : ". __line__;

?>
```

发帖主题：Re：Колибри0.7.0

```php
The Line number is : 3
```

**2.__file__：**此魔术常量返回已执行文件的完整路径和文件名。

**语法：**

```php
.__file__
```

**示例：**

## PHP

```php
<?php

echo "The file name is : ". __file__;

?>
```

发帖主题：Re：Колибри0.7.0

```php
The file name is : /home/3d27a639c57aaed9efa5880e613bc273.php
```

**3.__dir__：**这个魔术常量返回执行文件的目录。

**语法：**

```php
.__dir__
```

**示例：**

## PHP

```php
<?php

echo "The directory is : ". __dir__;

?>
```

发帖主题：Re：Колибри0.7.0

```php
The directory is : /home
```

**4.__Function__：**此幻数返回包含此幻数的函数的名称。

**语法：**

```php
.__function__
```

**示例：**

## PHP

```php
<?php
function Geeks(){
    echo "The function name is : ". __function__;
}
Geeks();
?>
```

发帖主题：Re：Колибри0.7.0

```php
The function name is : Geeks
```

**5.__class__：**此幻数返回包含此幻数的类名。

**语法：**

```php
__class__
```

**示例：**

## PHP

```php
<?php
class Geeks
{
    public function getClassName(){
        return __class__;
    }
}
$obj = new Geeks();
echo $obj->getClassName();
?>
```

发帖主题：Re：Колибри0.7.0

```php
Geeks 
```

**6.__method__：**此幻数返回包含此幻数的方法名。

**语法：**

```php
__method__
```

**示例：**

## PHP

```php
<?php
class Company
{
    public function GeeksforGeeks(){
        return __method__;
    }
}
$obj = new Company();
echo  $obj->GeeksforGeeks();
?>
```

发帖主题：Re：Колибри0.7.0

```php
Company::GeeksforGeeks 
```

**7.__NAMESPACE__：**此幻数返回包含此幻数的当前命名空间。

**语法：**

```php
__namespace__
```

**示例：**

## PHP

```php
<?php
namespace GeeksforGeeks;

class Company {
    public function gfg() {
        return __namespace__;
    }
}

$obj = new Company();
echo  $obj->gfg();

?>
```

发帖主题：Re：Колибри0.7.0

```php
GeeksforGeeks
```

**8.__ 特征 __：**此魔术常量返回包含此魔术常量的特征名称。

**语法：**

```php
__trait__
```

**示例：**

## PHP

```php
<?php
trait GeeksforGeeks{ 
    function gfg(){ 
        echo __trait__; 
        } 
    } 
    class Company{ 
        use GeeksforGeeks; 
        } 
    $a = new Company; 
    $a->gfg(); 
?>
```

发帖主题：Re：Колибри0.7.0

```php
GeeksforGeeks 
```

**9.ClassName：：Class：**这个神奇常量返回完全限定的类名。

**语法：**

```php
ClassName::class
```

**示例：**

## PHP

```php
<?php

namespace Computer_Sciecnec_Portal;
class Geeks{ }

echo Geeks::class;//Classname::class

?>
```

发帖主题：Re：Колибри0.7.0

```php
Computer_Sciecnec_Portal\Geeks 
```

**引用：**[https://www.php.net/manual/en/language.constants.predefined.php](https://www.php.net/manual/en/language.constants.predefined.php)