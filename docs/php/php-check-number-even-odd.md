# PHP |检查数字是偶数还是奇数

> 原文:[https://www.geeksforgeeks.org/php-check-number-even-odd/](https://www.geeksforgeeks.org/php-check-number-even-odd/)

一个数如果能被 2 整除就叫做偶数，如果不能被 2 整除就叫做奇数。给定一个数字，我们需要在 PHP 中检查它是奇数还是偶数。

**示例:**

```
Input : 42
Output : Even
Explanation: The number 42 is divisible by 2

Input : 39
Output : Odd
Explanation: The number 39 is not divisible by 2

```

我们可以通过两种不同的方式解决这个问题，如下所述:

1.  **Using modulo (%) operator**: This is the simplest method of checking for even and odd and in this method, we simply check whether the number is divisible by 2 or not using the modulo ‘%’ operator.

    下面的程序解释了上面的方法:

    ## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

    ```
    <?php
    // PHP code to check whether the number 
    // is Even or Odd in Normal way
    function check($number){
        if($number % 2 == 0){
            echo "Even"; 
        }
        else{
            echo "Odd";
        }
    }

    // Driver Code
    $number = 39;
    check($number)
    ?>
    ```

    **Output :**

    ```
    Odd

    ```

    **时间复杂度** : O(1)

2.  **Recursive method**: In the recursive approach, we reduce the number by 2 in each recursive call. If the final number is 0 then its even or else it is 1, the result will be odd.
    Below is the implementation of above approach:

    ## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

    ```
    <?php
    // Recursive function to check whether
    // the number is Even or Odd 
    function check($number){
        if($number == 0)
            return 1;
        else if($number == 1)
            return 0;
        else if($number<0)
            return check(-$number);
        else
            return check($number-2);        
    }

    // Driver Code
    $number = 39;
    if(check($number))
        echo "Even";
    else
        echo "Odd";
    ?>
    ```

    **Output :**

    ```
    Odd

    ```

    **时间复杂度** : O(n)

3.  **Using Bit Manipulation:**
    In this method we will find bit-wise AND of the number with 1\. If the bit-wise AND is 1, then the number is odd, else even.

    **下面是上面思路的实现。**

    ## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

    ```
    <?php
    // PHP code to check whether the number 
    // is Even or Odd using Bitwise Operator
    function check($number)
    {

        // One
        $one = 1;

        // Bitwise AND
        $bitwiseAnd = $number & $one;

        if($bitwiseAnd == 1)
        {
            echo "Odd"; 
        }
        else{
            echo "Even";
        }
    }

    // Driver Code
    $number = 39;
    check($number)
    ?>
    ```

    **Output :**

    ```
    Odd

    ```

    **时间复杂度:** O(1)

PHP 是一种专门为 web 开发设计的服务器端脚本语言。您可以通过以下 [PHP 教程](https://www.geeksforgeeks.org/php-tutorials/)和 [PHP 示例](https://www.geeksforgeeks.org/php-examples/)从头开始学习 PHP。