# PHP|会话

> Original: [https://www.geeksforgeeks.org/php-sessions/](https://www.geeksforgeeks.org/php-sessions/)

**什么是会话？**

通常，会话是指两个介质之间通信帧。 PHP 会话用于将数据存储在服务器上，而不是用户的计算机上。 会话标识符或 SID 是唯一的数字，用于标识基于会话的环境中的每个用户。 SID 用于将用户与他在服务器上的信息(如帖子、电子邮件等)联系起来。

**会话如何比 cookie 更好？**

虽然 Cookie 也用于存储与用户相关的数据，但它们存在严重的安全问题，因为 Cookie 存储在用户的计算机上，因此很容易被攻击者修改 Cookie 的内容。攻击者在 Cookie 中添加有害数据可能会导致应用程序崩溃。
除了 Cookie 会影响站点的性能之外，因为 Cookie 会在用户每次查看页面时发送用户数据。每次浏览器向服务器请求 URL 时，该网站的所有 Cookie 数据都会在请求中自动发送到服务器。

以下是 PHP 会话中涉及的不同步骤：

*   **Starting a PHP Session**: The first step is to start up a session. After a session is started, session variables can be created to store information. The PHP **session_start()** function is used to begin a new session.It als creates a new session ID for the user.

    以下是启动新会话的 PHP 代码：

    ```
    <?php

    session_start();

    ?>
    ```

*   **Storing Session Data**: Session data in key-value pairs using the **$_SESSION[]** superglobal array.The stored data can be accessed during lifetime of a session.

    下面是用两个会话变量 Rollnumber 和 Name 存储会话的 PHP 代码：

    ```
    <?php

    session_start();

    $_SESSION["Rollnumber"] = "11";
    $_SESSION["Name"] = "Ajay";

    ?>
    ```

*   **Accessing Session Data**: Data stored in sessions can be easily accessed by firstly calling **session_start()** and then by passing the corresponding key to the **$_SESSION** associative array.

    使用两个会话变量 Rollnumber 和 Name 访问会话数据的 PHP 代码如下所示：

    ```
    <?php

    session_start();

    echo 'The Name of the student is :' . $_SESSION["Name"] . '<br>'; 
    echo 'The Roll number of the student is :' . $_SESSION["Rollnumber"] . '<br>';

    ?>
    ```

    发帖主题：Re：Колибри0.7.0

    ```
    The Name of the student is :Ajay 
    The Roll number of the student is :11
    ```

*   **Destroying Certain Session Data**: To delete only a certain session data,the unset feature can be used with the corresponding session variable in the **$_SESSION** associative array.

    仅从关联会话数组中取消设置“Rollnumber”会话变量的 PHP 代码：

    ```
    <?php

    session_start();

    if(isset($_SESSION["Name"])){
        unset($_SESSION["Rollnumber"]);
    }

    ?>
    ```

*   **销毁完整会话**：**SESSION_Destroy()**函数用于完全销毁会话。 SESSION_Destroy()函数不需要任何参数。

    ```
    <?php

    session_start();
    session_destroy();

    ?>
    ```

**要点**

1.  会话 ID 由 PHP 引擎随机生成。
2.  会话数据存储在服务器上，因此不必随每个浏览器请求一起发送。
3.  在浏览器中的脚本生成任何输出之前，需要在页面开头调用 session_start()函数。