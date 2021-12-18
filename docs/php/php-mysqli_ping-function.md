# PHP|mysqli_ping()函数

> Original: [https://www.geeksforgeeks.org/php-mysqli_ping-function/](https://www.geeksforgeeks.org/php-mysqli_ping-function/)

函数的作用是：ping 服务器连接。 也就是说，它用于检查主机是否可以在 IP 网络上访问。 如果现有服务器连接丢失，此功能还会尝试重新连接。 要使用此功能，必须先建立与 MySQL 数据库的连接。

此函数可在面向对象和程序样式中使用，如下所述：

*   **Object oriented style**:

    **语法：**

    ```php
    ping();
    ```

    **参数：**此函数不接受任何参数，它与连接实例一起使用。

    **返回值**：此函数成功时返回 True，失败时返回 False。

    下面的程序以面向对象的方式演示了 ping()函数：

    ```php
    <?php
    $servername = "localhost";
    $username = "username";
    $password = "password";

    // Creating a connection
    $conn = new mysqli($servername, $username, $password);

    // Check connection
    if ($conn->connect_error) {
        die("Connection to the server failed: " . $conn->connect_error);
    } 

    /* check if server is alive */
    if ($conn->ping()) {
        printf ("Successful Coonection!\n");
    } else {
        printf ("Error: %s\n", $conn->error);
    }

    /* close connection */
    $conn->close();
    ?>
    ```

*   **Procedural style**:

    **语法：**

    ```php
    mysqli_ping($conn);
    ```

    **参数：**此函数接受表示要使用的连接的单个参数$conn。

    **返回值**：此函数成功时返回 True，失败时返回 False。

    下面的程序演示了 Procedure 样式中的 mysqli_ping()：

    ```php
    <?php
    $servername = "localhost";
    $username = "username";
    $password = "password";

    // Creating connection
    $conn = mysqli_connect($servername, $username, $password);

    // Checking connection
    if (!$conn) {
        die("Connection to the server failed: " . mysqli_connect_error());
    }

    /* check if server is alive */
    if (mysqli_ping($conn)) {
        printf ("Successful Coonection!\n");
    } else {
        printf ("Error: %s\n", mysqli_error($conn));
    }

    /* close connection */
    mysqli_close($conn);
    ?>
    ```

**参考**：[http://php.net/manual/en/mysqli.ping.php](http://php.net/manual/en/mysqli.ping.php)