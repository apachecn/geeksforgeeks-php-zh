# PHP 中如何更改会话超时？

> 原文:[https://www . geesforgeks . org/如何更改会话超时 php/](https://www.geeksforgeeks.org/how-to-change-the-session-timeout-in-php/)

在 PHP 中，维护[](https://www.geeksforgeeks.org/php-sessions/)**会话来检查用户是否活跃。当用户变得不活动并且用户忘记从网页注销时，其他用户有可能查看该页面，从而导致安全漏洞。默认情况下，当浏览器关闭时，PHP 中的会话会被破坏。可以自定义会话超时，使用户页面在固定时间后不活动。
**启动会话:**PHP， **session_start()** 功能用于启动网页中的会话。
**语法:**** 

```
session_start();
```

****会话变量:**会话开始后，可以创建会话变量以备将来使用。可以创建会话变量，并将值存储在这些变量中，如下所示:
**语法:**** 

*   **创建变量名为“var1”的会话变量，并将值“5”赋给它，可以按如下方式完成:** 

```
 $_SESSION['var1']=5;
```

*   **将变量分配给会话变量可以通过以下方式完成:** 

```
$username="John";
$_SESSION['username']=$username;
```

****销毁会话变量和会话:**要删除销毁会话前初始化的所有会话变量，应使用以下命令:
**语法:**** 

*   **要销毁特定会话，应使用以下命令:** 

```
session_unset();
```

*   **要销毁整个会话，应使用以下命令:** 

```
session_destroy();
```

****更改会话超时:**考虑到在 HTML 表单中有一个带有“登录”按钮的登录页面。当用户点击“登录”按钮时，会话开始并设置会话变量。初始化存储登录时间的会话变量。然后它被导向用户的主页。** 

*   ****登录页:**T2]**

## **服务器端编程语言（Professional Hypertext Preprocessor 的缩写）**

```
<?php

// Session starts
session_start();
$username = $_POST["username"];

if(isset($_POST["Login"])) {

    // Session Variables are created
    $_SESSION["user"] = $username;  

    // Login time is stored in a session variable
    $_SESSION["login_time_stamp"] = time(); 
    header("Location:homepage.php");
}
?>
```