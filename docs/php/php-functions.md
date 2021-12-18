# PHP|函数

> Original: [https://www.geeksforgeeks.org/php-functions/](https://www.geeksforgeeks.org/php-functions/)

函数是在程序中编写的用于执行某些特定任务的代码块。 我们可以将程序中的功能与现实生活中办公室的员工联系起来，以便更好地理解功能是如何工作的。 假设老板想让他的员工计算年度预算。 那么，这个过程将如何完成呢？ 员工将从老板那里获取有关静态数据的信息，执行计算并计算预算，并将结果显示给老板。 函数的工作方式与此类似。 它们将信息作为参数，执行一组语句或对此参数执行操作并返回结果。
PHP 为我们提供了两种主要类型的函数：

*   **内置函数**：PHP 为我们提供了大量的内置库函数。 这些函数已经以函数的形式进行了编码和存储。 要使用它们，我们只需根据需要调用它们，如 var_dump、fopen()、print_r()、gettype()等。
*   **用户定义函数**：除了内置函数，PHP 允许我们创建我们自己的自定义函数，称为用户定义函数。(
    使用它，我们可以创建我们自己的代码包，并在需要的地方通过简单地调用它来使用它。

**为什么要使用函数？**

*   **可重用性：**如果我们有一个想要在程序的各个部分使用的公共代码，我们可以简单地将其包含在函数中，并在需要时调用它。 这减少了重复单个代码的时间和精力。 这既可以在程序中完成，也可以通过在其他程序中导入包含该函数的 PHP 文件来完成
*   **更容易检测错误：**由于我们的代码分为多个函数，因此我们可以很容易地检测出错误在哪个函数中，并快速轻松地修复它们。
*   **易于维护：**因为我们在程序中使用了函数，所以如果需要更改任何内容或任何一行代码，我们可以很容易地在函数内部进行更改，更改将反映在调用函数的所有位置。 因此，易于维护。

**创建函数**

在创建用户定义函数时，我们需要记住几件事：

1.  任何以左括号和右括号结尾的名称都是函数。
2.  函数名始终以关键字*Function*开头。
3.  要调用一个函数，我们只需在后面加上圆括号写下它的名称
4.  函数名不能以数字开头。 它可以以字母表或下划线开头。
5.  函数名称不区分大小写。

**语法**：↔

```php
function function_name(){
    executable code;
}
```

示例：

## PHP

```php
<?php

function funcGeek()
{
    echo "This is Geeks for Geeks";
}

// Calling the function
funcGeek();

?>
```

输出：0

```php
This is Geeks for Geeks
```

**函数参数或参数**

函数括号内的信息或变量称为参数。 它们用于保存运行时可执行的值。 用户可以随心所欲地接受任意数量的参数，并用逗号(，)操作符分隔。 这些参数用于在运行时接受输入。 当像在函数调用期间那样传递值时，它们被称为参数。 参数是传递给函数的值，参数用于保存这些参数。 通常，参数和实参的含义是相同的。 我们需要记住，对于每个参数，我们都需要传递其相应的参数。
**语法**：

```php
function function_name($first_parameter, $second_parameter) {
    executable code;
}
```

示例：

## PHP

```php
<?php

// function along with three parameters
function proGeek($num1, $num2, $num3)
{
    $product = $num1 * $num2 * $num3;
    echo "The product is $product";
}

// Calling the function
// Passing three arguments
proGeek(2, 3, 5);

?>
```

输出：0

```php
The product is 30
```

**设置功能参数**的默认值

PHP 允许我们为函数参数设置默认参数值。 如果我们没有为具有默认值的参数传递任何实参，则 PHP 将在函数调用中使用此参数的默认设置值。示例：

## PHP

```php
<?php

// function with default parameter
function defGeek($str, $num=12)
{
    echo "$str is $num years old \n";
}

// Calling the function
defGeek("Ram", 15);

// In this call, the default value 12
// will be considered
defGeek("Adam");

?>
```

输出：0

```php
Ram is 15 years old 
Adam is 12 years old
```

在上面的示例中，参数$num 的默认值为 12，如果我们没有在函数调用中传递此参数的任何值，则将考虑此默认值 12。 此外，参数$str 没有默认值，因此它是必需的。

**从函数**返回值

函数还可以将值返回到调用它的程序部分。 关键字*Return*用于将值返回到程序的调用部分。 返回值可以是任何类型，包括数组和对象。 RETURN 语句还标记函数的结束，并在此之后停止执行并返回值。
示例：

## PHP

```php
<?php

// function along with three parameters
function proGeek($num1, $num2, $num3)
{
    $product = $num1 * $num2 * $num3;

    return $product; //returning the product
}

// storing the returned value
$retValue = proGeek(2, 3, 5);
echo "The product is $retValue";

?>
```

输出：0

```php
The product is 30
```

**传递给函数**的参数

PHP 允许我们通过两种方式将参数传递给函数：

*   **按值传递：**使用按值传递参数时，参数的值在函数内更改，但函数外部的原始值保持不变。 这意味着原始值的副本将作为参数传递。
*   **按引用传递：**将参数作为按引用传递时，传递原始值。 因此，原始值会被更改。 在通过引用传递时，我们实际上传递了值的地址，该值是使用与号(&)存储的。

示例：

## PHP

```php
<?php

// pass by value
function valGeek($num) {
    $num += 2;
    return $num;
}

// pass by reference
function refGeek(&$num) {
    $num += 10;
    return $num;
}

$n = 10;

valGeek($n);
echo "The original value is still $n \n";

refGeek($n);
echo "The original value changes to $n";

?>
```

输出：0

```php
The original value is still 10 
The original value changes to 20
```

本文由[**Chinmoy Lenka**](https://auth.geeksforgeeks.org/profile.php?user=lenkachinmoy&list=practice)贡献。 如果你喜欢 GeeksforGeek 并想投稿，你也可以使用[Contribute.geeksforgeeks.org](http://www.contribute.geeksforgeeks.org)写一篇文章，或者把你的文章邮寄到 Contribute@geeksforgeeks.org。 看看你的文章出现在 GeeksforGeek 主页上，并帮助其他 Geek。
如果您发现任何不正确的地方，或者您想分享有关上述主题的更多信息，请写下评论。