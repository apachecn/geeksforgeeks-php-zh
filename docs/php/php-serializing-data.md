# PHP|序列化数据

> Original: [https://www.geeksforgeeks.org/php-serializing-data/](https://www.geeksforgeeks.org/php-serializing-data/)

大多数情况下，我们需要将**复数组**存储在数据库中或 PHP 的文件中。 我们中的一些人可能肯定已经在寻找一些内置函数来完成这项任务。 复数组是具有多个数据类型或数组的元素的数组。
但是，我们已经有了一个方便的解决方案来处理这种情况。 我们不必编写自己的函数来将复杂数组转换为格式化字符串。 序列化变量有两种流行的方法。

*   _
*   _ 取消序列化()_

我们可以使用 Serialize()函数序列化 PHP 中的任何数据。 Serialize()函数接受单个参数，即我们想要序列化的数据，并返回序列化的字符串。 下面的程序说明了这一点：

```
<?php

// a complex array
$myvar = array(
    'hello',
    42,
    array(1, 'two'),
    'apple'
);

// convert to a string
$string = serialize($myvar);

// printing the serialized data
echo $string;

?>
```

产出：

```
a:4:{i:0;s:5:"hello";i:1;i:42;i:2;a:2:{i:
0;i:1;i:1;s:3:"two";}i:3;s:5:"apple";}

```

从上面的代码中，我们有一个包含序列化数据的变量*$string*。 我们可以使用**unSerialize()**函数对变量的值进行反序列化，以返回到**复杂数组**、*$myvar*的原始值。

下面的程序演示了 Serialize()和 UnSerialize()函数：

```
<?php

// a complex array
$myvar = array(
    'hello',
    42,
    array(1, 'two'),
    'apple'
);

// serialize the above data
$string = serialize($myvar);

// unserializing the data in $string
$newvar = unserialize($string);  

// printing the unserialized data 
print_r($newvar);

?>
```

产出：

```
Array
(
    [0] => hello
    [1] => 42
    [2] => Array
        (
            [0] => 1
            [1] => two
        )

    [3] => apple
)

```

这是原生 PHP 序列化方法。 然而，由于**JSON**在最近几年变得如此流行，他们决定在 PHP5.2 中添加对它的支持。 现在，您还可以使用**json_encode()**和**json_decode()**函数分别在 PHP 中序列化和反序列化数据。

因为**JSON**格式是纯文本的，所以它可以很容易地发送到服务器和从服务器发送，并且可以作为任何编程语言的数据格式使用。

让我们看看如何在 PHP 中使用**json_encode()**：

```
<?php

// a complex array
$myvar = array(
    'hello',
    42,
    array(1, 'two'),
    'apple'
);

// serializing data
$string = json_encode($myvar);

// printing the serialized data
echo $string;

?>
```

产出：

```
["hello",42,[1,"two"],"apple"]

```

我们可以使用 json_decode()函数对上面程序中编码的数据进行解码，以获得原始的复数组。 下面的程序说明了这一点：

```
<?php

// a complex array
$myvar = array(
    'hello',
    42,
    array(1, 'two'),
    'apple'
);

// serializing data
$string = json_encode($myvar);

// decoding the above encoded string
$newvar = json_decode($string);

// printing the decoded data  
print_r($newvar);

?>
```

产出：

```
Array
(
    [0] => hello
    [1] => 42
    [2] => Array
        (
            [0] => 1
            [1] => two
        )

    [3] => apple
)

```

**注**：JSON 编码和解码更加紧凑，最重要的是，它与 javascript 和许多其他语言兼容。 但是，对于复杂对象，某些信息可能会丢失。