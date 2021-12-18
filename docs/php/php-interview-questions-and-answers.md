# PHP 面试问答

> Original: [https://www.geeksforgeeks.org/php-interview-questions-and-answers/](https://www.geeksforgeeks.org/php-interview-questions-and-answers/)

![PHP interview questions](img/19a7a975dc51450401ac805fb784882c.png)

1.  **[What is PHP ?](https://www.geeksforgeeks.org/php-introduction/)**
    PHP is the general-purpose programming language used to design a website or web application. It is server-side scripting language embedded with HTML to develop a Static website, Dynamic website or Web applications. It was created by Rasmus Lerdorf in 1994.
2.  **[What is the full form of PHP ?](https://www.geeksforgeeks.org/php-full-form/)**
    PHP is the abbreviation of Hypertext Preprocessor and earlier it was abbreviated as Personal Home Page.
3.  **What was the old name of PHP ?**
    The old name of PHP was Personal Home Page.
4.  **What are the uses of PHP ?**
    *   它是一种服务器端脚本语言，用于设计动态网站或 Web 应用程序。
    *   它从表单接收数据以生成动态页面内容。
    *   它可以处理数据库、会话、发送和接收 cookie、发送电子邮件等。
    *   它可以用来添加、删除、修改数据库中的内容。
    *   它可以用来设置对用户访问网页的限制。

5.  **What is PEAR in PHP ?**
    PEAR is a framework and distribution system for reusable PHP components. It stands for PHP Extension and Application Repository. It contains PHP snippets and a library to ruse the code. It provides a command-line interface to install packages.
6.  **[What is the difference between static and dynamic websites ?](https://www.geeksforgeeks.org/static-vs-dynamic-website/)**
    *   **静态网站：**从服务器返回网页，这些网页是使用 HTML、CSS 或 JavaScript 等简单语言构建的预构建源代码文件。 静态网站中的服务器上没有内容处理。
    *   **动态网站：**网页是从服务器返回的，在运行时进行处理意味着它们不是预先构建的网页，而是在运行时根据用户的需求，借助服务器支持的 PHP、Node.js、ASP.NET 等服务器端脚本语言构建的。
7.  **What is the correct and the two most common ways to start and finish a PHP block of code ?**
    The PHP code always starts with <?php and ends with ?>. The block of PHP code are:

    ```php
    <?php   [ --Content of PHP code-- ]   ?>
    ```

8.  **[How to execute a PHP script from the command line?](https://www.geeksforgeeks.org/how-to-execute-php-code-using-command-line/)**
    Use the following steps to run PHP program using command line:
    *   打开终端或命令行窗口。
    *   转到 PHP 文件所在的指定文件夹或目录。
    *   然后，我们可以使用命令`php file_name.php`运行 PHP 代码
    *   使用命令`php -S localhost:port -t your_folder/`启动服务器以测试 php 代码
9.  **How to display text with a PHP script ?**
    There are two methods **echo** and **print** to display the text.
10.  **Is PHP a case sensitive language ?**
    No, PHP is a partially case sensitive language. It means the variable names are **case-sensitive** and the function names are **not case sensitive** i.e. user-defined functions are not case sensitive.

11.  **What is the main difference between PHP 4 and PHP 5 ?**
    PHP 5 contains many additional OOP (object-oriented programming) features.
12.  **[What are the rules for naming a PHP variable ?](https://www.geeksforgeeks.org/php-variables/)**
    Variables in a program are used to store some values or data that can be used later in a program. PHP has its own way of declaring and storing variables. The characteristics of the variables are listed below:
    *   在 PHP 中声明的变量必须以美元符号($)开头，后跟变量名。
    *   变量名称中包含字母数字字符和下划线(即‘a-z’、‘A-Z’、‘0-9’和‘_’)。
    *   变量名必须以字母或下划线开头，而不是数字。
    *   PHP 是一种松散类型的语言，我们不需要声明变量的数据类型，而是 PHP 通过分析值自动假定变量类型。
    *   PHP 变量区分大小写，即$SUM 和$SUM 的处理方式不同。
13.  **[How do you define a constant in PHP ?](https://www.geeksforgeeks.org/php-defining-constants/)**
    The define() function is used to create and retrieve the value of a constant. A PHP constant is an identifier whose value can not be change over the time (such as the domain name of a website eg. www.geeksforgeeks.org). If you have defined a constant, it can never be changed or undefined. The $ symbol is not used with a constant.
14.  **What are the popular Content Management Systems (CMS) in PHP ?**
    *   **WordPress：**WordPress 是一个免费的开源内容管理系统(CMS)框架。 它是目前使用最广泛的 CMS 框架。
    *   **Joomla：**它是一个免费的开源内容管理系统(CMS)，用于发布网络内容。 它遵循可以独立使用的模型-视图-控制器 Web 应用程序框架。
    *   **Magento：**它是一个开源的电子商务平台，用于发展在线业务。
    *   **Drupal：**它是用 PHP 开发的内容管理系统(CMS)平台，在 GNU(通用公共许可证)下发布。
15.  **What is the purpose of break and continue statement ?**
    *   **Break：**Break 语句立即终止循环的整个迭代，程序控制从循环之后的下一条语句恢复。
    *   **Continue：**Continue 语句跳过当前迭代，提前进行下一次迭代。 Continue 2 充当 Case 的终止符，并跳过循环的当前迭代。
16.  **What are the popular frameworks in PHP ?**
    *   拉勒维尔
    *   CodeIgniter
    *   塞姆法尼
    *   CakePHP
    *   叶氏
    *   Zend 框架
    *   法尔康
    *   FuelPHP
    *   PHPIXIE
    *   苗条的 / 小的 / 少的
17.  **How to make single and multi-line comments in PHP ?**
    Comments are used to prevent the execution of the statement. It is ignored by the compiler. In PHP, there are two types of comments: single-line comments and multi-line comments.
    *   **单行注释：**注释以双正斜杠(//)开头。
    *   **多行注释：**注释包含在/*注释部分*/中
18.  **[What is the use of count() function in PHP ?](https://www.geeksforgeeks.org/php-count-function/)**
    The count() function in PHP is used to count the number of elements present in the array. The function might return 0 for the variable that has been set to an empty array. Also for the variable which is not set the function returns 0.
19.  **[What are the different types of loop in PHP ?](https://www.geeksforgeeks.org/php-loops/)**
    PHP supports four different types of loop which are listed below:
    *   For 循环
    *   While 循环
    *   Do-While 循环
    *   Foreach 循环
20.  **PHP 中的 for 循环和 foreach 循环有什么区别？**
    *   For 循环被认为是公开执行迭代，而 foreach 循环隐藏迭代并明显简化。
    *   与 for 循环相比，foreach 循环的性能被认为更好。
    *   尽管 foreach 循环遍历了一组元素，但与 for 循环相比，执行得到了简化，完成循环所需的时间更少。
    *   Foreach 循环为索引迭代分配临时内存，这使得整个系统在内存分配方面的性能变得冗余。