# PHP 中 fopen 模式“r+”、“rw+”和“w+”有什么区别？

> 原文:[https://www . geeksforgeeks . org/fopen-modes-r-rw-和-w-in-php/](https://www.geeksforgeeks.org/what-is-the-difference-between-fopen-modes-r-rw-and-w-in-php/) 的区别是什么

当涉及到制作应用程序时，文件处理是编程的一个非常重要的部分。我们可能需要从文件中读取输入或将输出写入文件。PHP 中的文件处理类似于其他编程语言。有预定义的功能可以用来完成指定的任务。查看[文件处理基础](https://www.geeksforgeeks.org/php-basics-file-handling/)了解功能。

**语法:**

```
{content}lt;variable_name> = fopen(<file source path>,<access mode>)
```

PHP 中的 fopen 模式 r+、rw+和 w+的区别

*   **r+:** 以读写模式打开文件。文件指针从文件的开头开始。
*   **w+:** 以读写模式打开文件。如果不存在，它会创建一个新文件，如果存在，它会擦除文件的内容，并且文件指针会从头开始。
*   **rw+:** 以读写模式打开文件。文件指针从文件的开头开始。PHP 文档中不存在这种模式，但它运行良好。

**示例:**为了更好的理解，让我们观察一下 fopen 的解析函数。

*   它检查参数的第一个字符，即模式[0]。根据它是 r、w、a 还是 x，识别相应的模式。
*   它会在模式参数中查找“+”的存在。如果存在，它会设置适当的标志。

因此**“r+”****“w+”**打开文件和放置文件指针的方式是有区别的。**“r+”****“rw+”**相同。PHP 只关心字符串以**“r”**开头，有一个**“+”**。**“w”**在**“rw+”**中忽略。因此，它们的工作原理是一样的。

```
PHPAPI int php_stream_parse_fopen_modes(const char *mode, int *open_flags)
{
    int flags;

    switch (mode[0]) {
        case 'r':
            flags = 0;
            break;
        case 'w':
            flags = O_TRUNC|O_CREAT;
            break;
        case 'a':
            flags = O_CREAT|O_APPEND;
            break;
        case 'x':
            flags = O_CREAT|O_EXCL;
            break;
        case 'c':
            flags = O_CREAT;
            break;
        default:
            /* unknown mode */
            return FAILURE;
    }

    if (strchr(mode, '+')) {
        flags |= O_RDWR;
    } else if (flags) {
        flags |= O_WRONLY;
    } else {
        flags |= O_RDONLY;
    }

#if defined(O_CLOEXEC)
    if (strchr(mode, 'e')) {
        flags |= O_CLOEXEC;
    }
#endif

#if defined(O_NONBLOCK)
    if (strchr(mode, 'n')) {
        flags |= O_NONBLOCK;
    }
#endif

#if defined(_O_TEXT) && defined(O_BINARY)
    if (strchr(mode, 't')) {
        flags |= _O_TEXT;
    } else {
        flags |= O_BINARY;
    }
#endif

    *open_flags = flags;
    return SUCCESS;
}
```