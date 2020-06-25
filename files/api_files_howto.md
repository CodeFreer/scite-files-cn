
[返回](api_files.md)

<a name="how_to_install_api"></a>
### 如何安装一个 api 文件并启用调用提示+补全

* 作为示范，让我们安装用于 C 标准库的 API 文件

* 下载 [c.api](./files/api_files/c.api)

* 把 `c.api` 移到包含 SciTE 的目录中。 在 Linux 中，这通常是 `/usr/bin/scite` 或 `/usr/local/bin/scite`

* 打开 SciTE

* 从 Options (选项)菜单中，选择 Open User Options File (打开用户选项文件)

* 添加一行 `api.$(file.patterns.cpp)=$(SciteDefaultHome)/c.api`

* 添加一行 `calltip.cpp.use.escapes=1`

* 添加一行 `calltip.cpp.word.characters=$(chars.alpha)$(chars.numeric)_`

* 保存这个文件并重启 SciTE

* 在 SciTE 中，开始一个新文件并把它另存为 "test.c"

* 调用提示

    * 键入文本 "fprintf("
    
    * 当你按下 (，会出现一个调用提示，显示用于 "fprintf" 的文档
    
    * 你可以通过点击 ( 右侧并按 Ctrl+Shift+Space 可以再次显示调用提示工具提示
    
* 补全

    * 在空行上，键入文本 "fp" 并按下 Ctrl+Space
    
    * 出现一个列表框让你在 fprintf, fputc 和 fputs 之间选择
    
    * 你可以使用箭头键导航这个框并按回车从这个框中选择一项


<a name="how_to_install_properties"></a>
### 如何安装一个 properties 文件

* 一个 .properties 文件可以更改颜色和字体，指定关键字的列表，定义在“编译”和“运行”时采取的动作，映射文件扩展名到一种编程语言，等等

* 要安装一个 properties 文件，只需移动 .properties 文件到包含 SciTE 的目录中。 在 Linux 中，这个通常是 `/usr/bin/scite` 或 `/usr/local/bin/scite`

* 如果需要，那么你可以基于你的配置编辑 properties 文件。例如，你已安装了多个不同版本的 Python。 你可以打开 SciTE，并从 Options (选项)菜单中选择 `Open python.properties`(打开..)。 在文件底部，你可以看到用于 `command.go.*.py` 的定义。如果，譬如说，你想按 F5 让 SciTE 运行一个使用 Python 3.7 的 Python 脚本，你可以更改该行为 `command.go.*.py=C:\python37\pythonw -u "$(FileNameExt)"`

### 更多细节

```
你有两种主要方式可以告知 SciTE 要加载哪些 properties 文件。

1) 
# (SciTE 按默认使用这个)
# 在 SciTEGlobal.properties 中，
imports.exclude=(要跳过的 properties 文件的列表)
# 导入这个目录中所有专用语言的 properties 文件
import *

2) 
# 要加载内容的一个显式列表。
# 在 SciTEGlobal.properties 中，
import myprop1
import myprop2
# 等
# import myprop1 导入行
# 查找一个名为 myprop1.properties 的文件并使用这种方式加载它，
# 可以使用相对目录
# 如果使用这种方式，要安装一个 properties 文件，你将必须添加一行
# import mypropfile
# 来开始使用文件 mypropfile.properties

这里是如何配置自动补全和调用提示的一些示例，

# 如果你按下 ctrl-space 并只有一个单词匹配的话，
# 那么我们是否应该跳过显示菜单而只需插入该词呢?
autocomplete.cpp.choose.single=0

# 是否区分大小写匹配?
autocomplete.cpp.ignorecase=0

# 启用包含超过一行信息的调用提示，推荐使用 \n. 。
calltip.cpp.use.escapes=1

# 当键入这个字符时自动开始自动补全，见下文
autocomplete.cpp.start.characters=

# 哪些单词可以作为一个单词的一部分?
calltip.cpp.word.characters=$(chars.alpha)$(chars.numeric)_

# 哪个字符开始一个参数列表(例如，开始一个函数调用的内容)
calltip.cpp.parameters.start=(

# 哪个字符间隔一个列表的参数(例如，在一个函数调用中)
calltip.cpp.parameters.separators=,

# 是否匹配大小写?
calltip.cpp.ignorecase=0

# 终止字符
calltip.cpp.parameters.end=)
calltip.cpp.end.definition=)

# 例如，用于 HTML 和 CSS 的调用提示可以是,
autocomplete.hypertext.ignorecase=1
calltip.hypertext.ignorecase=1
calltip.hypertext.word.characters=_$(chars.alpha)$(chars.numeric)$:>
calltip.hypertext.end.definition=) 
calltip.css.word.characters=-$(chars.alpha)$(chars.numeric)
calltip.css.parameters.start=:
calltip.css.parameters.end=
calltip.css.parameters.separators=|

编写 API 文件时的一个提示:
如果该语言拥有来自一个命名空间的函数调用，譬如 "File.WriteAllText()"，
那么让 API 文件对每个函数拥有两个条目可能更好，
一个条目用于自动补全方法，
File.WriteAllText
而另一个条目用于调用提示，
WriteAllText(string path, string contents)\n\tDescription: Creates a new file

然后你可以设定 start.characters 为 "."，
autocomplete.(current lexer).start.characters=.
然后，当你键入 "File." 时，将会自动显示该建议

你可以一次添加多个 API 文件，如
api.$(file.patterns.cpp)=/path/to/first.api;/path/to/second.api

```
