
[返回](../../helpers.md)

打开 `SciTEGlobal.properties`，并添加下列行，

```
ext.lua.startup.script=$(SciteDefaultHome)/see_ascii_selection.lua

#print selection info
command.33.*=PrintSelectionInfo
command.subsystem.33.*=3
command.mode.33.*=savebefore:no
command.shortcut.33.*=F1

# User defined key commands
user.shortcuts=\
F1|1133|\
Ctrl+Shift+V|IDM_PASTEANDDOWN|\
Ctrl+PageUp|IDM_PREVFILE|\
Ctrl+PageDown|IDM_NEXTFILE|
```

在 SciTE 目录中创建一个称为 `see_ascii_selection.lua` 的文件，带上下列内容，

```
function PrintSelectionInfo()
   local sel = editor:GetSelText()
   print(#sel..' chars selected')
   print(table.concat({sel:byte(1,-1)},','))
end
```

现在，你可以在 SciTE 中编辑任何文件的时候按 F1 来查看选择内容下的符号的 ASCII 代码。

基于 Egor Skriptunoff [在这里](https://stackoverflow.com/questions/21603285/scite-lua-scripting-extension-api-beginner)编写的一个脚本。
