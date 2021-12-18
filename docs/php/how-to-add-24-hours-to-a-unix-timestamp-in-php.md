# 如何在 php 中给一个 unix 时间戳加上 24 小时？

> 原文:[https://www . geesforgeks . org/how-add-24-hours-to-a-UNIX-timestamp-in-PHP/](https://www.geeksforgeeks.org/how-to-add-24-hours-to-a-unix-timestamp-in-php/)

Unix 时间戳旨在跟踪从 1970 年 1 月 1 日世界协调时的 Unix 纪元开始的总运行秒数。为了给 Unix 时间戳增加 24 小时，我们可以使用以下任何方法:

**方法 1:** 将 24 小时转换为秒，并将结果添加到当前 Unix 时间。

*   **程序:**

    ```
    <?php 

    echo time() + (24*60*60); 

    ?>
    ```

*   **输出:**

    ```
    1588671070
    ```

**方法 2:** 由于在夏令时(DST)等系统中，一天中的小时数与一天中的 24 小时正好不同。最好使用 **[PHP strtotime()函数](https://www.geeksforgeeks.org/php-strtotime-function/)** 来适当说明这些异常。使用**时间**解析当前日期时间，一天解析时间戳

*   **程序:**

    ```
    <?php 

    echo strtotime("now"), "\n";
    echo strtotime('+1 day'); 

    ?>
    ```

*   **输出:**

    ```
    1588584696
    1588671096
    ```

**方法三:**使用 **DateTime** 类我们可以达到同样的效果。首先用当前时间戳创建一个 DateTime 对象，并添加一天的时间间隔。P1D 表示要添加的 1 天时间间隔。

*   **程序:**

    ```
    <?php 

    // Get current time stamp
    $now = new DateTime();
    $now->format('Y-m-d H:i:s');    
    echo $now->getTimestamp(), "\n";   

    // Add interval of P1D or Period of 1 Day
    $now->add(new DateInterval('P1D'));
    echo $now->getTimestamp();

    ?>
    ```

*   **输出:**

    ```
    1588584729
    1588671129
    ```