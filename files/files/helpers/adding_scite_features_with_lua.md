
## 如何使用 Lua 添加 SciTE 功能

由 Ben Fisher 于 2018 年提供。 首先，这里是入门的逐步指南。

* 下载 SciTE

* 打开包含 SciTE 的目录。 在 Linux，这个通常是 /usr/bin/scite

* 创建一个称为 "scripts" 的子目录

* 在 "scripts" 目录中创建一个新文件，称为 "example.lua"

* 输入下列文本到 example.lua 中，

```
print('moving to the start')
editor:GotoPos(0)
```

* 打开 SciTE

* 从“选项”菜单中选择“打开用户选项文件”，这将会打开称为 SciTEUser.properties 的文件

* 添加下列行到 SciTEUser.properties

```
command.name.9.*=my lua example
command.mode.9.*=subsystem:lua,savebefore:no
command.9.*=dofile $(SciteDefaultHome)/scripts/example.lua
```

* 在 SciTE 中创建一个新文件并键入一些单词。在“工具”菜单中，你现在应该会看到 "my lua example"。如果你点击“工具”菜单中的“my lua example”，它将会运行我们的 lua 脚本。文本 "moving to the start" 将显示在右侧的输出窗格中，而当前位置将被发送回到文档的开始处，就像你按了 Home 键，因为我们的脚本告诉 SciTE 要 `GotoPos` 0。

## 更多关于 .properties 文件的信息

在一个 .properties 文件中，你可以指定一个"命令"。命令可以运行程序、打开文件，或者我们的例子中一样，运行一个 lua 脚本。

在这一行

```
command.name.9.*=my lua example
```

\* 符号代表该命令适用于哪些文件扩展名。如果该行被更改为 command.9.\*.py，那么该命令将只会在 SciTE 在编辑 .py 文件时激活。 一个纯 \* 意味着该命令针对每个文件类型激活。

数字 9 代表命令编号。 例如，如果你要添加一个新脚本，那么你可以添加这种形式 `command.name.8.*=...` 或 `command.name.10.*=...` 的行，只要你不再使用 9 。

如果该命令是在 1 到 9 之间，那么命令 1 可以通过按 Ctrl-1 启动，2 则使用 Ctrl-2，如此类推。所以我们可以按 Ctrl-9 运行我们的例子。

你也可以为该命令指定你自己的快捷键，例如通过添加该行: `command.shortcut.9.*=Ctrl+Shift+J`

你可以通过添加类似下面的一行来添加一个命令到上下文菜单(该菜单在右击时出现): `user.context.menu=my lua example|1109|` (我们键入 1109 因为这是 1100 (第一个工具命令) 和 9 (我们项运行的该工具的命令号) 的和)。

## 安装其它人的 Lua 脚本

如何安装一个 Lua 脚本，例如在 [helpers](../../helpers.md) 页面中列出的一个脚本。在这个例子中，我们正在安装 gusnan 的 switch-from-cpp-to-header 脚本。

* 执行上面的第一节的步骤来安装 "my lua example"。

* 下载 [swapheader.lua](./swapheader.lua)

* 把 `swapheader.lua` 放入先前提及的 `scripts` 目录中。

* 从“选项”菜单中选择“打开用户选项文件”，这将会打开称为 SciTEUser.properties 的文件

* 添加下列行到 SciTEUser.properties

```
command.name.20.*=Swap C / Header
command.20.*=dofile $(SciteDefaultHome)/scripts/swapheader.lua
command.subsystem.20.*=3
command.mode.20.*=savebefore:no
command.shortcut.20.*=F11
```

* 现在，如果你正在编写 C 代码，你可以按 F11 在 myfile.c 和 myfile.h 之间切换

(某些脚本使用 "extman" 来注册事件。或者说，如果该脚本拥有类似 `AddEventHandler('OnOpen', ...)` 的代码，这个可以使用 `require('extman') ... scite_OnOpen(...)` 替换，参考下面的"Register for events"(注册事件)章节。


## 编写 Lua 代码

脚本是使用 Lua 语言编写的。

我已经编写了一个小的封装工具脚本，让它更容易从 Lua 中引导 SciTE。

* 执行在上面第一节中的步骤来安装 "my lua example"。

* 下载 [moltenform_scite_utils.lua](./moltenform_scite_utils.lua)

* 把 `moltenform_scite_utils.lua` 放置到先前提及的 `scripts` 目录中。

* 打开先前创建的 `example.lua` 文件，并更改它读取

```
require('scripts/moltenform_scite_utils')

-- printing to the output pane without a newline
ScApp:Trace('a')
ScApp:Trace('b')
ScOutput:PaneAppend('a')
ScOutput:PaneAppend('b')

-- getting/setting SciTE properties
print('\n current value of find.use.strip = '..ScApp:GetProperty('find.use.strip'))
ScApp:SetProperty('find.use.strip', '0')

-- opening a new document
ScApp:menunew()
require('scripts/moltenform_scite_utils') -- remember to re-import after changing document

-- adding text to the document
ScEditor:PaneWrite('abcdefg')

-- set selection
ScEditor:SetSel(2,5)
print('sel starts at ' .. ScEditor:GetSelectionStart())
print('sel ends at ' .. ScEditor:GetSelectionEnd())
print('selected text is ' .. tostring(ScEditor:GetSelText()))
print('length of this line is ' .. ScEditor:LineLength(0))
ScEditor:DocumentEnd()

-- underline chars 2 to 5
local underline = 4
local prev_indic = ScEditor:GetIndicatorCurrent()
ScEditor:SetIndicatorCurrent(underline)
ScEditor:IndicatorFillRange(2, 3)
ScEditor:SetIndicatorCurrent(prev_indic)

```

打开 SciTE，转到“工具”菜单，并选择 "my lua example"，则该代码将运行。 一些字母现在将会由一个红色下划线，作为脚本可以做的事情的例子。

[moltenform_scite_utils 的完整 API](moltenform_scite_utils_api.md)

请注意，每当打开一个不同的文档，则 lua 的全局状态就会被重置。 这是为何在任何对 `ScApp:OpenFile` 或 `ScApp:menunew` 的调用后，你需要再次 `require` (请求)所有脚本依赖关系。

Lua 的内建 `os.execute` 函数可以用于运行一个外部程序。(不过在 Windows 中， os.execute 有时会在屏幕上短暂显示一个 cmd.exe 实例的闪动，它看起来让人分心。对这个的一个解决方法就是 [scite_lua_startprocess](./scite_lua_startprocess.zip) 助手程序。) 

Lua 的标准库是受限的。 添加功能的一个方法就是编写一个 C 扩展，就像前面所述的 lua\_startprocess。 另一个选项就是使用我的 SciTE 分支版 [SciTE-with-Python](https://github.com/moltenform/scite-with-python)，它使用 Python 代替 Lua，因为 Python 更大的标准库和生态系统，以及附带许多[插件](https://github.com/moltenform/scite-with-python/wiki/Features)。 Lua 代码可以通过添加代码到 'lua startup script' 在 SciTE 启动时运行; 查看下面的例子。

## 注册事件

一个 lua 脚本也可以监听 SciTE 中的事件，并在事件被触发时运行代码。 这里是如何配置这个的例子:

* 执行上面的"编写 Lua 代码"一节中的步骤。

* 下载 [extman](./extman.zip)，解压它，并把 extman.lua 放置到你早前创建的 "scripts" 目录中。 (和其它 extman 脚本不同，这个版本的 extman 将不会自动搜索并运行所有 lua 脚本)。

* 从“选项”菜单中选择“打开用户选项文件”，这将会打开一个称为 SciTEUser.properties 的文件

* 添加下列行到 SciTEUser.properties

```
ext.lua.startup.script=$(SciteDefaultHome)/scripts/startup.lua
```

* 保存更改到 SciTEUser.properties 并重启 SciTE。 从“选项”菜单中选择“打开用户选项文件”，选择“打开 lua 启动脚本”。这将会制作一个称为 startup.lua 的文件

* 添加下列行到 startup.lua

```
require('scripts/extman')
require('scripts/moltenform_scite_utils')

local function notifyWhenTextFileOpened(filename)
    if stringendswith(filename, '.txt') then
        print('opening a text file ' .. filename)
    end
end

local function typingCapitalWTypesAnAInstead(key, shift, ctrl, alt)
    if key == string.byte('W') and shift and not ctrl and not alt then
        ScEditor:PaneWrite('A')
        return true -- stop normal handling
    end
end

scite_OnOpen(notifyWhenTextFileOpened)
scite_OnKey(typingCapitalWTypesAnAInstead)
```

* 保存更改到 startup.lua 并重启 SciTE

* 现在，当你打开一个 \.txt 文件时，你将会看到该消息，并在你键入 W 时，它会制作一个 A 来代替。

* 注意，该行 `return true` 是导致正常的事件处理被停止的原因; 没有这一行，W 仍将会出现。

如果在 Lua 启动脚本中定义了一个函数，那么它可以无需指定"dotfile"（点文件）即可通过一个命令调用; [这个脚本](./see_ascii_selection.md)用于显示选择内容中的 ASCII 字符就是一个例子。

("extman" 干什么? SciTE 只允许一个处理程序用于一个 Lua 事件， extman 调度事件到任意数量的调用者，允许不同的 lua 脚本都能被通知同一事件。) 可以在 extman 中注册的其它事件有:

| 注册一个事件的函数 |  |
| ------------- | ------------- |
| scite_OnMarginClick(fn) | 提供一个不接收参数的回调函数  |
| scite_OnDoubleClick(fn) | 提供一个不接收参数的回调函数  |
| scite_OnSavePointLeft(fn) | 提供一个不接收参数的回调函数  |
| scite_OnSavePointReached(fn) | 提供一个不接收参数的回调函数  |
| scite_OnChar(fn) | 提供一个提供一个回调函数，其中一个参数 "char"  |
| scite_OnSave(fn) | 提供一个回调函数，其中一个参数 "filename"  |
| scite_OnBeforeSave(fn) | 提供一个回调函数，其中一个参数 "filename"  |
| scite_OnSwitchFile(fn) | 提供一个回调函数，其中一个参数 "filename"  |
| scite_OnOpen(fn) | 提供一个回调函数，其中一个参数 "filename"  |
| scite_OnUpdateUI(fn) | 提供一个不接收参数的回调函数  |
| scite_OnKey(fn) | 提供一个接受 4 个参数 (key,shift,ctrl,alt) 的回调函数 |
| scite_OnDwellStart(fn) | 提供一个接受 2 个参数 (pos,string) 的回调函数 |
| scite_OnClose(fn) | 提供一个不接收参数的回调函数  |
| scite_OnStyle(fn) | 提供一个接受 1 个参数的回调函数  |
| scite_OnStrip(fn) | 提供一个接受 2 个参数 (controlNum, eventType) 的回调函数  |

## 为你的 lua 脚本添加一个 UI ("user strip")

* 执行上面“注册事件”一节中的步骤

* 打开 SciTE

* 从“选项”菜单中选择“打开用户选项文件”，这将会打开一个称为 SciTEUser.properties 的文件

* 添加下列行到 SciTEUser.properties

```
command.name.8.*=my gui example
command.mode.8.*=subsystem:lua,savebefore:no
command.8.*=dofile $(SciteDefaultHome)/scripts/userstrip_example.lua
```

* 在 `scripts` 目录中创建一个称为 `userstrip_example.lua` 的文件，并添加下列代码:

```
require('scripts/extman')
require('scripts/moltenform_scite_utils')
ScToolUIManager:RegisterEventWithExtman()

ExampleUIClass = inheritsFrom(ScToolUIBase)
function ExampleUIClass:AddControls()
    local callbackOk = function() self:OnOK() end
    local callbackGo = function() self:OnGo() end
    self:AddLabel('A label')
    self.idCombo = self:AddCombo()
    self.idBtnGo = self:AddButton('Go', callbackGo)
    self:AddRow()
    self:AddLabel('Name:')
    self.idEntry = self:AddEntry('default name')
    self:AddButton('OK', callbackOk, true, true)
    self:AddButton('Cancel', nil, true, false)
end

function ExampleUIClass:OnOpen()
    self:SetList(self.idCombo, 'pear\nlemon\norange')
    self:Set(self.idEntry, 'default name')
    self:Set(self.idCombo, 'default food')
end
    
function ExampleUIClass:OnGo()
    print('clicked Go, val='.. self:Get(self.idCombo) ..', entry='.. self:Get(self.idEntry))
end
    
function ExampleUIClass:OnOK()
    print('clicked OK, val='.. self:Get(self.idCombo) ..', entry='.. self:Get(self.idEntry))
end

local instance = ExampleUIClass:create()
instance:Init()
instance:Show()

```

*  保存并重启 SciTE

* 在 SciTE 中创建一个新文件并键入一些单词。 在“工具”菜单中，你现在可以看到 "my gui example"。如果你点击“工具”菜单中的“my gui example”，那么该用户工具带用户界面应该会出现在窗口的底部，而你现在可以通过点击按钮来进行交互。

* 如果你点击 ok 或 cancel，该用户界面将关闭。

用户工具带的进一步文档: 要使用 moltenform_scite_utils 显示用户带 UI，创建一个从 ScToolUIBase 继承的类，就如在该例子中所见。 然后下列方法可供使用:

| Method |  |
| ------------- | ------------- |
| instance:Show() | 显示 user strip  |
| instance:Close() | 关闭 user strip  |
| instance:AddControls() | 改写这个方法来绘制你的 UI  |
| instance:OnOpen() | 改写这个方法来进行设置，例如设置默认值 |
| instance:AddLabel(text) | 添加一个标签，返回这个控件的 ID; 应该只在 AddControls() method方法中被调用。  |
| instance:AddButton(text, callback, closes, default) | 添加一个按钮，并在点击按钮时回调。如果 `closes` 为 true，那么按钮将关闭 user strip。 如果 `default` 为 true，那么该按钮将拥有一个带有较厚边框的"默认"样式。 返回这个控件的 id; 应该仅在 AddControls() 方法中被调用。 |
| instance:AddCombo() | 添加一个组合框。 之后使用 setlist() 来填充内容。 返回这个控件的 ID; 应该仅在 AddControls() 方法中被调用。 |
| instance:AddEntry() | 添加一个文本条目框。之后使用 set() 来填充内容。返回这个控件的 ID; 应该仅在 AddControls() 方法中被调用。 |
| instance:AddRow() | 添加新行。 |
| instance:Get(controlId) | 获取在一个组合框或文本条目框中的当前值  |
| instance:Set(controlId, val) | 在一个组合框或文本条目框中设定当前值  |
| instance:SetList(controlId, val) | 设置一个组合框中的选项，数值用 \n 新行符间隔  |
| instance:OnEvent(controlId, eventType) | (可选)你可以改写这个方法来接收低级的事件。 eventType 通常是下列值之一: self.eventTypeClicked, self.eventTypeChange, self.eventTypeFocusIn 或 self.eventTypeFocusOut  |

(如果对这里的信息有疑问或者评论，可以在 scitewiki at gmail dot com 联系我。)

