# PHP|向上或向下移动(键、值)对的程序

> Original: [https://www.geeksforgeeks.org/php-program-move-keyvalue-pair-upwards-downwards/](https://www.geeksforgeeks.org/php-program-move-keyvalue-pair-upwards-downwards/)

**给定一个具有键、值对的数组，我们需要使用键向上或向下移动特定值。**

例如：

```php
Input : $continents = array(
                      'First' => 'Asia',
                      'Second' => 'Europe',
                      'Third' => 'North America',
                      'Fourth' => 'South America',
                            );
        move_to_up($continents, 'Third');
Output : Array
(
    [Third] => North America
    [First] => Asia
    [Second] => Europe
    [Fourth] => South America
)

Input :$continents = array(
                      'First' => 'Asia',
                      'Second' => 'Europe',
                      'Third' => 'North America',
                      'Fourth' => 'South America',
                            );
       move_to_bottom($continents, 'Second');
Output : Array
(
    [First] => Asia
    [Third] => North America
    [Fourth] => South America
    [Second] => Europe
)

```

上述问题可以使用下面介绍的 PHP 函数来解决：
**unset()：**该函数销毁指定的变量。

**方法：**我们准备一个带有指定键(要上移或下移的值)的临时数组，然后根据将值上移或下移的目的来取消设置该键，最后追加该键。

下面是方法
**代码 1 的实现：**在顶部移动键、值

```php
<?php

        $continents = array(
                      'First' => 'Asia',
                      'Second' => 'Europe',
                      'Third' => 'North America',
                      'Fourth' => 'South America',
                            );

        move_to_up($continents, 'Third');
        print_r ($continents);

function move_to_up(&$continents, $string)
       {
           $var = array($string => $continents[$string]);
           unset($continents[$string]);
           $continents = $var + $continents;
       }
?>
```

产出：

```php
Array
(
    [Third] => North America
    [First] => Asia
    [Second] => Europe
    [Fourth] => South America
)

```

**代码 2：**移动键，值在底部

```php
<?php

        $continents = array(
                      'First' => 'Asia',
                      'Second' => 'Europe',
                      'Third' => 'North America',
                      'Fourth' => 'South America',
                            );
       move_to_bottom($continents, 'Second');
       print_r ($continents);

 function move_to_bottom(&$continents, $string)
       {
           $var = array($string => $continents[$string]);
           unset($continents[$string]);
           $continents = $continents + $var;
       }

?>
```

产出：

```php
Array
(
    [First] => Asia
    [Third] => North America
    [Fourth] => South America
    [Second] => Europe
)

```