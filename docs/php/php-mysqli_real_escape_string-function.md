# PHP|mysqli_real_scape_string()函数

> Original: [https://www.geeksforgeeks.org/php-mysqli_real_escape_string-function/](https://www.geeksforgeeks.org/php-mysqli_real_escape_string-function/)

**mysqli_real_scape_string()函数**是 PHP 中的一个内置函数，用于转义 SQL 查询中使用的所有特殊字符。 在数据库中插入字符串之前使用它，因为它会删除任何可能干扰查询操作的特殊字符。当使用简单字符串时，可能会包含反斜杠和撇号等特殊字符(特别是当它们直接从输入此类数据的表单获取数据时)。 这些被认为是查询字符串的一部分，会干扰其正常功能。

## PHP

```
<?php

$connection = mysqli_connect(
    "localhost", "root", "", "Persons");

// Check connection
if (mysqli_connect_errno()) {
    echo "Database connection failed.";
}

$firstname = "Robert'O";
$lastname = "O'Connell";

$sql="INSERT INTO Persons (FirstName, LastName)
            VALUES ('$firstname', '$lastname')";

if (mysqli_query($connection, $sql)) {

    // Print the number of rows inserted in
    // the table, if insertion is successful
    printf("%d row inserted.\n",
            $mysqli->affected_rows);
}
else {

    // Query fails because the apostrophe in
    // the string interferes with the query
    printf("An error occurred!");
}

?>
```

在上面的代码中，查询失败，因为在使用 mysqli_query()执行查询时，撇号被视为查询的一部分。 解决方案是在查询中使用字符串之前使用 mysqli_real_scape_string()。

## PHP

```
<?php

$connection = mysqli_connect(
        "localhost", "root", "", "Persons");

// Check connection
if (mysqli_connect_errno()) {
    echo "Database connection failed.";
}

$firstname = "Robert'O";
$lastname = "O'Connell";

// Remove the special characters from the
// string using mysqli_real_escape_string

$lastname_escape = mysqli_real_escape_string(
                    $connection, $lastname);

$firstname_escape = mysqli_real_escape_string(
                    $connection, $firstname);

$sql="INSERT INTO Persons (FirstName, LastName)
            VALUES ('$firstname_escape', '$lastname_escape')";

if (mysqli_query($connection, $sql)) {

    // Print the number of rows inserted in
    // the table, if insertion is successful
    printf("%d row inserted.\n", $mysqli->affected_rows);
}

?>
```

发帖主题：Re：Колибри0.7.8.0

```
1 row inserted. 
```