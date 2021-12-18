# PHP|用电子邮件发送附件

> Original: [https://www.geeksforgeeks.org/php-send-attachment-email/](https://www.geeksforgeeks.org/php-send-attachment-email/)

在 Web 浏览器中，发送电子邮件是非常常见的活动。 例如，当新用户加入网络时发送电子邮件、发送时事通讯、发送问候信、发送发票。 我们可以使用内置的[**mail()**](https://www.geeksforgeeks.org/php-sending-mails-using-mail-function/)函数以编程方式发送电子邮件。 该函数需要三个必需的参数来保存有关收件人、邮件主题和邮件正文的信息。 除了这三个必需的参数外，还有两个参数是可选的。 其中一个是标题，另一个是参数。)
我们在上一篇文章[中已经讨论过用 PHP 发送基于文本的电子邮件。 在本文中，我们将了解如何使用 mail()函数发送带有附件的电子邮件。
当调用 mail()函数时，PHP 将尝试立即将邮件发送给收件人，然后在成功传递邮件时返回 TRUE，如果出现错误则返回 FALSE。
**语法**：](https://www.geeksforgeeks.org/php-sending-mails-using-mail-function/) 

```
bool mail( $to, $subject, $message, $headers, $parameters );
```

以下是每个参数的说明。
n

<figure class="table">

| 名字 / 姓名 / 姓 / 名人 | 描述 / 描写 / 形容 / 类别 | Required / optional | 类型 / 品种 / 象征 / 印刷文字 |
| **to** | It contains specific emails | What is needed | One or more recipients of. ] |
| **topic** | This contains the subject of the email. This parameter cannot contain any newline characters | Necessary | String |
| **消息** | It contains the message to be sent. Each line is separated by LF (\ n). The line should not exceed 70 characters (we will use the WordWrap () function to do this.) | Necessary | String |
| **title** | This includes other headings, such as From, CC, Mime Version, Bcc. | Optional | 线 / 细绳 / 一连串 / 纤维 |
| **parameter** | For sending mail programs | Optional | 细绳 |

</figure>

指定一个附加参数

当我们通过 PHP 发送邮件时，消息中的所有内容将仅被视为简单文本。 如果我们在消息正文中放置任何 HTML 标记，它将不会被格式化为 HTML 语法。 HTML 标签将显示为简单文本。
要根据 HTML 语法格式化任何 HTML 标签，我们可以指定邮件正文的**MIME(多用途 Internet 邮件扩展)版本、内容类型和字符集**。如果
要随电子邮件一起发送附件，我们需要将**内容类型**设置为**混合/多部分**，并且我们必须在**边界**内定义文本和附件部分。
**创建 HTML 表单**：

## 超文本标记语言

```
<form enctype="multipart/form-data" method="POST" action="">
    <label>Your Name <input type="text" name="sender_name" /> </label>
    <label>Your Email <input type="email" name="sender_email" /> </label>
    <label>Subject <input type="text" name="subject" /> </label>
    <label>Message <textarea name="message"></textarea> </label>
    <label>Attachment <input type="file" name="attachment" /></label>
    <label><input type="submit" name="button" value="Submit" /></label>
</form>
```

**处理表单数据的 PHP 脚本**：t

## PHP

```
if($_POST['button'] && isset($_FILES['attachment']))
{

    $from_email         = 'sender@abc.com'; //from mail, sender email address
    $recipient_email    = 'recipient@xyz.com'; //recipient email address

    //Load POST data from HTML form
    $sender_name    = $_POST["sender_name"] //sender name
    $reply_to_email = $_POST["sender_email"] //sender email, it will be used in "reply-to" header
    $subject        = $_POST["subject"] //subject for the email
    $message        = $_POST["message"] //body of the email

    /*Always remember to validate the form fields like this
    if(strlen($sender_name)<1)
    {
        die('Name is too short or empty!');
    }
    */

    //Get uploaded file data using $_FILES array
    $tmp_name    = $_FILES['my_file']['tmp_name']; // get the temporary file name of the file on the server
    $name        = $_FILES['my_file']['name'];  // get the name of the file
    $size        = $_FILES['my_file']['size'];  // get size of the file for size validation
    $type        = $_FILES['my_file']['type'];  // get type of the file
    $error       = $_FILES['my_file']['error']; // get the error (if any)

    //validate form field for attaching the file
    if($file_error > 0)
    {
        die('Upload error or No files uploaded');
    }

    //read from the uploaded file & base64_encode content
    $handle = fopen($tmp_name, "r");  // set the file handle only for reading the file
    $content = fread($handle, $size); // reading the file
    fclose($handle);                  // close upon completion

    $encoded_content = chunk_split(base64_encode($content));

    $boundary = md5("random"); // define boundary with a md5 hashed value

    //header
    $headers = "MIME-Version: 1.0\r\n"; // Defining the MIME version
    $headers .= "From:".$from_email."\r\n"; // Sender Email
    $headers .= "Reply-To: ".$reply_to_email."\r\n"; // Email address to reach back
    $headers .= "Content-Type: multipart/mixed;"; // Defining Content-Type
    $headers .= "boundary = $boundary\r\n"; //Defining the Boundary

    //plain text
    $body = "--$boundary\r\n";
    $body .= "Content-Type: text/plain; charset=ISO-8859-1\r\n";
    $body .= "Content-Transfer-Encoding: base64\r\n\r\n";
    $body .= chunk_split(base64_encode($message));

    //attachment
    $body .= "--$boundary\r\n";
    $body .="Content-Type: $type; name=".$name."\r\n";
    $body .="Content-Disposition: attachment; filename=".$name."\r\n";
    $body .="Content-Transfer-Encoding: base64\r\n";
    $body .="X-Attachment-Id: ".rand(1000, 99999)."\r\n\r\n";
    $body .= $encoded_content; // Attaching the encoded file with email

    $sentMailResult = mail($recipient_email, $subject, $body, $headers);

    if($sentMailResult )
    {
       echo "File Sent Successfully.";
       unlink($name); // delete the file after attachment sent.
    }
    else
    {
       die("Sorry but the email could not be sent.
                    Please go back and try again!");
    }
}
```

PHP 是一种专门为 Web 开发设计的服务器端脚本语言。 您可以按照这个[PHP 教程](https://www.geeksforgeeks.org/php-tutorials/)和[PHP 示例](https://www.geeksforgeeks.org/php-examples/)从头开始学习 PHP。