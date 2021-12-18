# PHP 7 有什么新功能？

> 原文:[https://www.geeksforgeeks.org/whats-new-in-php-7/](https://www.geeksforgeeks.org/whats-new-in-php-7/)

**先决条件:** [PHP 7 |特性集 1](https://www.geeksforgeeks.org/php-7-features/)

PHP 5 出现了许多小版本，令人兴奋，包括提供面向对象编程和许多与之相关的特性。

**那么，为什么是 7 而不是 6 呢？**
几乎所有为 PHP 6 考虑的特性最终都在 PHP 5.3 中执行并成功了，所以没有遗漏什么。最后，提出了一种新的特征请求方法。当一个重要版本的特性集被接受时，为了避免混淆，它跳到了最新版本的版本 7。

**是什么让 PHP 7 独一无二？**
PHP 7 的速度和性能变得更好了 PHP codebase 使用了更少的内存，开发了一个更快的引擎，话虽如此，让我们看看这个包中增加了什么

*   **常量数组使用 define():** PHP 数组常量可以通过使用 define()函数来定义。在 PHP 5.6 中，它由 const 关键字定义。

    ```
    <?php

    // Use define() function
    define('GFG', 
        ['Geeks', 'G4G', 'geek']
    );

    // Display content
    echo GFG[0];
    ?>
    ```

    **输出:**

```
Geeks

```