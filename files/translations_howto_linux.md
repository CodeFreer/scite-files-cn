
<a name="how_to_install_translation_linux"></a>
### 如何安装一个翻译 (Linux)

* 在[这里](translations_list.md)访问翻译的列表。

* 右击链接之一并选择"保存链接为..." 或 "保存目标为..."

   <a href="#">![右击链接截屏](./translations_install_linux_right.png)</a>

* 保存到一个可写的目录，譬如 ~/Downloads.

   <a href="#">![保存到下载截屏](https://raw.githubusercontent.com/CodeFreer/scite-files-cn/master/files/translations_install_linux_path.png)</a>

* 打开中断，使用 sudo ，把文件移到 `/usr/share/scite/locale.properties`

   <a href="#">![保存到下载截屏](https://raw.githubusercontent.com/CodeFreer/scite-files-cn/master/files/translations_install_linux_terminal.png)</a>

* (注意，目标文件名是 locale.properties)。如果 `/usr/share/scite` 不存在，尝试 `/usr/local/share/scite`。

* 重新打开 SciTE.exe，而菜单和对话框将会显示翻译的文本

* (总之，文件的名称必须是 locale.properties 并且应该放置在和 SciTEGlobal.properties 同一目录中)

[返回](translations.md)
