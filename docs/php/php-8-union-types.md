# PHP 8 联合类型

> 原文:[https://www.geeksforgeeks.org/php-8-union-types/](https://www.geeksforgeeks.org/php-8-union-types/)

“联合类型”接受多个不同数据类型的值，而不是单个数据类型的值。如果编程语言支持联合类型，则可以在多种类型中声明一个变量。例如，可以有一个函数接受“string”或“float”类型的变量作为参数。PHP 已经支持两种特殊的联合类型。

*   类型或 null，使用特殊"？类型”语法。
*   数组或可遍历的，使用特殊的可迭代类型。

但是在更新之前，语言不支持任意的联合类型。相反，我们使用了 PHPDoc 注释，这是一项相当艰巨的工作。

**例 1:**

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```
<?php
 class GFG {
    /**
     * @var int|float $CodingScore
     */
    private $CodingScore;

    /**
     * @param int|float $CodingScore
     */
    public function setScore($CodingScore) {
        $this->CodingScore = $CodingScore;
    }

    /**
     * @return int|float
     */
    public function getScore() {
        return $this->CodingScore;
    }
}
$a = new GFG();
$a->setScore(120.5);
echo $a->getScore(), "\r\n" ;

$b = new GFG();
$b->setScore(100);
echo $b->getScore();

?>
```

**输出:**

```
120.5
100
```

但是在此更新之后，使用以下语法指定联合类型

```
T1|T2|...
```

它可以用于当前接受类型的所有职位，如下所示。

**例 2:**

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```
<?php
    class GFG {
    private int|float $CodingScore;

    // Union type
    public function setScore(int|float $CodingScore): void {
        $this->CodingScore = $CodingScore;
    }

    //Union type
    public function getScore(): int|float {
        return $this->CodingScore;
    }
}

$a = new GFG();
$a->setScore(120.8);
echo  $a->getScore(),"\r\n";
$a->setScore(100);
echo $a->getScore();

?>
```

**输出:**

```
120.8
100
```