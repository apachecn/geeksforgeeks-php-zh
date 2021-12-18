# PHP|输出缓冲

> Original: [https://www.geeksforgeeks.org/php-output-buffering/](https://www.geeksforgeeks.org/php-output-buffering/)

PHP 语言是一种解释型语言，也就是说，它是一条接一条语句执行的。 默认情况下，PHP 的一个特性使其在通过执行语句生成 HTML 后立即将其作为块发送；此特性使网页的加载变得细粒度，加载时间跨度可能以一种随意的方式出现。 以下示例可以是阻止广告拦截器或其他类似应用程序的网站的加载时间，其中内容首先加载，然后显示禁止广告拦截器查看内容的通知。

这就是输出缓冲发挥作用的地方。 通过使用输出缓冲，生成的 HTML 存储在缓冲区或变量中，并在执行 PHP 脚本中的最后一条语句后发送到缓冲区进行呈现。 这是一个显著的性能提升，同时也增加了网页的美学价值。 以下是使用输出缓冲的几个优点：

**输出缓冲的优点**

*   When output buffering is enabled, the developer reduces the number of interactions between the server and client browsers by sending the entire HTML at once, so output buffering provides a more time-saving way for larger projects.
*   Because the output buffer stores the entire HTML as a string, we can manipulate the HTML using all string methods or custom methods, providing more flexibility in rendering content.
*   We can also apply various compression methods to create more efficient rendering.
*   Using output buffering makes it easier to set up the cookie and process the session, because the rest of the page is not sent when the title information is sent.

**需要注意的重要事项**

*   As a medium-to-advanced theme, output buffering is not enabled by default.
*   Output buffering provides a faster, more secure, more flexible, less redundant rendering method. Output buffering also allows for advanced features such as minimizing and reducing database calls. Output buffering applies to cookie and sessions.
*   PHP provides an API to enable and access the output buffer. These methods will be discussed in future articles.