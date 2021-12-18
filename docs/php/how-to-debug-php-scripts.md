# 如何调试 PHP 脚本？

> 原文:[https://www.geeksforgeeks.org/how-to-debug-php-scripts/](https://www.geeksforgeeks.org/how-to-debug-php-scripts/)

当我们用 PHP 编写大量代码行，然后出现一些错误时，消除这些错误可能是一项艰巨的任务。程序员在用 PHP 编程时会犯的一些基本错误有:

*   缺少分号“；”和右括号“}”。
    要调试上述错误，使用一个好的 PHP ide 会很有帮助，因为它会建议用“}”结束括号，用“；”结束语句。
*   变量名拼写错误。记住$var！= $Var 我们知道，PHP 是一种区分大小写的语言。
*   Using “=” instead of “==” (Assignment operator and Equal operator)
    **Example:**

    ```php
    if($a = $b) {
        // Statement
    }
    ```

    这将始终导致“真”，因为将一个变量分配给另一个变量从来都不是错误。

*   像“”和“”这样的 SQL 查询中缺少引号。这是 PHP 编程时非常常见和频繁出现的错误。要调试这种错误，请始终使用带有 echo 的 **mysqli_error($con)** 命令，查看您在 SQL 语句中出现了什么错误，其中**$ con】**是您正在使用的连接变量。
    **例:**

    ```php
    if (!mysqli_query($conn, $sql)) {
        echo "Error: " . $sql . "
    " . mysqli_error($con);
    }

    ```

*   如果您的 PHP 脚本在运行时不产生任何输出，那么请确保在 php.ini 文件中将“display_errors”设置为 on。
*   “解析错误”——当您的代码不被 PHP 理解时，就会出现这个错误。此错误通常伴随语法错误而出现。
*   “Misunderstanding isset() behavior” – Despite its name, isset() not only returns false if an item does not exist but also returns false for null values. This behavior is more problematic than it might appear at first and is a common source of problems.
    **Example:**

    ```php
    $data = fetchRecordFromStorage($storage, $identifier);
    if (!isset($data['keyShouldBeSet']) {
        // do something here if 'keyShouldBeSet' is not set
    }

    ```

    这段代码的作者大概想检查是否在$data 中设置了 keyShouldBeSet。但是，如前所述，如果设置了$data['keyShouldBeSet']但设置为 null，则 isset($data['keyShouldBeSet']也将返回 false。所以上述逻辑是有缺陷的。

*   一个常见的错误是在使用 HTML 命令之前缺少 PHP 关闭。所以总是用 PHP 关闭"？> "然后编写 HTML 代码并在结束 HTML 代码后使用"
*   **PHP debugging tools:** PHP code can be debug using one of many debugging tools to attach a debugger client. PhpStorm works with debug utilities like Xdebug and ZendDebugger.

    作为一个多语种者(知道或使用多种语言)，我们需要一个支持多种语言的 IDE。过去使用的是 Visual Studio 的 Xdebug，所以让我们看看如何用 VS 代码设置它。

    调试服务器设置相同，但每个客户端(IDE 或 CLI)的设置略有不同。参见调试服务器(Zend 扩展)打开一个端口，客户端通过该端口与服务器通信。这只是配置和安装正确组件的问题。

    下面是进行 PHP 编程的步骤:

    *   检查 VS 代码中的 PHP 扩展。
    *   安装 PHP 调试扩展。
    *   点击“重新加载”重新加载 VS 代码。
    *   安装 Xdebug。VS 代码的 PHP 调试扩展只是对 Xdebug 的集成。如果我们安装 PHP 7.0，那么它必须从下载页面获得正确版本的 Xdebug。
    *   现在当你有了正确的版本，把它放在 PHP/ext 目录下。
    *   Next, you need to configure PHP to use the extension and allow remote debugging. Add the following configuration to the php.ini file that’s listed in PHP Info:

        ```php
        ; set the extension path
        zend_extension="C:/Program Files 
        (x86)/PHP/v7.0/ext/php_xdebug-2.6.1-7.0-vc14-nts.dll"
        ; allow remote debugging
        [XDebug]
        xdebug.remote_enable = 1
        xdebug.remote_autostart = 1

        ```

        它将设置 PHP 服务器使用 XDebug。无论使用什么样的 IDE，这里的步骤都是一样的。

    *   Xdebug 打开一个 HTTP 端口，以便调试器可以附加。客户端仍然需要配置为附加和使用调试协议。

最后，配置 VS 代码以连接到 Xdebug。有几个简单的步骤，然后连接是自动的。

*   **配置自己的 IDE:** 安装完 Xdebug 之后，需要配置 IDE 连接到调试器。在 VS 代码中，这意味着添加调试配置。幸运的是，在这一点上是自动的。这只是几个简单的步骤:
    *   切换到调试视图。
    *   单击齿轮调出语言菜单。
    *   选择 PHP。Visual Studio 代码将生成默认配置。
    *   重新加载 PHP 服务器。我们必须安装另一个名为“PHP 服务器”的扩展，这样做就很简单了。使用上下文菜单(右键单击)控制 PHP 服务器。
    *   它将集成开发环境置于一种可以连接到 Xdebug 的状态。与调试器的通信通过调试服务器上的 TCP 端口进行。默认情况下，Xdebug 通过端口 9000 使用 DBGp 协议。*   **Attaching a debugger:** The PHP Debug extension for VS Code generated a launch.json file. That file goes into a .vscode directory in the root of the project.

    ```php
    {
        // Use IntelliSense to learn about possible attributes.
        // Hover to view descriptions of existing attributes.
        // For more information, visit: https://go.microsoft.com/fwlink/?linkid=830387

        "version": "0.2.0",
        "configurations": [
            {
                "name": "Listen for XDebug",
                "type": "php",
                "request": "launch",
                "port": 9000
            },
            {
                "name": "Launch currently open script",
                "type": "php",
                "request": "launch",
                "program": "${file}",
                "cwd": "${fileDirname}",
                "port": 9000
            }
        ]
    }

    ```

    它增加了两种发射配置。这些在调试视图中可用。我们可以连接到一个正在运行的服务器，或者用当前的脚本启动一个新的服务器。因为我已经运行了 phpinfo，所以我将从选择监听 XDebug 来连接到该服务器开始。连接后，您将看到调试工具栏。大多数调试器都有类似的控制机制，允许启动、停止、单步执行和重新启动调试器。

    *   **切换报错级别:** PHP 有几种配置报错的方式。您可以使用 php.ini 文件，并且必须访问它。否则，您可能会使用 htaccess 配置。如果不能使用配置文件，可以选择通过脚本更改值。设置的组合将获得正确的错误记录级别。您需要考虑以下设置:
    *   error_reporting 设置日志记录的级别。
    *   E_NOTICE 在开发过程中很有用，因为它会告诉我们诸如未赋值变量之类的缺陷。
    *   display_errors 用于显示错误消息。
    *   display_startup_errors 只应在调试时使用。
    *   log_errors 和 error_log 协同工作，将错误发送到日志文件。在生产中这样做，而不是向最终用户展示。
    *   PHP 手册更详细地阐述了这些设置，并提供了更多信息。