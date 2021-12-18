# PHP|使用 mail()函数发送邮件

> Original: [https://www.geeksforgeeks.org/php-sending-mails-using-mail-function/](https://www.geeksforgeeks.org/php-sending-mails-using-mail-function/)

PHP 是一种服务器端脚本语言，丰富了所需的各种实用程序。 邮件是当今大多数 Web 服务器都需要的服务器端实用程序之一。 邮寄用于广告、账号回收、订阅等。

为了用 PHP 发送邮件，可以使用 mail()方法。

**语法：**

```
bool mail(to , subject , message , additional_headers , additional_parameters)

```

**参数**：该函数有两个必选参数和一个可选参数，如下所述：

*   **至**：指定收件人的电子邮件 ID。 可以使用逗号传递多个电子邮件 ID
*   **Subject**：指定邮件的主题。
*   **message**：指定要发送的消息。
*   **Additional-Headers**(可选)：这是一个可选参数，可以创建多个标题元素，例如 From(指定发件人)、CC(指定抄送/抄送收件人)、Bcc(指定密件抄送/密送收件人)。 **注意：**要添加多个标题参数，必须使用‘\r\n’。
*   **附加参数**(可选)：这是另一个可选参数，可以作为附加标头的扩展传递。 这可以指定一组用作 Sendmail_PATH 配置设置的标志。

**返回类型**：如果邮件发送成功，此方法返回 TRUE，如果发送失败，则返回 FALSE。

例如：

1.  Sending a Simple Mail in PHP

    ```
    <?php
      $to = "recipient@example.com";
      $sub = "Generic Mail";
      $msg="Hello Geek! This is a generic email.";
      if (mail($to,$sub,$msg))
          echo "Your Mail is sent successfully.";
      else
          echo "Your Mail is not sent. Try Again.";
    ?> 
    ```

    发帖主题：Re：Kolibrios

    ```
    Your Mail is sent successfully.

    ```

2.  Sending a Mail with Additional Options

    ```
    <?php
      $to = "recipient@example.com";
      $sub = "Generic Mail";
      $msg = "Hello Geek! This is a generic email.";
      $headers = 'From: sender@example.com' . "\r\n" .'CC: another@example.com';
      if(mail($to,$sub,$msg,$headers))
          echo "Your Mail is sent successfully.";
      else
          echo "Your Mail is not sent. Try Again.";
    ?> 
    ```

    发帖主题：Re：Kolibrios

    ```
    Your Mail is sent successfully.

    ```

**摘要**：

*   使用 mail()方法可以发送各种类型的邮件，如标准邮件、HTML 邮件。
*   Mail()方法打开 SMTP 套接字，尝试发送邮件，然后关闭套接字，因此是一个安全选项。
*   Mail()方法不应用于批量邮件，因为它的成本效益不高。
*   Mail()方法只检查参数或网络故障，因此 mail()方法的成功并不能保证预期的人会收到邮件。