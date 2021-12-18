# 如何在 PHP 中强制下载一个文件？

> 原文:[https://www . geesforgeks . org/如何强制文件在 php 中下载/](https://www.geeksforgeeks.org/how-to-force-a-file-to-get-downloaded-in-php/)

要强制下载文件，如果您想保持简单，就不需要使用 PHP 脚本。如果此类文件存储在公共可访问的文件夹中，只需创建一个指向该文件的超链接。当用户点击文件链接时，文件将被下载。你可以查看第一个例子[如何在点击一个 HTML 按钮](https://www.geeksforgeeks.org/how-to-trigger-a-file-download-when-clicking-an-html-button-or-javascript/)文章时触发文件下载。

**使用 PHP 强制文件下载:**我们这里将使用 PHP 作为服务器端脚本语言。在 PHP 中，这可以通过使用 **[readfile()函数](https://www.geeksforgeeks.org/php-readfile-function/)** 来完成。 **readfile()** 的主要功能是输出一个文件。单击任何超链接，浏览器将下载相应的文件，如图所示。上例中使用 **[preg_match()函数](https://www.geeksforgeeks.org/php-preg_match-function/)** 进行的正则表达式(regex)验证根本不允许插入任何非法字符。

*   **脚本:**这个脚本是**downloader.php**负责下载文件。

    ```
    <?php
    if(isset($_REQUEST["file"])){
        // Get parameter and decode URL-encoded string
        $file = urldecode($_REQUEST["file"]); 

        // Test whether the file name contains illegal characters

        if(preg_match('/^[^.][-a-z0-9_.]+[a-z]$/i', $file)){
            $filepath = "public/" . $file;

            // Process download
            if(file_exists($filepath)) {
                header('Content-Description: File Transfer');
                header('Content-Type: application/octet-stream');
                header('Content-Disposition: attachment; filename="'
                                            .basename($filepath).'"');
                header('Expires: 0');
                header('Cache-Control: must-revalidate');
                header('Pragma: public');
                header('Content-Length: ' . filesize($filepath));

                // Flush system output buffer
                flush(); 
                readfile($filepath);
                die();
            } else {
                http_response_code(404);
                die();
            }
        } else {
            die("Download cannot be processed");
        }
    }
    ?>
    ```

**示例:**思路是将文件路径信息通过 URL 作为参数发送到 PHP 文件**downloader.php**。其中文件路径信息将在检查文件的有效性后被馈送到**读取文件()功能**。如果在验证过程中出现错误，我们将显示一条消息，说明“下载无法处理”。让我们首先在名为**index.html**的文件中为用户创建界面。

*   **index.html****[url encode()功能](https://www.geeksforgeeks.org/php-urlencode-function/)** 作为一种安全措施，对 URL 中的文件路径进行编码。

    ```
    <?php

    // Array containing sample pdf file names
    $files = array(
        "test1.pdf",
        "test2.pdf"
    );
    $names = array(
        "Book GFG1",
        "Book GFG2"
    );

    // Loop through array to create library
    for ($i = 0;$i <= 1;$i++)
    {
        echo $names[$i];
        echo '<p>
        <a href="downloader.php?file=' . urlencode($files[$i]) . '">Download</a></p>';

    }
    ?>
    ```

*   **输出:** ![](img/779392c04b6a2256023a79df4276ae75.png)