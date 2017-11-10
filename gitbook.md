Gitbook是一个命令行工具，可以把你的Markdown文件汇集成电子书，并提供PDF等多种格式输出。你可以把Gitbook生成的HTML发布出来，就形成了一个简单的静态网站。Gitbook还有一个同名的平台（gitbook.io），可以发布和销售电子书，并提供了一个Markdown客户端工具（支持Mac、Windows和Linux）帮助写作。以下是我在使用Gitbook中的笔记。

首先Gitbook和Git/Github都没有什么关系。它只是一个build book的工具而已。但它的Git前缀的确引起了许多人的迷惑，起初我认为至少它也是个和Github类似的Git平台吧，但其实没什么关系，你只要懂几条markdown语法，不必理解任何与Git相关的东西就能用Gitbook了，不要为其名字迷惑。

第0步 安装npm（Node Package Manager）。从node.js的官网上下载安装程序，即可完成Node.js和npm的安装。

第1步 通过npm安装Gitbook。

$ npm install gitbook -g
完成后花10分钟阅读下Gitbook的帮助文档。如果你没耐心看手册，那就继续往下读吧 :D

第2步 了解Gitbook的基本规则。

Gitbook需要2个基本文件：

README.md
SUMMARY.md
README.md是关于你的书的介绍，而SUMMARY.md中则包含了书目，即章节结构，它的格式大致是：

* [第1章](c1.md)
 * [第1节](c1s1.md)
 * [第2节](c1s2.md)
* [第2章](c2.md)
剩下的东西就很好理解了，你只需要编写相应章节即可。在编辑完README.md和SUMMARY.md后，你可以运行以下命令：

$ gitbook serve -p 8080 .
Gitbook首先把你的Markdown文件编译为HTML文件，并根据SUMMARY.md生成书的目录。所有生存的文件都保存在当前目录下的一个名为_book的子目录中。完成这些工作后，Gitbook会作为一个HTTP Server运行，并在8080端口监听HTTP请求。

运行以上命令后，打开浏览器，在地址栏输入：http://localhost:8080即可看到你的书页了。

其中位于左侧书目顶部的Introduction一节就编译自README.md，而书目本身自编译自SUMMARY.md。你要在自己的网站上发布新书，只需把_book目录复制到服务器相应目录即可。至此Gitbook的基本用法就介绍完毕。

Gitbook 格式的文档，也可以转为 PDF 格式。
