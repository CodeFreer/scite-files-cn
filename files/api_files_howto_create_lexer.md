
[返回](api_files.md)

### 为一个新语言添加加亮/折叠

如果该语言和 SciTE 已支持的一种语言足够相似的话，那么你可以复制用于那种语言的 properties 文件并更改它以匹配你的新语言。

如果这样不行的话，那么你可以编写一段代码，SciTE 称之为 "lexer"(词法分析器)。

* 词法分析器定义如何添加语法加亮和/或折叠

* 这比真正解析用户正在编辑的文件要简单得多。

* 在最新版本的 SciTE 中，可以用 Lua 语言编写一个词法分析器(更简单且不需要 C++ 编译器)

* [使用 Lua 语言编写一个词法分析器](https://www.scintilla.org/ScriptLexer.html)上的文档

* Andreas Tscharner 的有关添加[语法加亮和代码折叠](./files/api_files_new_lexer/newlexertutorial.pdf)的教程，以及使用 C++ 的[示例代码](./files/api_files_new_lexer/newlexertutorialcode.tar.bz2)

