# Kotlin简介
Kotlin 是一种非常适合开发服务端应用的语言，因为它语法简洁，运行高效，并且能够和Java技术完全的兼容。更重要的是，它的学习曲线也很平滑。

## Kotlin具体有哪些优势呢？
1. Expressiveness（表现）：Kotlin有自己独具特色的语言特性。例如：它支持 type-safe builders（以半声明的方式定义数据）和 delegated properties（这个是什么？？没仔细看）来帮助
开发者建立强大，易于使用且抽象化程度高的应用。

2. Scalability（直接翻译：可测量性。自己理解~~~） ：Kotlin支持 coroutines （协程），类似线程，但是和线程不一样，它更轻量。 coroutines 可以帮助后端开发人员处理客户端数量大或者客户端硬件
性能一般的情况。

3. Interoperability（互操作性）：kotlin和Java完全兼容，完全兼容，完全兼容，重要的事情说三遍。所以如果你是一名Java开发者，那么kotlin可以让你在熟悉的技术栈中体验到现代编程语言所带来的非一般的体验。

4. Migration（迁移）：和第三条有联系，也就是说如果当前的项目是Java，但是想换成kotlin。那么这个时候可以先写kotlin，慢慢的迁移，因为他们是兼容的。

5. Tooling（工具）：IDEA Ultimate对kotlin有很强大的支持。

## 支持kotlin的服务器端开发框架
1. spring：从5.0开始spring充分利用了kotlin的语言特性，允许用kotlin快速生成一个新的项目。
2. Vert.x：一种可以构建reacttive（交互）web的并且在JVM上运行的框架，它为kotlin提供了专门的支持，并且提供了全文档。
3. Ktor ：他是被JetBrains公司构建的一种kotlin原生的web框架。为了高的scalability ，它充分使用了coroutines （协程）。并提供了易于使用且符合开发人员使用习惯的API。
4. kotlinx.html：它是一种DSL（DSL的全称是domain-specific language，常见的有HTML,Shell,XML等），它可以替代传统的web模板，如 JSP 和 FreeMarker。

## kotlin服务端应用程序的发布
kotlin服务端的应用可以发布到任何支持Java程序的主机上，如Amazon Web Services， Google Cloud Platform等等。


>本文目的：大概了解kotlin是什么，有什么优势和特点。