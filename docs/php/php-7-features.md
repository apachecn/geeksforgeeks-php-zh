# PHP 7 |功能

> 原文:[https://www.geeksforgeeks.org/php-7-features/](https://www.geeksforgeeks.org/php-7-features/)

PHP7 中增加了许多特性。PHP7 发布后，网站性能提升了 25-70%。现在我们将通过示例逐一讨论 PHP7 的特性。

**标量数据类型提示:**标量数据类型有布尔型、整数型、浮点型和字符串型。之前我们无法对标量数据类型进行类型提示。我们在做数组或类对象的提示。

**示例:**

```php
<?php 
ini_set('display_errors', '1');

class User{}

function test(User $abc) {
    var_dump($abc);
}

test(new User);
?>
```

**输出:**

```php
object(User)#1 (0) {
}
```

现在让我们看看如何为 Php7 中可用的标量数据类型进行类型提示

```php
<?php 
ini_set('display_errors','1');

class User{} 

function add(int $a, int $b) {
    return $a + $b;
}

echo add(3, '34');
?>
```

**输出:**

```php
37
```

我们在第二个参数字符串‘34’中传递一个字符串，但是我们在这里得到的输出是 34 和 3 的相加，即 37，因为这里严格模式被禁用。现在，如果您想要限制这一点，您需要在文件的顶部给出一个声明。
**例:**

```php
<?php 
declare(strict_types = 1);
ini_set('display_errors','1');

class User{} 

function add(int $a, int $b) {
    return $a + $b;
}

echo add(3, '34');
?>
```

**输出:**

```php
Fatal error: Uncaught TypeError: Argument 2 passed to add() must be of the type integer,
string given, called in /home/cg/root/5012177/main.php on line 11 and defined 
in /home/cg/root/5012177/main.php:7
Stack trace:
#0 /home/cg/root/5012177/main.php(11): add(3, '34')
#1 {main}
  thrown in /home/cg/root/5012177/main.php on line 7
PHP Fatal error:  Uncaught TypeError: Argument 2 passed to add() must be of the type integer,
string given, called in /home/cg/root/5012177/main.php on line 11 and defined 
in /home/cg/root/5012177/main.php:7
Stack trace:
#0 /home/cg/root/5012177/main.php(11): add(3, '34')
#1 {main}
  thrown in /home/cg/root/5012177/main.php on line 7

```

现在让我们看看布尔型的例子。下面是布尔数据类型的代码。
**例:**

```php
<?php 
declare(strict_types = 1);
ini_set('display_errors','1');

class User{} 

function isBoolean(bool $a) {
    var_dump($a);
}

isBoolean(true);
?>
```

**输出:**

```php
bool(true)
```

**返回类型声明:**在 C 或 C++中，定义将从函数返回的值的数据类型。现在我们将看到如何在 Php7 中做到这一点。
T3】例:

```php
<?php 

declare(strict_types = 1);
ini_set('display_errors','1');

function test(): array {
    return[];
}

var_dump(test());
?>
```

**输出:**

```php
array(0) {
}
```

在上例中声明一个函数后，需要给数据类型使用:然后在函数测试中返回相同的数据类型数组()。

**空合并运算符:**空合并运算符是？?"。这个运算符基本上取代了三元运算符。之前我们使用了如下的三元运算符…

```php
<?php 
declare(strict_types = 1);
ini_set('display_errors','1');

$name = isset($_GET['name']) ? $_GET['name'] : 'Not Found';
var_dump($name);
?>
```

**输出:**

```php
string(9) "Not Found"
```

现在使用？?'我们可以缩短代码。
**例:**

```php
<?php 
declare(strict_types = 1);
ini_set('display_errors','1');

$name = $_GET['name'] ?? 'Not Found';
var_dump($name);
?>
```

**输出:**

```php
string(9) "Not Found"
```

**摸索导入和命名空间:**之前我们要定义多个命名空间和类，使用或者导入一个类从一个命名空间到另一个命名空间的时候使用了‘use’关键字，然后我们要给命名空间加上需要导入的类名。
T3】例:

```php
<?php 

namespace Course {
    class BTech {
    }

    class MTech {
    }
}

namespace Course\Branch {

     // CSE is in both Course
     // BTech and MTech
     class CSE {
     }   
}

namespace App {
      use Course\BTech;
      use Course\MTech;
      use Branch\CSE;
      var_dump(new BTech());
      var_dump(new MTech());
}

?>
```

**输出:**

```php
object(Course\BTech)#1 (0) {
}
object(Course\MTech)#1 (0) {
}
```

在上面的示例中，导入了两个类，但是如果需要从一个命名空间到另一个命名空间使用多个类，该怎么办。它必须编写多行“use”语句来定义每一个类，这会使代码变得冗长。所以在 PHP7 中针对这个问题引入了分组导入。让我们看看上面的例子如何在分组导入和嵌套命名空间的帮助下工作。
**例:**

```php
<?php 

namespace Course {
    class BTech {
    }

    class MTech {
    }
}

namespace Course\Branch {

     // CSE is in both Course BTech and MTech
     class CSE {
     }   
}

namespace App {

      use Course\{
          BTech,
          MTech,
          Branch\CSE
      };

      var_dump(new BTech());
      var_dump(new MTech());
      var_dump(new CSE());
}

?>
```

**输出:**

```php
object(Course\BTech)#1 (0) {
}
object(Course\MTech)#1 (0) {
}
object(Course\Branch\CSE)#1 (0) {
}
```

因此，分组导入将减少代码，并且更加易读和方便。

**组合比较/飞船算符:**组合比较算符是三个算符的组合。这些运算符小于、大于和等于。三次操作员运行的组合和输出将根据结果而变化。现在让我们举一个这个运算符的例子。

**示例:**

```php
<?php 

$arr = ['welcome' ,'to' , 'geeksforgeeks'];

usort($arr, function($a, $b) {
    return strlen($a) <=> strlen($b); 
});

var_dump($arr);

?>
```

**输出:**

```php
array(3) {
  [0]=>
  string(2) "to"
  [1]=>
  string(7) "welcome"
  [2]=>
  string(13) "geeksforgeeks"
}
```

在上面的例子中，我们比较了定义在数组中的单词的长度，并按升序对其进行排序。usort()是一个 PHP 预构建的函数，其中传递一个数组作为第一个参数，第二个参数是用户定义的函数，这意味着您自己的自定义逻辑函数。通过此链接[了解更多关于 usort()函数的信息。因此，我们可以使用宇宙飞船或组合运算符来完成相同的任务，而不是手动使用 if 和 else。](https://www.w3schools.com/php/func_array_usort.asp)

**匿名类:** PHP7 引入了匿名类，现在的问题是什么时候使用？当你只使用一个类一次，并且你不希望它再次被实例化。首先让我们看看我们通常如何创建一个类和对象。

**示例:**

```php
<?php 
class test {
  function hiGeeks() {
      echo "geeksforgeeks";
  }
}

$sayGeeks = new test;
$sayGeeks->hiGeeks();
?>
```

**输出:**

```php
geeksforgeeks
```

现在让我们看看如何创建一个匿名类。
**例:**

```php
<?php 
$anonymous = new class {
  private $readme  = "Welcome to geeksforgeeks";
  function printOut() {
    echo $this->readme;
  }
};
$anonymous -> printOut();
?>
```

**输出:**

```php
Welcome to geeksforgeeks
```

这里我们可以为这个类创建一个对象，但是我们可以扩展另一个类。
**例:**

```php
<?php 
class test {
    function hiGeeks() {
        echo "geeksforgeeks ";
    }
}

$sayGeeks = new test;
$sayGeeks->hiGeeks();

$anonymous = new class extends test{
    private $readme  = "Welcome to geeksforgeeks";
    function printOut() {
        echo $this->readme;
    }
};

$anonymous -> printOut();
$anonymous -> hiGeeks();
?>
```

**输出:**

```php
geeksforgeeks Welcome to geeksforgeeksgeeksforgeeks
```

**闭包::call()方法:** PHP7 引入了一个新的方法调用()，这是一种在将对象范围绑定到闭包的同时调用闭包的简写方式。在 JavaScript 中，大多数时候我们使用闭包，也就是匿名函数，在 PHP 5 中，我们也使用闭包，但是在 PHP7 中，我们以不同的方式使用它。
T3】例:

```php
<?php 

class User {
    private $username;
     private $email;

public function __construct($username, $email) {
        $this->username = $username;
        $this->email= $email;
    }
}

$getUserEmail = function() {
    return $this->username. ' email address is '.$this->email;
};

$user = new User('abc','abc@gmail.com');

// Using PHP5 
$email = $getUserEmail->bindTo($user, 'User');
echo $email().'  ';

// Using PHP7
echo $getUserEmail->call($user);
?>
```

**输出:**

```php
abc email address is abc@gmail.com  abc email address is abc@gmail.com
```

所以调用()方法使我们的代码更加干净和易于使用。

**生成器:**用 Php 编程变得更加强大，因为引入了一些新的特性，比如生成器的“返回”和其中的收益。我们将在 PHP7 中看到它的层次是如何工作的。
T3】例:

```php
<?php 

function values() {
    yield 200;
    yield 300;
    return 500;
}

$control = values();

foreach ($control as $value) {
    echo '<br>'. $value;
}

echo '<br>'. $control->getReturn();

?>
```

**输出:**

```php

200
300
500
```

在上面的例子中，为了得到收益值，我们使用 foreach 循环，为了得到返回值，我们使用 getReturn()。这里我们需要注意秩序，以获得收益和回报的价值。如果我们改变订单，我们会得到一个错误。
**例:**

```php
<?php 

function values() {
    yield 200;
    yield 300;
    return 500;
}

$control = values();

echo '<br>'. $control->getReturn();

foreach ($control as $value) {
    echo '<br>'. $value;
}

?>
```

**输出:**

```php
PHP Fatal error:  Uncaught Exception: Cannot get return value of a generator that
hasn't returned in /home/cg/root/6474693/main.php:14
Stack trace:
#0 /home/cg/root/6474693/main.php(14): Generator->getReturn()
#1 {main}
  thrown in /home/cg/root/6474693/main.php on line 14

```

所以在上面的例子中，我们试图先得到返回值，然后给出一个错误。同样在 PHP7 中，它允许从另一个生成器函数屈服。我们可以编写几个生成器函数，您可以允许它们链接到另一个。

**示例:**

```php
<?php 

function values() {

    yield from Gen2();

    yield 300;

    return 500;
}

function Gen2() {

    yield 'This is from Gen2';

    yield 'This is from Gen200';

    yield from Gen3();
}

function Gen3() {

    yield 'This is from Gen3';

    yield 'This is from Gen300';
}

$control = values();

foreach ($control as $value) {

    echo '<br>'. $value;
}

echo '<br>'. $control->getReturn();

?>
```

**输出:**

```php

This is from Gen2
This is from Gen200
This is from Gen3
This is from Gen300
300
500
```

**错误处理:**错误和异常实现可抛出接口。我们可以使用 try/catch 块来处理错误对象和异常。

1.  **类型错误:**当特定类型的错误与类型声明不匹配时，会出现此错误。
2.  **解析错误:**当代码或包含文件中有语法错误时，会出现此错误。
3.  **断言错误:**当不满足断言设置的条件时，会出现此错误。

在 PHP7 中，我们可以用一种优雅的方式处理错误，无论何时发生异常，我们都可以抛出异常。Php7 之前的致命错误不会调用错误处理程序并停止脚本，也不能正确关闭资源。让我们看看可投掷界面。

```php
interface Throwable
{
    public function getMessage(): string;
    public function getCode(): int;
    public function getFile(): string;
    public function getLine(): int;
    public function getTrace(): array;
    public function getTraceAsString(): string;
    public function getPrevious(): Throwable;
    public function __toString(): string;
}

```

下面是如何在 try/catch 块中使用 Throwable 的语法。

```php
try {
  // Code
}catch(Throwable $e) {
  // Exceptions or Error handling
}

```

1.  **Fatal Error Handling:** Below is the example for handling fatal error in a more elegant way and we will also see how to close the resources properly.

    **示例:**

    ```php
    <?php 

    class User {

        public function __construct() {
            echo 'User Construct...<br>';
        }

        public function __destruct() {
           echo 'User Destruct...<br>'; 
        }

    }

    function run($object) {
        $object->hello();
    }

    try {
        $user = new User();
        run(null);

    // Use Error instead of exception to
    // generate custom error message    
    } catch (Error $e) {
        echo '<strong>Error on Line: '.$e->getLine().' in '
            .$e->getFile().'</strong>'. $e->getMessage().'<br>';
    } finally {
        echo 'Finally Ran...<br>';
    }

    ?>
    ```

    **输出:**

    ```php
    User Construct...
    Error on Line: 16 in /home/cg/root/6474693/main.php
    Call to a member function hello() on null
    Finally Ran...
    User Destruct...

    ```

    这是我们如何处理致命错误，我们可以关闭我们的资源，也可以创建自定义消息。如果我们在像“catch (Exception $e)”这样的 catch 块中使用“Exception”而不是“Error”，我们将不会从我们的终端获得我们已经创建的正确消息，所以使用 Error 而不是 Exception。

2.  **Type Error and Parse Error Handling:** We can handle the type errors and parse errors much like in a similar way like we did for fatal error. Let’s see first how to handle **type error**. Below is the example where we are trying to get the some of two integers and we are doing type hinting.

    **示例:**

    ```php
    <?php 

    class User {

        public function __construct() {
            echo 'User Construct...<br>';
        }

        public function __destruct() {
           echo 'User Destruct...<br>'; 
        }

    }

    function sum(int $num1, int $num2) {
        return $num1 + $num2;
    }

    try {
        $user = new User();
        echo sum('Test', 2);
    } catch(Exception $e) {
        echo $e->getMessage();
    } catch(Error $e) {
        echo '<strong>'.get_class($e). 'on line '.
            $e->getLine().':</strong>'.$e->getMessage().'<br>';
    }

    ?>
    ```

    **输出:**

    ```php

    User Construct...
    TypeError on line 15:Argument 1 passed to sum() must be
    of the type integer, string given, called in /home/cg/root/4010040/main.php on line 21
    User Destruct...

    ```

    在上面的例子中，我们传递了一个字符串和一个整数，由于在我们的函数中使用了类型提示，这给我们带来了类型错误。从上面的例子中，我们可以正确地处理错误，即使我们有错误，我们也可以关闭资源。我们使用不同的函数，如 get_class()、getLine()、getMessage()以最优雅的方式处理错误。

    现在我们举个例子来处理**解析错误**。下面是由于文件中的语法错误而导致我们收到错误的代码。

    **示例:**

    ```php
    <?php 

    class User {    
        public function __construct() {
            echo 'User Construct...<br>';
        }

        public function __destruct() {
           echo 'User Destruct...<br>'; 
        }

    }

    function sum(int $num1, int $num2) {
        return $num1 + $num2;
    }

    try {
        $user = new User();

        // Syntax error for var_dump in below line
        $result = eval("var_dup(1);");
    } catch(Exception $e) {
        echo $e->getMessage();
    } catch(Error $e) {
        echo '<strong>'.get_class($e). ' on line '.$e->getLine()
            .':</strong>'.$e->getMessage().'<br>';
    }

    ?>
    ```

    **输出:**

    ```php

    User Construct...
    Error on line 1:Call to undefined function var_dup()
    User Destruct...

    ```

**整数除法函数:** PHP7 引入了 intdiv()函数，该函数取两个参数，一个是被除数，一个是除数。结果将是除法结果为 int。
T3】例:

```php
<?php
   $value = intdiv(13,4);
   var_dump($value);
   echo $value;
?>
```

**输出:**

```php
int(3)
3
```