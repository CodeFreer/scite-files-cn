[返回](../README.md)

### 信息

* 一个[介绍使用 Lua 脚本添加功能到 SciTE](./files/helpers/adding_scite_features_with_lua.md), 阅读这个链接如何安装下面列表中的 .lua 脚本

### SciTE 的脚本

* [swapheader](./files/helpers/swapheader.lua) 从一个 .c 移到一个 .h。阅读[这个指南](./files/helpers/adding_scite_features_with_lua.md)中的"安装其他人的 Lua 脚本"一节了解安装说明。

* [autoblock.zip](./files/helpers/autoblock.zip) 由 Mario Ray M 提供的用于块补全的 lua 脚本。

* [查看选择内容的 ascii 代码](./files/helpers/see_ascii_selection.md)

* [smartpaste](./files/helpers/smartpaste.lua)，用于正确缩排粘贴的代码的 lua 脚本

* [scitecmd](http://www.frykholm.se/scitecmd.html) 从 Windows 命令行在 SciTE 中打开文件

* [SciTE Windows 上下文菜单](https://github.com/andreburgaud/wscitecm) 由 andre burgaud 提供

* [Orthospell](http://tools.diorama.ch/orthospell.html), SciTE 的拼写检查，基于 [luahunspell](https://code.google.com/p/luahunspell/)

* [extman](./files/helpers/extman.zip) 

    * 调度 scite 事件以便多个 lua 脚本可以同时安装而不会冲突。 你可能拥有多个不同的脚本，每个都需要响应 OnOpen 事件，而 extman 让每个脚本共存。

* [来自 SciTE 的即时 markdown 预览](./files/helpers/markdown.txt)

* [Mitchell 的 SciTE 工具](https://github.com/btakita/scite-tools)，包括 snippets.lua 的文本编辑工具

* [Serge Baranov 的脚本](./files/helpers/perlformatters.txt) 使用 Perl 来重新格式化/清理文档中的空白

* yipf 的 [SciTEStartup.lua](https://github.com/yipf/scite-files/blob/master/SciTEStartup.lua) 有一些有用的脚本用于自动闭合括号，当按下 Tab 时展开代码段，拼写检查，单词计数，移到一个句子的开始/结尾，诸如此类

* 我已[存档了 lua-users SciTE 脚本的目录](./files/helpers/lua-users-scite-scripts.zip) 使用时光机(wayback machine)来恢复大部分缺少的内容。包括许多用于 SciTE 的 lua 脚本，包括用于 AsciiTable, AutoCompleteAnyLanguage, AutoExpansion, BackupFile, BufferSwitch, Calculator, CleanDocWhitespace, CleanWhiteLines, ColouriseDemo, CommentBox, ConvertDecHex, CustomFolding, Debug, DeleteBlankLines, DisplayFunctions, EditWithVim, ElizaClassic, ExternalFileBrowser, ExtMan, Favs, FileBrowser, FuncList, HexEdit, Hexify, HtmlEntities, Indentation, InplaceCalculator, InsertDate, JavadocComment, Latex, LineBreak, ListAllOccurances, LuaDll, LuaPrompt, MacroExpander, MakeMonospace, ManPages, MarkWord, MergeOnChange, MiscScripts, NumberedBookmarks, OpenFilename, OpenPhpLocalhost, OpenToLine, OpenUrl, Other, ProcessString, Programmers, ProgrammingUtils, QuickStartXhtml, ReadTags, RunOneScript, ScriptManager, Scripts, SimpleTemplate, SortSelection, StripTrailings, TabsToSpacesObserveTabstop, Tags, TextFolding, TicTacToe, TitleCase, UnicodeInput, UsingUnicode, WordSelect, WordSubstitution 和 XmlAutocompletion 的脚本。原始的维基[在这里](http://lua-users.org/wiki/SciteScripts)

* 这里是[来自 my-scite 项目的一些 lua 脚本](./files/helpers/my_scite_scripts.zip) 包括 AutoComplete, Calculator, HexEdit, Socket 和 sortText。 myScite 还包括补全代码片段， orthospell 拼写检查器，经由 scintillua 的自定义语法解析器，调试/步进功能以及一个用于 lua 用户界面的侧栏。[myScite 项目](https://github.com/arjunae/myScite)了解更多。

* 这里是[来自 scite-ru 项目的一些 lua 脚本](./files/helpers/scite-ru-scripts.zip) 包括 move_lines, abbrevlist, ascii_table, auto_backup, auto_complete_object, change_comment_char, codepage, code_poster2, code_poster_html, color_set, copymarkedlines, css_formatter, event_manager, exec, find_text, fold_text, font_changer, goto_line, highlighting_identical_text, highlighting_text, highlight_links, html_tags_autoclose, indent_tab_to_space, insertspecialchar, lexer_name, luainspect_install, macro_support, make_abbrev, movemenuitem, new_file, open_selected_filename, open_find_files, paired_tags, readonly, recode, rename, restore_recent, rocheck, rowrite, save_settings, set_html, showcalltip, sidebar, smartbraces, smartcomment, sort_text, style_changer, svn_menu, translit, url_detect, value, xcomment 和 zoom

* 这里是[来自 scite_scripts 项目的  一些 lua 脚本](https://github.com/mkottman/scite_scripts) 包括 gitdiff, mark_word 和 xml_close_tag

* [Lua Exporters](./files/helpers/SciTELuaExporters-0.9.11.zip)  包括一个增强的 PDF 导出器(带换行和字距调整)，一个 OpenOffice.org 格式的导出器，一个 AbiWord 格式的导出器，和一个 ODT (Open Document) 导出器。

* Kein-Hong Man 已开发了在 SciTE 中运行的[计算器脚本](./files/helpers/scite_calculator.zip) 和 [hex 编辑器脚本](./files/helpers/scite_hexedit.zip)

### Lua 工具

为 SciTE lua 脚本构建块

* [moltenform_scite_utils.lua](./files/helpers/moltenform_scite_utils.lua) 和它的 [API 文档](./files/helpers/moltenform_scite_utils_api.md)

* [extman](./files/helpers/extman.zip)

* [来自 myscite 项目的一些 lua 实用工具](./files/helpers/my_scite_lua.zip) 包括从 lua 运行 COM，列出 lua 定义，解析 CTags，并添加基于每个项目的 CTags 支持，和代码片段。还有用于位操纵、类、md5、正则表达式的 lua 实用工具，以及 "serpent" 美化打印机。

* [scite_msg](./files/helpers/scite_msg.zip) 

    * 可以发送消息到 scite 窗口的命令行工具，由 Ben Fisher 开发(使用来自 scite_other 的一些代码)

* [scite_other](./files/helpers/scite_other.zip) 

   * 查找 SciTE 实例并给它发送一条消息，若找不到则启动一个新 SciTE 实例，由 Steve Donovan 开发
   
* [lua_shell_dll](./files/helpers/lua_shell_dll.zip)

    * 这个 lua 扩展库，位于和 scite 同一目录中，允许 scite lua 脚本调用:
    * `shell.msgbox` 显示带按钮的文本消息。
    * `shell.inputbox` 显示对话框用于输入某些文本值。
    * `shell.getfileattr`, `shell.setfileattr`, `shell.fileexists
    * `shell.exec` 一个不显示窗口的更漂亮的 'exec' (用于启动一个进程)
    * `shell.findfiles` 使用掩码搜索文件和文件夹，并按表格返回结果。

* [scite_lua_startprocess](./files/helpers/scite_lua_startprocess.zip) 

    * 这个 lua 扩展库，位于和 scite 同一目录中，允许 scite lua 脚本调用:
    * `shell.exec` 一个不显示窗口的更漂亮的 'exec' (用于启动一个进程)
    
* [SciTE.Helper](./files/helpers/SciTE.Helper.zip) 

    * 一个可以发送消息给 scite 的 ActiveX 控件，可以被 jscript/vbscript 也可能一个 hta 用户界面所使用
    
* [scite-strip-wrapper](https://github.com/klonuo/scite-strip-wrapper) 显示如何在 SciTE 中添加带式对话框，以便你的 lua 脚本可以显示用户界面

### Gui 附加组件/补丁

* [sciteproj](https://savannah.nongnu.org/projects/sciteproj/), 用于 SciTE 的项目管理器

* [SciTE 侧栏扩展](http://valentin.dasdeck.com/projects/scite_sidebar/)，添加标签页用于打开文件、FTP、函数等等

* [hilfer](https://rubygems.org/gems/hilfer/), 使用和 SciTE 对话的 ruby-gtk 的 keyboard-rich (键盘功能丰富)目录浏览器

* [Steve D 的 SciTE-GUI](https://groups.google.com/forum/#!topic/scite-interest/yZubpejP-bM) 扩展，用于 SciTE Lua 来添加列表、文件和颜色对话框，浮动工具栏等

* [scite-gui](https://github.com/frank-w/scite-gui) 用于更改 SciTE 设置的 GTK 工具，最后更新于 2010

* [示例 Ruby 扩展](https://groups.google.com/forum/#!topic/scite-interest/cl6DogvZz2k)

### 添加到本页

你可以通过添加 pull 请求或者发送电邮给 scitewiki at gmail dot com 来添加到本页

