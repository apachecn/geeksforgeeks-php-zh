# 是什么。PHP 中的 htaccess 文件？

> 原文:[https://www.geeksforgeeks.org/what-is-htaccess-file-in-php/](https://www.geeksforgeeks.org/what-is-htaccess-file-in-php/)

那个。htaccess(超文本访问)文件是一个 Apache 分布式服务器配置文件。您可以使用。htaccess 文件为特定目录设置服务器配置。该目录可以是网站的根目录，也可以是。创建 htaccess 文件是为了启用该子目录的额外功能。

您可以使用。htaccess 文件来修改各种配置，从而对您的网站进行更改。这些更改包括授权、错误处理、特定 URL 的重定向、用户权限等。像任何其他 Apache 配置文件一样。从上到下读取 htaccess 文件。也就是说，上面的配置在下面的配置之前执行。

**的常见用法。htaccess 文件:**

**1。更改默认起始页:**假设您想用其他 HTML 页面(例如 home.html)更改您的主页(例如 index.html)，同时保持 index.html 文件不变，您可以通过在中添加以下代码来更改默认登录页。htaccess 文件。

```
DirectoryIndex home.html
```

在配置文件中，也可以添加多个文件。在这个例子中，首先，服务器将检查 index.html，如果它没有找到具有该名称的文件，它将继续到 home.htm，以此类推。

```
DirectoryIndex index.html home.html config.php
```

**2。阻止特定的 IP 或 IP 范围:**您也可以阻止特定的 IP 地址或 IP 地址范围访问您的网站。为此，您需要将这些行添加到。htaccess 文件:

*   **拒绝特定 IP:** 通过使用此模板，您可以阻止任何所需的 IP 地址

    ```
    Order Deny,Allow
    Deny from 192.206.221.140 
    (Here 192.206.221.140 is a specific IPv4 Address)
    ```

*   **拒绝 IP 列表:**通过逐行列出 IP 地址，您可以阻止一组 IP 地址。

    ```
    Order Deny,Allow
    Deny from 185.120.120.120
    Deny from 192.190.190.190
    ```

*   **拒绝来自特定域的访问:**假设您想拒绝来自特定域(例如 www.redirectingdomain.com)的对托管网站的访问，该域包含指向您网站的链接，在这种情况下，您可以在中使用下面的代码。htaccess 文件。点击 redirectingdomain.com

    ```
    SetEnvIfNoCase Referer "redirectingdomain.com" bad_referer
    Order Allow,Deny
    Allow from ALL
    Deny from env=bad_referer
    ```

*   **的链接会显示 403 禁止错误阻止或允许 IP 地址范围:**

    ```
    Order Allow,Deny
    Deny from 192.192.*.*
    Allow from all
    ```

    其中*用于整个八位字节

**注意:**要限制来自某些国家的访问，您必须获得分配给该特定国家的 IP 地址范围。需要注意的是，这种方法不是 100%有效，因为 IP 地址分配可能会改变，并且 IP 地址范围可能会重叠。即便如此，这种方法也阻挡了来自特定国家的大部分流量。

**3。301 永久重定向:** 301 是从网络服务器到您的网络浏览器的 HTTP 响应代码。301 状态代码表示所请求的资源已被永久移动到新的网址。当页面不再相关或页面被删除时，301 重定向非常有用。您可以使用下面的代码来应用 301 重定向。

```
RewriteEngine on
RewriteCond %{HTTP_HOST} ^domain1.com [NC,OR]
RewriteCond %{HTTP_HOST} ^www.domain1.com [NC]
RewriteRule ^(.*)$ http://domain2.com/$1 [L,R=301,NC]
```

也可以简单使用

```
Redirect 301 / http://domain.com
```

下面的代码

**4。WWW 到非 WWW 和非 WWW 到 WWW:** 由于搜索引擎认为“WWW”和“非 WWW”URL 是两回事，因此重定向来自非首选域的请求变得非常重要。让我们以“www . example . com”

*   为例，要使 301 从 www 重定向到非 www，您必须将以下代码添加到您的。htaccess 文件:

    ```
    RewriteEngine on
    RewriteCond %{HTTP_HOST} ^geeksforgeeks.com [NC]
    RewriteRule ^(.*)$ http://www.geeksforgeeks.com/$1 [L,R=301,NC]
    ```

*   如果要让 301 从非 www 重定向到 www 域添加以下代码:

    ```
    RewriteEngine on
    RewriteCond %{HTTP_HOST} ^www.geeksforgeeks.com [NC]
    RewriteRule ^(.*)$ http://geeksforgeeks.com/$1 [L,R=301,NC]
    ```

**5。从 HTTP 重定向到 HTTPS:**

为什么要将流量从 HTTP 重定向到 HTTPS？

主要有两个原因，一个是安全性，因为它确保用户数据从用户浏览器到网络服务器都是加密的，第二个原因是 SEO(搜索引擎优化)，因为 HTTPS 网站比 HTTP 网站具有更高的排名优势。如果你想把你的网站的全部流量从 HTTP 转移到 HTTPS，那你就需要在你的。htaccess 文件。

```
RewriteEngine On
RewriteCond %{HTTPS} !=on
RewriteRule ^(.*)$ https://%{HTTP_HOST}%{REQUEST_URI} [L,R=301,NE]
Header always set Content-Security-Policy "upgrade-insecure-requests;"
<IfModule mod_rewrite.c>
RewriteEngine On
RewriteBase /
RewriteRule ^index\.php$ - [L]
RewriteCond %{REQUEST_FILENAME} !-f
RewriteCond %{REQUEST_FILENAME} !-d
RewriteRule . /index.php [L]
</IfModule>
```

**6。自定义您的错误页面:**如果您想要自定义您的 404 错误页面，您可以在中定义您自己的自定义错误页面。htaccess 文件。只需将以下文本复制到您的。htaccess 文件。

```
# Example 1: redirect errors to html files
ErrorDocument 404 /404.html

# Example 2: redirect errors to PHP file
ErrorDocument 404 /error.php?q=404
```

**7。经过身份验证的文件夹:**出于身份验证的目的，您可以通过在中添加下面给出的代码来保护应用程序的目录。htaccess 文件。一旦。htaccess 文件已更新，您的目录需要用户名和密码才能访问。

```
AuthName "Your Authenticated Folder"
AuthUserFile /path/.htpasswd
AuthType Basic
require valid-user
```

这里，代码的第一行告诉 Apache 网络服务器，受密码保护的目录的名称是“您的已验证文件夹”。第二行告诉该文件夹的路径，下一行确定身份验证的类型，在本例中，我们使用的是 HTTP Basic 身份验证。最后，最后一行说我们需要有效的凭证。