# PHP|str_word_count()函数

> Original: [https://www.geeksforgeeks.org/php-str_word_count-function/](https://www.geeksforgeeks.org/php-str_word_count-function/)

**str_word_count()**函数是 PHP 中的内置函数，用于返回有关字符串中使用的单词的信息，如字符串中的单词总数、单词在字符串中的位置等。

**语法：**

```php
str_word_count ( $string , $returnVal, $chars )
```

**使用的参数：**

1.  **$string：**此参数指定用户要计算其单词的字符串。这不是可选参数。
2.  **$rereturn Val：**str_word_count()函数的返回值由$rereturn Val 参数指定。 可选参数，默认值为 0。
    该参数可以根据需要采用以下值：
    *   **0：**它返回字符串*$string*中的字数。
    *   **1：**它返回一个数组，其中包含在字符串中找到的所有单词。
    *   **2：**它返回一个具有键-值对的关联数组，其中键定义单词在字符串中的位置，值是单词本身。
3.  **$chars：**这是一个可选参数，用于指定应视为‘word’的附加字符列表。

**返回类型**：函数的返回类型取决于参数*$rereturn Val*，返回值如上所述。

以下程序解释了 str_word_count()函数的工作原理：

1.  **Calculating the number of words in a string**: To Display only the number of words in a string,the str_word_count() function should be executed in the following way:

    ```php
    <?php
    $mystring = "Twinkle twinkl4e little star";
    print_r(str_word_count($mystring));
    ?>
    ```

    发帖主题：Re：Колибри0.7.0

    ```php
    5
    ```

2.  **Find the words in a string**: To return an array containing the words in a string,the str_word_count() function should be executed in the following way:

    ```php
    <?php
    $mystring = "Twinkle twinkl4e little star";
    print_r(str_word_count($mystring, 1));
    ?>
    ```

    发帖主题：Re：Колибри0.7.0

    ```php
    Array ( [0] => Twinkle [1] => twinkl [2] => e [3] => little [4] => star )
    ```

3.  **Find words in a string along with numeric position of the words**: To return an array containing the words in a string along with numeric position of the words,the str_word_count() function should be executed in the following way:

    ```php
    <?php
    $mystring = "Twinkle twinkl4e little star";
    print_r(str_word_count($mystring, 2));
    ?>
    ```

    发帖主题：Re：Колибри0.7.0

    ```php
    Array ( [0] => Twinkle [8] => twinkl [15] => e [17] => little [24] => star )
    ```

4.  **Find words in a string when some special character are considered as word**: To return an array containing the words in a string where a character shall be considered as a word, the str_word_count() function should be executed in the following way:

    ```php
    <?php
    $mystring = "Twinkle twinkl4e little star";
    print_r(str_word_count($mystring, 2 ,4));
    ?>
    ```

    发帖主题：Re：Колибри0.7.0

    ```php
    Array ( [0] => Twinkle [8] => twinkl4e [17] => little [24] => star )
    ```