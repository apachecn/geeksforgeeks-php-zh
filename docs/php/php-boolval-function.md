# PHP | boolval()函数

> 原文:[https://www.geeksforgeeks.org/php-boolval-function/](https://www.geeksforgeeks.org/php-boolval-function/)

boolval()函数是 PHP 中的一个内置函数，它为给定的表达式提供布尔值。

**语法**:

```
*boolean* boolval( $expr )
```

**参数**:该函数只接受一个参数，如上面语法所示，描述如下:

*   **$expr:** 要转换为布尔值的表达式或标量。它可以是字符串类型、整数类型等。

**返回值**:该函数将根据以下条件返回一个布尔值。

*   如果 *$expr* 被评估为布尔真，它将返回真。
*   如果 *$expr* 被评估为布尔假，它将返回假。

以下是不同变量类型及其值的列表，当转换为布尔值时，这些值的计算结果为真或假:

*   **整数**–在本例中 0 为假，其他都为真。
*   **float**–在这个 0.0 中是假的，其他都是真的。
*   **字符串**–“0”和空字符串为假，其他都为真(甚至“0.0”)
*   **数组**–空数组为假，其他都为真
*   **对象**–这里 null 是假的，其他都是真的
*   **null**–null 总是假的。

下面的程序说明了 PHP 中的 boolval()函数:

```
<?php
// PHP program to illustrate 
// the boolval() function

echo 'boolval of 3: '.( boolval( 3 )? 'true' : 'false')."\n";
echo 'boolval of -3    : '.( boolval( -3 )? 'true' : 'false')."\n";
echo 'boolval of 0: ' .( boolval( 0 )? 'true' : 'false')."\n";
echo 'boolval of 3.5: '.( boolval( 3.5 )? 'true' : 'false')."\n";
echo 'boolval of -3.5: '.( boolval( -3.5 )? 'true' : 'false' )."\n";
echo 'boolval of 0.0: '.( boolval( 0.0 )? 'true' : 'false' )."\n";
echo 'boolval of "1": '.( boolval( "1" )? 'true' : 'false' )."\n";
echo 'boolval of "0": '.( boolval( "0" )? 'true' : 'false' )."\n";
echo 'boolval of "0.0": '.( boolval( "0.0" )? 'true' : 'false' )."\n";
echo 'boolval of "xyz": '.( boolval( "xyz" )? 'true' : 'false' )."\n";
echo 'boolval of "": '.( boolval( "" )? 'true' : 'false' )."\n";
echo 'boolval of [1, 5]: '.( boolval( [1, 5] )? 'true' : 'false' )."\n";
echo 'boolval of []: '.( boolval( [] )? 'true' : 'false' )."\n";
echo 'boolval of NULL: '.( boolval( NULL )? 'true' : 'false' )."\n";

?>
```

**输出**:

```
boolval of 3: true
boolval of -3    : true
boolval of 0: false
boolval of 3.5: true
boolval of -3.5: true
boolval of 0.0: false
boolval of "1": true
boolval of "0": false
boolval of "0.0": true
boolval of "xyz": true
boolval of "": false
boolval of [1, 5]: true
boolval of []: false
boolval of NULL: false

```

**参考**:
T3