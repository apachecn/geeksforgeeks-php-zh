# PHP|shell_exec()与 exec()函数

> Original: [https://www.geeksforgeeks.org/php-shell_exec-vs-exec-function/](https://www.geeksforgeeks.org/php-shell_exec-vs-exec-function/)

**shell_exec()函数**

Shell_exec()函数是 PHP 中的一个内置函数，用于通过 shell 执行命令并以字符串形式返回完整的输出。 Shell_exec 是反引号操作符的别名，用于那些习惯于*nix 的操作符。 如果命令失败，则返回 NULL，并且这些值对于错误检查不可靠。

**语法：**

```
*string* shell_exec( $cmd )
```

**参数：**此函数接受单个参数*$cmd*，该参数用于保存将要执行的命令。

**返回值：**此函数返回执行的命令，如果出现错误，则返回 NULL。

**注意：**当 PHP 在安全模式下运行时，此功能被禁用。

**示例：**

```
<?php

// Use ls command to shell_exec
// function
$output = shell_exec('ls');

// Display the list of all file
// and directory
echo "<pre>$output</pre>";
?>
```

发帖主题：Re：Колибри0.7.8.0

**exec()函数**

Exec()函数是 PHP 中的内置函数，用于执行外部程序并返回输出的最后一行。 如果没有命令正确运行，它还返回 NULL。

**语法：**

```
*string* exec( $command, $output, $return_var )
```

**参数：**此函数接受上述三个参数，如下所述：

*   **$COMMAND:** this parameter is used to save the command to be executed.
*   **$OUTPUT:** this parameter is used to specify the array to be populated with each line output of the command.
*   The **$RETURN_var:** $RETURN_var parameter appears with the output parameter, and then it returns the status of the executed command that will be written to this variable.

**返回值：**此函数返回执行的命令，请务必设置并使用 OUTPUT 参数。

**示例：**

```
<?php
// (on a system with the "iamexecfunction" executable in the path)
echo exec('iamexecfunction');
?>
```

发帖主题：Re：Колибри0.7.8.0

**参考文献：**

*   [http：//php.net/manual/en/function.shell-exec.php](http://php.net/manual/en/function.shell-exec.php)
*   [http：//php.net/manual/en/function.exec.php](http://php.net/manual/en/function.exec.php)

PHP 是一种专门为 Web 开发设计的服务器端脚本语言。 您可以按照这个[PHP 教程](https://www.geeksforgeeks.org/php-tutorials/)和[PHP 示例](https://www.geeksforgeeks.org/php-examples/)从头开始学习 PHP。