# [将网页转换为机器可读数据的3个步骤](https://blog.webhose.io/2017/10/30/3-steps-to-turn-webpages-into-machine-readable-data/)

由[ Eran Levy	](https://blog.webhose.io/author/eran/)于2017年10月30日发表

[![阅读文章](https://blog.webhose.io/wp-content/uploads/2017/10/acquiring-web-data-688x308.png)](https://blog.webhose.io/2017/10/30/3-steps-to-turn-webpages-into-machine-readable-data/)

我们绝大多数人每天都使用网络 - 用于新闻，购物，社交以及您可以想象的任何类型的活动。但是，当[从网络](https://webhose.io/online-data-acquisition)上[获取数据](https://webhose.io/online-data-acquisition)用于分析或研究目的时，您需要开始以更技术性的方式查看Web内容 - 将其分解为由其组成的构建块，然后将它们重新组合为结构化的，机器可读数据集。

在这篇文章中，我们将介绍将文本Web内容转换为数据的三个基本步骤 - 无论您选择应用什么样的[提取技术](https://blog.webhose.io/2017/09/07/how-to-extract-data-from-websites-scraping-tools-diy-or-daas/)来执行此操作。这也应该有助于您了解您在讨论Web数据时常常听到的一些术语，从...开始

## 1.爬行

Web爬网程序（或蜘蛛程序）是一种自动访问网页的脚本或机器人，通常会创建其内容的副本以供以后处理。Web爬虫实际上是从网页抓取原始数据 - 最终用户在他或她的屏幕上看到的各种[DOM元素](https://www.w3schools.com/js/js_htmldom.asp) - 这是我们希望对这些数据采取的任何进一步行动的必要先决条件。

基本上，它是一个浏览网页并点击隐喻ctrl + a，ctrl + c，ctrl + v按钮的机器人。

搜索引擎，研究公司和数据提供商使用爬虫，这使得它们在网络上非常普遍。

通常情况下，爬虫不会停留在一个网页上，而是根据一些预定的逻辑在停止之前爬过一系列URL - 例如，它可能会跟踪它找到的每个链接，然后抓取该网站，然后按照链接进行操作发现那里......但是，您通常希望以更智能的方式进行爬网，优先考虑您抓取的网站数量与您可以投入任务的资源数量（存储，处理，带宽等）。

## 解析

通常，解析意味着从数据集或文本块中提取相关信息组件，以便以后可以容易地访问它们并用于其他操作。

在Web数据的上下文中，您的抓取工具通常会抓取一大堆HTML - 其中包括用户看到的文本以及针对浏览器有关如何呈现页面的大量指令，以及从中发送的各种相关信息。网站给最终用户。

要将网页转换为实际上对研究或分析有用的数据，我们需要以一种使数据易于根据定义的参数集进行搜索，分类和服务的方式进行解析。例如，Webhose.io将如何解析留言板帖子：

![img](https://blog.webhose.io/wp-content/uploads/2017/10/webhose-parsed-web-data.png)

### 等等，所以刮什么？

通常使用的刮擦基本上是此过程的前两个步骤 - 抓取网页并提取数据。这里的区别主要在于术语而不是本质。

## 3.存储和索引

最后，在获得所需的数据并将其分解为有用的组件之后，您可能希望找到一种可扩展的方法来将所有提取和解析的数据存储在数据库或集群中，然后创建一个允许结束的索引用户及时查找相关数据集或提要。

在Webhose.io的案例中，由于我们处理了相当大量的网络数据（由于我们提供的[高覆盖率](https://webhose.io/white-papers/100-web-coverage)），并且因为我们的客户自然期望持续的正常运行时间，我们在内部管理硬件基础设施 - 运行在我们自己的服务器场而不是AWS，Azure或类似的。对于索引，我们使用ElasticSearch。

## 结果：整齐有序的数据，准备分析

总结一下：将一段Web内容转换为机器可读数据是一个3步骤的过程。你必须发送你的机器人来抓取数据; 那么你必须将它解析成逻辑组件; 最后，你需要找到存储和索引的数据可扩展的方式，这样可以很容易地搜索和重新[特里](https://blog.webhose.io/2017/10/30/3-steps-to-turn-webpages-into-machine-readable-data/#)已经从它的具体信息。

如果您尝试从单个网站甚至一百个网站提取数据，这很简单 - 但要大规模地进行，需要一些专业知识并了解每个步骤中可用的技术障碍和优化。