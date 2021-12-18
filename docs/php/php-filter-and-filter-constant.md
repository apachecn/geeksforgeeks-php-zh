# PHP|过滤和过滤常量

> Original: [https://www.geeksforgeeks.org/php-filter-and-filter-constant/](https://www.geeksforgeeks.org/php-filter-and-filter-constant/)

PHP Filter 是一个扩展，它通过清理或验证数据来过滤数据。 它在网站的安全方面起着至关重要的作用，当数据来自未知或外来来源(如用户提供的输入)时，它尤其有用。 例如，来自 HTML 表单的数据。

过滤器主要有两种类型，如下所示：

*   **Verification:** is used to verify or check whether the data meets certain conditions. For example, passing in FILTER_VALIDATE_URL determines whether the data is a valid URL, but it does not change the existing data itself.
*   **cleanup:** unlike validation, cleanup cleans up data to ensure that unwanted characters do not appear by deleting or changing the data. For example, passing in filter_sanitize_email removes all characters that are not suitable for e-mail addresses. That is, it does not validate the data.

**示例 1：**使用 FILTER_VALIDATE_URL 过滤器验证 URL 的 PHP 程序。

```php
<?php
// PHP program to validate URL

// Declare variable and initialize it to URL
$url = "https://www.geeksforgeeks.org";

// Use filter function to validate URL
if (filter_var($url, FILTER_VALIDATE_URL)) {
    echo("valid URL");
} 
else {
    echo("Invalid URL");
}

?>
```

**示例 2：**使用 FILTER_VALIDATE_EMAIL 过滤器验证电子邮件的 PHP 程序。

```php
<?php
// PHP program to validate email

// Declare variable and initialize it to email
$email = "xyz@gmail.com";

// Use filter function to validate email
if (filter_var($email, FILTER_VALIDATE_EMAIL)) {
    echo "Valid Email";
} 
else {
    echo "Invalid Email";
}

?>
```

**过滤功能：**过滤功能用于过滤来自不安全来源的数据。

*   **filter_var()：**筛选特定变量
*   **filter_var_array()：**过滤多个变量，即变量数组
*   **filter_has_var()：**检查特定输入类型的变量是否存在
*   **filter_id()：**帮助获取指定筛选器名称的筛选器 ID
*   **filter_list()：**以数组形式返回支持的筛选器名称列表。
*   **filter_input()：**获取外部变量并对其进行过滤(如果设置为这样做的话)。
*   **filter_input_array()：**与 filter_input()相同，但这里获取多个变量，即变量数组，如果设置为这样做，则对其进行过滤。

**预定义筛选器常量：**下面列出了许多预定义筛选器常量：

*   **verify filter constant:**
    *   **filter_valify_boolean:** verify Boolean value
    *   **filter_valify_int:** validate integers
    *   **filter_Valid_Float . T18]**
    *   ****FILTER_VALIDATE_REGEXP:** validate the regular expression**
    ***   **FILTER_VALIDATE_IP:** verify the IP address*   **FILTER_VALIDATE_EMAIL:** verify the email address*   **FILTER_VALIDATE_URL:** verify URL**

    **Clean filter constant:**

    *   **FILTER_SANITIZE_EMAIL:** remove all illegal characters from the email address
    *   **FILTER_SANITZE_ENCODED:** Delete / encode special characters
    *   **FILTER_SANITZE_MAGIC_QUOTES：**应用 Addslash()函数

    *   **FILTER_SANITIZE_NUMBER_INT:** Delete all characters except numbers, +-
    *   **FILTER_SANITIZE_SPECIAL_CHARS:** Delete special characters
    *   **FILTER_SANITZE_FULL_SPECIAL_CHARS** can use FILTER_FLAG_ to disable encoding quotation marks.
    *   **FILTER_SANITIZE_STRING:** remove tags / special characters from the string
    *   **FILTER_SANITIZE_STRIPED：**FILTER_SANITZE_STRING
    *   **FILTER_SANITZE_URL：**ρURL
*   All illegal characters are deleted in **.**
*   ****FILTER_UNSAFE_RAW:** do nothing and can choose to strip / encode special characters**
***   **FILTER_CALLBACK:** call user-defined functions to filter data**

**注意：**在 PHP 5.2.0 和更新版本中，默认情况下启用 PHP 筛选器。 安装需要较旧版本。

**引用：**[http://php.net/manual/en/filter.filters.sanitize.php](http://php.net/manual/en/filter.filters.sanitize.php)