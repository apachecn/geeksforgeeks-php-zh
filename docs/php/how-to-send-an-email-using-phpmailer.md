# 如何使用 PHPMailer 发送邮件？

> 原文:[https://www . geesforgeks . org/如何使用-phpmailer 发送电子邮件/](https://www.geeksforgeeks.org/how-to-send-an-email-using-phpmailer/)

PHPMailer 是一个代码库，用于从 web 服务器通过 PHP 代码安全轻松地发送电子邮件。通过 PHP 代码直接发送电子邮件需要高度熟悉 SMTP 标准协议以及有关垃圾邮件电子邮件注入的相关问题和漏洞。PHPMailer 简化了发送电子邮件的过程，非常容易使用。

**安装:**安装 PHPMailer 最好的方法是使用**作曲。**继续之前，确保安装[作曲家](https://getcomposer.org/)。

*   打开命令提示符，转到要使用 PHPMailer 的项目目录。
*   运行以下命令:

    ```
    composer require phpmailer/phpmailer
    ```

*   等待安装完成。它会将所有必要的类下载到您的项目文件夹中。

**使用 PHPMailer:**
将 PHPMailer 类导入全局命名空间。
**注意:**确保这些行在脚本顶部，不在任何函数内部。

```
use PHPMailer\PHPMailer\PHPMailer;
use PHPMailer\PHPMailer\Exception;

```

加载作曲家的自动加载器。

```
require 'vendor/autoload.php';

```

创建一个 PHPMailer 类对象。

```
$mail = PHPMailer()
```

**配置服务器设置:**

*   **SMTPDebug:** 用于显示有关连接问题和发送电子邮件的消息。它具有以下值:
    *   0:是默认值。禁用调试。
    *   1:显示客户端发送的输出消息。
    *   2:作为 1，加上显示从服务器收到的响应。
    *   3: As 2，加上有关初始连接的更多信息–此级别可帮助诊断 STARTTLS 故障。
    *   4: As 3，加上显示更低级别的信息。
*   **isSMTP():** 设置邮件程序使用 SMTP。
*   **isMail():** 设置邮件程序使用 PHP 的邮件功能。
*   **主机:**指定服务器。
*   【SMTP 身份验证:启用/禁用 SMTP 身份验证。
*   **用户名:**指定用户名。
*   **密码:**指定密码。
*   **SMTPSecure:** 指定加密技术。接受的值为“tls”或“ssl”。
*   **端口:**指定要连接的 TCP 端口。

```
$mail->SMTPDebug = 2;                   // Enable verbose debug output
$mail->isSMTP();                        // Set mailer to use SMTP
$mail->Host       = 'smtp.gfg.com;';    // Specify main SMTP server
$mail->SMTPAuth   = true;               // Enable SMTP authentication
$mail->Username   = 'user@gfg.com';     // SMTP username
$mail->Password   = 'password';         // SMTP password
$mail->SMTPSecure = 'tls';              // Enable TLS encryption, 'ssl' also accepted
$mail->Port       = 587;                // TCP port to connect to

```

添加邮件的收件人。

```
$mail->setFrom('from@gfg.com', 'Name');           // Set sender of the mail
$mail->addAddress('receiver1@gfg.net');           // Add a recipient
$mail->addAddress('receiver2@gfg.com', 'Name');   // Name is optional

```

添加附件(如果有)。

```
$mail->addAttachment('url', 'filename');    // Name is optional

```

添加内容。

*   **isHTML():** 如果传递 true，则将电子邮件格式设置为 HTML。
*   **主题:**设置邮件的主题。
*   **正文:**设置邮件的内容。
*   **备选正文:**备选正文，以防电子邮件客户端不支持 HTML。

```
$mail->isHTML(true);                                  
$mail->Subject = 'Subject';
$mail->Body    = 'HTML message body in <b>bold</b>!';
$mail->AltBody = 'Body in plain text for non-HTML mail clients';

```

最后，发邮件。

```
$mail->send();
```

你的电子邮件会被发送。

**程序:**用 PHPMailer 完成发送电子邮件的 PHP 程序。

```
<?php

use PHPMailer\PHPMailer\PHPMailer;
use PHPMailer\PHPMailer\Exception;

require 'vendor/autoload.php';

$mail = new PHPMailer(true);

try {
    $mail->SMTPDebug = 2;                                       
    $mail->isSMTP();                                            
    $mail->Host       = 'smtp.gfg.com;';                    
    $mail->SMTPAuth   = true;                             
    $mail->Username   = 'user@gfg.com';                 
    $mail->Password   = 'password';                        
    $mail->SMTPSecure = 'tls';                              
    $mail->Port       = 587;  

    $mail->setFrom('from@gfg.com', 'Name');           
    $mail->addAddress('receiver1@gfg.com');
    $mail->addAddress('receiver2@gfg.com', 'Name');

    $mail->isHTML(true);                                  
    $mail->Subject = 'Subject';
    $mail->Body    = 'HTML message body in <b>bold</b> ';
    $mail->AltBody = 'Body in plain text for non-HTML mail clients';
    $mail->send();
    echo "Mail has been sent successfully!";
} catch (Exception $e) {
    echo "Message could not be sent. Mailer Error: {$mail->ErrorInfo}";
}

?>
```