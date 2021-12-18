# PHP 程序输出|第 4 集

> 原文:[https://www.geeksforgeeks.org/output-php-programs-set-4/](https://www.geeksforgeeks.org/output-php-programs-set-4/)

预测以下 PHP 程序的输出:

**问题 1**

```
<?php

"Welcome to GeeksforGeeks!"

?>
```

选项:

1.  错误
2.  欢迎来到极客乐园！
3.  没有任何东西
4.  缺少分号错误

输出:

```
Nothing

```

**说明:**如果你需要在屏幕上输出一些东西，你需要使用 echo 或 print_r。

**问题 2**

```
<?php

print_r "I am intern at GeeksforGeeks."

?>
```

选项:

1.  错误
2.  我是极客公司的实习生。
3.  没有任何东西
4.  缺少分号错误

输出:

```
Error

```

**解释:**语句应该是 print _ r(‘我是 GeeksforGeeks 的实习生。’)来打印 Hello world。另外，如果只有一行，那么就不需要分号，但最好使用它。

**问题 3**

```
<?php

echo 'GeeksforGeeks';

<html>
GeeksforGeeks
</html>

?>
```

选项:

1.  极客们
2.  geeks forgeeks geeks geeks forgeeks
3.  GeeksforGeeks
    GeeksforGeeks
4.  句法误差

输出:

```
Syntax Error

```

**解释:**解析错误:语法错误，第 2 行出现意外的“<”。你不能在 php 标签中使用 html 标签。

**问题 4**

```
<?php

Echo "GeeksforGeeks1";
echo " GeeksforGeeks2";
ECHO " GeeksforGeeks3";

?>
```

选项:

1.  geeks forgeeks 1 geeks forgeeks 2 geeks forgeeks 3
2.  geeksforgeeks 1
    geeksforgeeks 2
    geeksforgeeks 3
3.  错误
4.  GeeksforGeeks1 GeeksforGeeks3

输出:

```
GeeksforGeeks1 GeeksforGeeks2 GeeksforGeeks3

```

**说明:**在 PHP 中，所有用户定义的函数、类和关键字(如 if、else、while、echo 等)。)不区分大小写。

**问题 5**

```
<?php

$color = "green";
echo "$color";
echo "$COLOR";
echo "$Color";

?>
```

选项:

1.  格林格林格林
2.  绿色绿色
3.  绿色的
4.  错误

输出:

```
green

```

**说明:**在 PHP 中，所有变量都区分大小写。

**问题 6**

```
<?php # echo "GeeksforGeeks";

echo "# GeeksforGeeks"; 

?>
```

选项:

1.  #极客们
2.  GeeksforGeeks# GeeksforGeeks
3.  极客们
4.  错误

输出:

```
# GeeksforGeeks

```

**问题 7**

```
<?php

echo "echo "GeeksforGeeks"";

?>
```

选项:

1.  极客们
2.  回音" GeeksforGeeks "
3.  回音 GeeksforGeeks
4.  错误

输出:

```
Error

```

**解释:**如果语句是 echo“echo”geeks forgeeks“”，它就会打印 echo“geeks forgeeks”；。