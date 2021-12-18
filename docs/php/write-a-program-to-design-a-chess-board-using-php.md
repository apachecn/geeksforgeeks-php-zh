# 使用 PHP 编写程序设计棋盘

> 原文:[https://www . geesforgeks . org/write-a-program-to-design-a-chess-board-use-PHP/](https://www.geeksforgeeks.org/write-a-program-to-design-a-chess-board-using-php/)

国际象棋是两个玩家之间进行的娱乐性和竞争性的棋盘游戏。它是在一个正方形棋盘上进行的，64 个正方形交替排列在一个 8 乘 8 的黑白网格中。在本文中，我们将学习如何使用 PHP 设计一个棋盘。

**方法:**

*   Create chess with php; We must run 2 loops, each of which will create 8 blocks.
*   The inner loop will generate a table row with a black/white background color according to a value.
*   If the value is even, a black background is generated.
*   If the value is odd, a white background is generated.

**棋盘使用 For-Loop:**

## PHP

```html
<!DOCTYPE html>
<html>

<body>
    <table width="400px" border="1px" cellspacing="0px">
        <?php
        echo "Chess by GeeksforGeeks";
        $value = 0;

        for($col = 0; $col < 8; $col++) {
            echo "<tr>";
            $value = $col;

            for($row = 0; $row < 8; $row++) {
                if($value%2 == 0) {
                    echo 
"<td height=40px width=20px bgcolor=black></td>";
                    $value++;
                }
                else {
                    echo 
"<td height=40px width=20px bgcolor=white></td>";
                    $value++;
                }
            }
            echo "</tr>";
        }
        ?>
    </table>
</body>

</html>
```