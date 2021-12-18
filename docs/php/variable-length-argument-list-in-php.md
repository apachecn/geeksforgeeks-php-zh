# PHP 中的变长参数列表

> 原文:[https://www . geesforgeks . org/变长参数列表-in-php/](https://www.geeksforgeeks.org/variable-length-argument-list-in-php/)

给定一组目前长度未知的参数，我们将看到一个函数如何处理这些未知数量的参数，这些参数的数量将根据需求而变化。

我们将一个接一个地讨论每个单词，以深入理解我们正在处理的主题。

*   **变量:**是参数个数不断变化。
*   **长度:**指参数个数。
*   **参数:**指传递给函数的输入。

现在，兴趣点在于单词列表，调用时传递的所有参数都将作为数组传递给函数。这些值将像从数组中检索一样被检索。

**访问变量参数方法:**在这种情况下，函数接受变量参数并相应地工作。必须有多个参数的变量用“…”(三点)声明。

*   **例:**

    ```
    <?php
    function sum(...$numbers) {
      $res = 0;
      foreach($numbers as $n) {
          $res+=$n;
        }
      return $res;
    }

    echo(sum(1,2,3,4)."\n");
    echo(sum(5,6,1));
    ?>
    ```

*   **输出:**

    ```
    10 
    12
    ```

**提供变量参数方法:**在调用函数将数组或可遍历变量或文字解包到参数列表中时，也可以使用“…”(三点)。

*   **例:**

    ```
    <?php
    function add($a,$b) {
      return $a + $b ;
    }
    echo add(...[1, 2])."\n";

    $a = [1, 2];
    echo add(...$a);
    ?>
    ```

*   **输出:**

    ```
    3
    3

    ```

**类型提示变量参数方法:**也可以在…标记前添加一种类型的提示。如果存在，那么…捕获的所有参数都必须是暗示类的对象。

*   **例:**

    ```
    <?php
    function total_intervals($unit, DateInterval ...$intervals) {
        $time = 0;
        foreach ($intervals as $interval) {
            $time += $interval->$unit;
        }
        return $time;
    }

    $a = new DateInterval('P1D');
    $b = new DateInterval('P2D');
    echo total_intervals('d', $a, $b).' days';

    ?>
    ```

*   **输出:**

    ```
     3 days
    ```