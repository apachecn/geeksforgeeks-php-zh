# PHP |按位运算符

> 原文:[https://www.geeksforgeeks.org/php-bitwise-operators/](https://www.geeksforgeeks.org/php-bitwise-operators/)

按位运算符用于对操作数执行位级运算。运算符首先转换为位级，然后对操作数执行计算。加法、减法、乘法等数学运算。可以在位级执行，以实现更快的处理。在 PHP 中，在位级别工作的运算符是:

*   **& (Bitwise AND) :** This is a binary operator i.e. it works on two operand. Bitwise AND operator in PHP takes two numbers as operands and does AND on every bit of two numbers. The result of AND is 1 only if both bits are 1.

    **语法**:

    ```
    $First & $Second

    This will return another number whose bits are 
    set if both the bit of first and second are set.

    ```

    示例:

    ```
    Input: $First = 5,  $Second = 3

    Output: The bitwise & of both these value will be 1\. 

    Explanation:
    Binary representation of 5 is 0101 and 3 is 0011\. 
    Therefore their bitwise & will be 0001 (i.e. set 
    if both first and second have their bit set.)

    ```

*   **|(按位或):**这也是二进制运算符，即对两个操作数起作用。按位“或”运算符将两个数字作为操作数，并对两个数字的每一位进行“或”。“或”的结果是 1，两位中的任何一位都是 1。

**语法**:

```
$First | $Second

This will return another number whose bits are 
set if either the bit of first or second are set.

```

示例:

```
Input: First = 5, Second = 3

Output: The bitwise | of both these value will be 7\. 

Explanation:
Binary representation of 5 is 0101 and 3 is 0011.
Therefore their bitwise | will be 0111 (i.e. set 
if either first or second have their bit set.)

```

*   **^ (Bitwise XOR ) :** This is also binary operator i.e. works on two operand. This is also known as Exclusive OR operator. Bitwise XOR takes two numbers as operands and does XOR on every bit of two numbers. The result of XOR is 1 if the two bits are different.

    **语法**:

    ```
    $First ^ $Second

    This will return another number whose bits are 
    set if one of the bit in first or second is 
    set but not both.

    ```

    示例:

    ```
    Input: First = 5, Second = 3 

    Output: The bitwise ^ of both these value will be 6\. 

    Explanation:
    Binary representation of 5 is 0101 and 3 is 0011\. 
    Therefore their bitwise ^ will be 0110 (i.e. set 
    if either first or second have their bit set but 
    not both.)

    ```

    *   **~ (Bitwise NOT)** : This is a unary operator i.e. works on only one operand. Bitwise NOT operator takes one number and inverts all bits of it.

    **语法**:

    ```
    ~$number

    This will invert all the bits of $number.

    ```

    示例:

    ```
    Input: number = 5

    Output: The bitwise '~' of this number will be -6.

    Explanation:
    Binary representation of 5 is 0101\. Therefore the
    bitwise ~ of this will be 1010 (inverts all the 
    bits of the input number)

    ```

    *   **<< (Bitwise Left Shift) :** This is a binary operator i.e. works on two operand. Bitwise Left Shift operator takes two numbers, left shifts the bits of the first operand, the second operand decides the number of places to shift.

    **语法**:

    ```
    $First << $Second

    This will shift the bits of $First towards the 
    left. $Second decides the number of time the
    bits will be shifted.

    ```

    示例:

    ```
    Input: First = 5, Second = 1

    Output: The bitwise << of both these value will be 10\. 

    Explanation:
    Binary representation of 5 is 0101 . Therefore, 
    bitwise << will shift the bits of 5 one times 
    towards the left (i.e. 01010 )

    ```

    **注:**一位按位左移相当于与 2 相乘。

    *   **>> (Bitwise Right Shift) :** This is also binary operator i.e. works on two operand. Bitwise Right Shift operator takes two numbers, right shifts the bits of the first operand, the second operand decides the number of places to shift.

    **语法**:

    ```
    $First >> $Second

    This will shift the bits of $First towards the 
    right. $Second decides the number of time the 
    bits will be shifted.

    ```

    示例:

    ```
    Input: First = 5, Second = 1 

    Output: The bitwise >> of both these value will be 2\. 

    Explanation:
    Binary representation of 5 is 0101 . Therefore, 
    bitwise >> will shift the bits of 5 one times 
    towards the right(i.e. 010)

    ```

    **注:**一位按位右移相当于 2 除。

下面是按位运算符在 PHP 中的实现:

```
<?php
    // PHP code to demonstrate Bitwise Operator.

    // Bitwise AND
    $First = 5;
    $second = 3;
    $answer = $First & $second;

    print_r("Bitwise & of 5 and 3 is $answer");

    print_r("\n");

    // Bitwise OR
    $answer = $First | $second;
    print_r("Bitwise | of 5 and 3 is $answer");

    print_r("\n");

    // Bitwise XOR
    $answer = $First ^ $second;
    print_r("Bitwise ^ of 5 and 3 is $answer");

    print_r("\n");

    // Bitwise NOT
    $answer = ~$First;
    print_r("Bitwise ~ of 5 is $answer");

    print_r("\n");

    // Bitwise Left shift
    $second = 1;
    $answer = $First << $second;
    print_r("5 << 1 will be $answer");

    print_r("\n");

    // Bitwise Right shift
    $answer = $First >> $second;
    print_r("5 >> 1 will be $answer");

    print_r("\n");
?>
```

输出:

```
Bitwise & of 5 and 3 is 1
Bitwise | of 5 and 3 is 7
Bitwise ^ of 5 and 3 is 6
Bitwise ~ of 5 is -6
5 << 1 will be 10
5 >> 1 will be 2

```