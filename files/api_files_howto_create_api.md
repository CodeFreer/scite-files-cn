
[返回](api_files.md) 

<a name="how_to_make_api"></a>
### 如何制作一个 API 文件

API 文件就是具有每行一个条目格式的纯文本文件。

例如，用于 C 标准库的 API 文件可能看起来这样，

```
abort();
abs(int n);
acos(double x);
asctime(const struct tm* tp);
```

如果启用 use.escapes，那么信息可以跨多行，例如，

```
abort() Param: ()\t\nDesc: Abort current process
abs(double x) Param: (Value whose absolute value is returned.)\t\nDesc: Compute absolute value
acos(double x) Param: (Value whose arc cosine is computed, in the interval [-1,+1].)\t\nDesc: Compute arc cosine
```

要生成用于你自己的源代码的 API 文件，这些工具可能会有用:

* 对于 C/C++ 头文件，生成 API 文件可以使用 [ctags](http://ctags.sourceforge.net/) 然后在 tags 文件上使用 [tags2api](./files/api_files_gen/tags2api.py) Python 脚本(它假定是 C/C++ 源代码)来收集完整的多行函数原型。一些常见的头文件使用一个 \__P 宏围住参数列表，并可能有注释。[cleanapi](./files/api_files_gen/cleanapi.cc) 工具可能在这些文件上使用
* 对于 Python，有一个 [gen_python_3_api](./files/api_files_gen/mpheath_gen_python_3_api.py) 脚本(还有较旧的脚本用于 [python3](./files/api_files_gen/gen_python_3_api.py) 和 [python2](./files/api_files_gen/gen_python_api.py)。)
* 对于 Java 类，有一个 [java_apibuilder.zip](./files/api_files_gen/java_apibuilder.zip) 程序
* 对于 C# 类，使用 [genapi.cs](./files/api_files_gen/gen_csgenapi.zip)
* 对于 PHP，使用 [php-api-generator](./files/api_files_gen/gen_php-api-generator.zip) 或 [phpapi.php](./files/api_files_gen/phpapi.php.txt)
* 用于最新 PHP 标准库的 API 文件可以使用[这里](./files/api_files_gen/gen_php-from-online-docs.zip)的工具生成，由 arjunae 贡献
* 用于最新 C++ 标准的 API 文件可以使用[这里](./files/api_files_gen/gen_cpp_cplusplusdotcom.zip)的脚本生成
* 用于最新 jquery 的 API 文件可以使用[这里](./files/api_files_gen/gen_jquery.zip)的脚本生成
* 用于最新 javascript (来自 MSDN) 的 API 文件可以使用[这里](./files/api_files_gen/gen_msdn_javascript.zip)的脚本生成
* 用于最新 wsh/vbs/vba (来自 MSDN) 的 API 文件可以使用[这里](./files/api_files_gen/gen_msdn_wsh_vba.zip)的脚本生成

按照[这里](api_files_howto_install_api.md)的说明激活一个 API 文件

要查看更高级的设置，搜索 [SciTE 文档](http://www.scintilla.org/SciTEDoc.html)中的"calltip"(调用提示)
