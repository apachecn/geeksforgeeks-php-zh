# PHP|Extract()函数

> Original: [https://www.geeksforgeeks.org/php-extract-function/](https://www.geeksforgeeks.org/php-extract-function/)

Extract()函数是 PHP 中的内置函数。 函数的作用是：执行数组到变量的转换。 也就是说，它将数组键转换为变量名，将数组值转换为变量值。 换句话说，我们可以说 Extract()函数将变量从数组导入到[符号表](https://en.wikipedia.org/wiki/Symbol_table)。
**语法**：

```php
*int* extract($input_array, $extract_rule, $prefix)
```

**参数**：Extract()函数接受三个参数，其中一个是必需的，另外两个是可选的。 下面介绍这三个参数：

1.  **$INPUT_ARRAY**：此参数是必需的。 这指定要使用的数组。
2.  **$EXTRACT_RULE**：该参数是可选的。 函数的作用是：检查无效的变量名以及与现有变量名的冲突。 此参数指定如何处理无效和冲突的名称。 此参数可以采用下列值：
    *   EXTR_OVERWRITE：该规则告诉我们，如果发生冲突，则覆盖现有变量。
    *   EXTR_SKIP：该规则告诉我们，如果发生冲突，不要覆盖现有变量。
    *   EXTR_PREFIX_SAME：该规则告诉我们，如果发生冲突，则根据$PREFIX 参数为变量名添加前缀。
    *   EXTR_PREFIX_ALL：该规则根据$PREFIX 参数告知前缀所有变量名。
    *   EXTR_PREFIX_INVALID：该规则告诉我们，根据参数$PREFIX，只有无效/数字变量名的前缀。
    *   EXTR_IF_EXISTS：此规则告诉您，只有在当前符号表中已存在变量时才覆盖该变量，否则不执行任何操作。
    *   EXTR_PREFIX_IF_EXISTS：此规则告诉您，只有在当前符号表中存在相同变量的非前缀版本时，才创建带前缀的变量名。
3.  **$PREFIX**：该参数是可选的。 此参数指定前缀。 前缀自动与数组键之间用下划线字符分隔。 此外，仅当参数$EXTRACT_RULE 设置为 EXTR_PREFIX_SAME、EXTR_PREFIX_ALL、EXTR_PREFIX_INVALID 或 EXTDR_PREFIX_IF_EXISTS 时，才需要此参数。

**返回值**：Extract()函数的返回值是一个整数，表示从数组中成功提取或导入的变量个数。
示例：

```php
Input : array("a" => "one", "b" => "two", "c" => "three")
Output :$a = "one" , $b = "two" , $c = "three"
Explanation: The keys in the input array will become the 
variable names and their values will be assigned to these
new variables.
```

下面的程序说明了 Extract()在 PHP 中的工作方式：
**示例-1**：

## PHP

```php
<?php

    // input array
    $state = array("AS"=>"ASSAM", "OR"=>"ORRISA", "KR"=>"KERELA");

    extract($state);

    // after using extract() function
    echo"\$AS is $AS\n\$KR is $KR\n\$OR is $OR";

?>
```

**输出：**

```php
$AS is ASSAM
$KR is KERELA
$OR is ORRISA
```

**示例-2**：

## PHP

```php
<?php

    $AS="Original";

    $state = array("AS"=>"ASSAM", "OR"=>"ORRISA", "KR"=>"KERELA");

    // handling collisions with extract() function
    extract($state, EXTR_PREFIX_SAME, "dup");

    echo"\$AS is $AS\n\$KR is $KR\n\$OR if $OR \n\$dup_AS = $dup_AS";

?>
```

**输出：1**

```php
$AS is Original
$KR is KERELA
$OR is ORRISA 
$dup_AS = ASSAM
```

**参考**：
[http://php.net/manual/en/function.extract.php](http://php.net/manual/en/function.extract.php)