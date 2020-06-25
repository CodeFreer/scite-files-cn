

* [返回](../README.md)
* [如何安装来自下表中的 .api 或 .properties 文件](api_files_howto.md) (以启用调式提示+补全)
* [如何为你自己的代码创建一个 .api 文件](api_files_howto_create_api.md)
* [如何为一个新语言添加加亮/折叠](api_files_howto_create_lexer.md)

### 语言

<!-- website refers to these, but I don't see them in properties: Clarion, Progress, Asymptote, TADS3, Gui4Cli, PL/M, PowerBasic -->
<!-- these lexers are available, but not referred to, set(['', 'SML', 'mysql', 'powerbasic','', 'kvirc', '', 'cppnocase', '', 'a68k', 'po', 'DMIS', '', 'bib', '', 'clarionnocase', 'tcmd', 'DMAP', 'PL/M', 'mssql', 'phpscript', 'clarion', 'fcST', 'magiksf', 'gui4cli', '']) -->
<!-- these lexers are available and just need to be turned on manually, as described below: markdown, visualprolog, tads3, progress , asy, literatehaskell, apdl -->

* HTML, CSS 和 JavaScript

    * HTML, CSS 和 JavaScript 默认情况下已启用加亮和折叠
    * [JavaScript API 文件](./files/api_files/javascript.api)
    * [JavaScript JQuery API 文件](./files/api_files/javascript_jquery.api) 和 [properties](./files/api_files/javascript.properties)
    * [css api](./files/api_files/css.api)
    * [html api](./files/api_files/html.api)

* Abaqus

    * 要启用加亮和折叠，打开 `SciTEGlobal.properties`，查找 `imports.exclude=`，删除 `abaqus`，然后保存并重启 SciTE

* ActionScript (Flash)

    * 默认情况下已启用加亮和折叠
    * [actionscript api](./files/api_files/actionscript.api)

* Ada

    * 默认情况下已启用加亮和折叠

* AMPL

    * [Properties 文件、api 文件、工具和设置说明](./files/api_files/ampl.zip)

* APDL

    * 在安装了下列属性文件后启用加亮和折叠
    * [APDL properties 和 API](./files/api_files/apdl.zip)

* Assembler (NASM/MASM)

    * 默认情况下已启用加亮和折叠
    
* Asl (ACPI 源代码)

    * 要启用加亮和折叠，打开 `SciTEGlobal.properties`，查找 `imports.exclude=`，删除 `asl`，然后保存并重启 SciTE

* ASN.1 MIB

    * 要启用加亮和折叠，打开 `SciTEGlobal.properties`，查找 `imports.exclude=`，删除 `asn1`，然后保存并重启 SciTE
    
* ASP

    * 默认情况下已启用加亮和折叠
    * [ASP API methods](./files/api_files/asp.api)
    * 编辑 html.properties 以设置 ASP 代码中的脚本的语言
        * 若 asp.default.language=1，在 ASP 代码块中的脚本是 JavaScript
        * 若 asp.default.language=2, 在 ASP 代码块中的脚本是 VBScript
        * 若 asp.default.language=3, 在 ASP 代码块中的脚本是 Python

* Asymptote

    * 在安装了下列属性文件后启用加亮和折叠
    * [Properties f文件ile](./files/api_files/asymptote.properties)
    
* Auto It3 

    * 要启用加亮和折叠，打开 `SciTEGlobal.properties`, 查找 `imports.exclude=`, 删除 `au3`，然后保存并重启 SciTE
    * [SciTE4AutoIt3 网站包含 Auto It3 相关的 properties 和 API 文件。](https://www.autoitscript.com/site/autoit-script-editor/)
    * [au3 API 文件](./files/api_files/au3.api)

* AutoHotkey (AHK)

    * [AutoHotkey properties](./files/api_files/ahk.properties)
    * [SciTE4AutoHotkey](https://github.com/fincs/SciTE4AutoHotkey) custom SciTE build for ahk
    * [ahk API 文件](./files/api_files/ahk.api)

* AutoCAD 对话框组件

    * [DCL properties](./files/api_files/adcl.properties)

* Avenue (Ave)

    * 要启用加亮和折叠，打开 `SciTEGlobal.properties`，查找 `imports.exclude=`，删除 `ave`，然后保存并重启 SciTE

* AviSynth (avs)

    * 要启用加亮和折叠，打开 `SciTEGlobal.properties`，查找 `imports.exclude=`，删除 `avs`，然后保存并重启 SciTE

* baan

    * 要启用加亮和折叠，打开 `SciTEGlobal.properties`，查找 `imports.exclude=`，删除 `baan`，然后保存并重启 SciTE

* Batch files (MS-DOS)

    * 默认情况下已启用加亮和折叠
    * [批处理的 API 文件](./files/api_files/batch.api.zip) (用于 NT, XP/2003, GNUWin32 UnixUtils 和 SysInternals 命令的 API 文件)

* Bash

    * 默认情况下已启用加亮和折叠

* BlitzBasic

    * 要启用加亮和折叠，打开 `SciTEGlobal.properties`，查找 `imports.exclude=`，删除 `blitzbasic`，然后保存并重启 SciTE

* Bullant

    * 要启用加亮和折叠，打开 `SciTEGlobal.properties`，查找 `imports.exclude=`，删除 `bullant`，然后保存并重启 SciTE
    
* C/C++

    * 默认情况下已启用加亮和折叠
    * [C 标准库](./files/api_files/c_withdoc.api) 带简短的 doc 字符串
    * [C 标准库](./files/api_files/c.api)
    * [C++ 标准库，包括 C++11](./files/api_files/cpp.api)
    * [cpp_more.properties](./files/api_files/cpp_more.properties) 添加用于 c99, c11, cpp98, cpp11, Objective C, idl, Doxygen, Arduino, go, Actionscript, vala, pike, swift 的加亮
    * [Windows API, cpp](./files/api_files/cpp_win32.api)
    * [OpenGL 1.2 API](./files/api_files/opengl.api)
    * [OpenGL 4.4 API](./files/api_files/glext.api)
    * [Glut API](./files/api_files/glut.api)
    * [SDL API](./files/api_files/sdl.api)

* C#

    * 默认情况下已启用加亮和折叠
    * [C# csharp api](./files/api_files/c_sharp.api)

* CIL 

    * [CIL/MSIL 的 Properties](./files/api_files/il.properties)

* Clojure

    * [一个包含了用于 Scheme 和 Clojure 支持的一个 lisp.properties](./files/api_files/lisp_and_closure.properties)
    * [Clojure 的 api 文件](./files/api_files/clojure.api)

* CMake

    * 要启用加亮和折叠，打开 `SciTEGlobal.properties`，查找 `imports.exclude=`，删除 `cmake`，然后保存并重启 SciTE
    * [CMake API](./files/api_files/cmake.api)

* COBOL

    * 要启用加亮和折叠，打开 `SciTEGlobal.properties`，查找 `imports.exclude=`，删除 `cobol`，然后保存并重启 SciTE

* Cobra

    * [用于 Cobra 和 Cobraproj 的 Properties](./files/api_files/cobra.zip)

* coffeescript

    * 要启用加亮和折叠，打开 `SciTEGlobal.properties`，查找 `imports.exclude=`，删除 `coffeescript`，然后保存并重启 SciTE

* conf (Apache)

    * 默认情况下已启用加亮和折叠

* csound

    * 要启用加亮和折叠，打开 `SciTEGlobal.properties`，查找 `imports.exclude=`，删除 `csound`，然后保存并重启 SciTE

* D

    * 默认情况下已启用加亮和折叠

* Delphi

    * 默认情况下已启用加亮和折叠
    * [Delphi api 文件和缩写](./files/api_files/delphi_extras.zip) 

* diff files

    * 默认情况下已启用加亮和折叠

* ecl

    * 要启用加亮和折叠，打开 `SciTEGlobal.properties`，查找 `imports.exclude=`，删除 `ecl`，然后保存并重启 SciTE

* Eiffel

    * 要启用加亮和折叠，打开 `SciTEGlobal.properties`，查找 `imports.exclude=`，删除 `eiffel`，然后保存并重启 SciTE

* Erlang

    * 要启用加亮和折叠，打开 `SciTEGlobal.properties`，查找 `imports.exclude=`，删除 `erlang`，然后保存并重启 SciTE

* E-Script (escript)

    * 要启用加亮和折叠，打开 `SciTEGlobal.properties`，查找 `imports.exclude=`，删除 `escript`，然后保存并重启 SciTE

* Flagship

    * 要启用加亮和折叠，打开 `SciTEGlobal.properties`，查找 `imports.exclude=`，删除 `flagship`，然后保存并重启 SciTE
    
* Forth

    * 要启用加亮和折叠，打开 `SciTEGlobal.properties`，查找 `imports.exclude=`，删除 `forth`，然后保存并重启 SciTE
    * [Forth 的 api 文件](./files/api_files/forth.api)
    
* Fortran

    * 默认情况下已启用加亮和折叠
    * [标准 FORTRAN API 函数](./files/api_files/fortran.api)

* Freebasic

    * 要启用加亮和折叠，打开 `SciTEGlobal.properties`，查找 `imports.exclude=`，删除 `freebasic`，然后保存并重启 SciTE
    * 加亮更多关键字的[属性文件](./files/api_files/freebasic.properties)
    * [api 文件](./files/api_files/freebasic.api)
    
* GAP

    * 要启用加亮和折叠，打开 `SciTEGlobal.properties`，查找 `imports.exclude=`，删除 `gap`，然后保存并重启 SciTE

* Gettext

    * 默认情况下已启用加亮和折叠
    
* GLPK/GMPL (MathProg)

    * 可以在[这里](https://sourceforge.net/projects/gusek/?source=directory)找到一个基于 SciTE 的 LP/MILP IDE

* Go

    * 默认情况下已启用加亮和折叠

* Haml

    * [properties 文件](./files/api_files/haml.properties)

* Haskell

    * 要启用加亮和折叠，打开 `SciTEGlobal.properties`，查找 `imports.exclude=`，删除 `haskell`，然后保存并重启 SciTE
    * literatehaskell 支持可以通过复制 `haskell.properties` 到 `lhaskell.properties` 来启用，更改所有对 .hs 的引用为 .lhs，并更改 `lexer.*.lhs=haskell` 行为 `lexer.*.lhs=literatehaskell`

* Intel HEX (hex)

    * 要启用加亮和折叠，打开 `SciTEGlobal.properties`，查找 `imports.exclude=`，删除 `hex`，然后保存并重启 SciTE

* InnoSetup (inno)

    * 要启用加亮和折叠，打开 `SciTEGlobal.properties`，查找 `imports.exclude=`，删除 `inno`，然后保存并重启 SciTE

* IDL/MSIDL/XPIDL

    * 默认情况下已启用加亮和折叠

* indent

    * 一个支持在缩进级别上折叠的纯文本文档的词法分析器
    * 默认情况下已启用加亮和折叠

* INI

    * 默认情况下已启用加亮和折叠

* Java <!-- used to link to https://www.burgaud.com/scite-java-api/ , but put this info in instructions instead -->
    
    * 默认情况下已启用加亮和折叠
    * [Java properties](./files/api_files/java.properties)，包括 Java 1.8 关键字
    * [Java API](./files/api_files/java.api)
    * [Java API，其它版本包括 1.5 和 1.6](./files/api_files/javaversions.api.zip)
    
* json 和 json-ld

    * 要启用加亮和折叠，打开 `SciTEGlobal.properties`，查找 `imports.exclude=`，删除 `json`，然后保存并重启 SciTE

* KiXtart (kix)

    * 要启用加亮和折叠，打开 `SciTEGlobal.properties`，查找 `imports.exclude=`，删除 `kix`，然后保存并重启 SciTE

* LaTeX / TeX

    * 要启用加亮和折叠，打开 `SciTEGlobal.properties`，查找 `imports.exclude=`，删除 `latex`，然后保存并重启 SciTE
    * 如何添加加亮、拼写检查和使用 ConTeXt 和 SciTE 的扩展的[描述](http://www.pragma-ade.com/general/manuals/scite-context-readme.pdf)和 [Windows 包](http://wiki.contextgarden.net/Windows_Installation:_ConTeXt_Suite_with_SciTe)
    
* LISP, Scheme (scm smd)

    * 默认情况下已启用加亮和折叠
    
* LOT

    * 要启用加亮和折叠，打开 `SciTEGlobal.properties`，查找 `imports.exclude=`，删除 `lot`，然后保存并重启 SciTE

* Lout

    * 要启用加亮和折叠，打开 `SciTEGlobal.properties`，查找 `imports.exclude=`，删除 `lout`，然后保存并重启 SciTE
    
* Lua  <!--  https://github.com/arjunae/myScite has a lua.properties with a few more keywords to highlight  -->

    * 默认情况下已启用加亮和折叠
    * [Lua 标准库](./files/api_files/lua.api)
    * [SciTE 扩展脚本的 API](./files/api_files/lua_scite_extension.api)
    * [Lua 5.1, 5.2, 5.3 C API 和 luajit](./files/api_files/lua_c_api.zip)
    * [Lua 5.0 C API 和标准库](./files/api_files/lua_5.0_api.zip)
    * [scite-for-lua](https://code.google.com/archive/p/scite-for-lua/), 用于 Lua 编程的广泛支持，包括调试和一个基于 lint 的加亮工具
    * [lua-inspect](https://github.com/davidm/lua-inspect), 用于 SciTE 的插件，可以进行 Lua 代码分析和添加功能，例如重命名多处出现位置和自动补全
    * [wxLua 的 Api](./files/api_files/lua_wx.api)
    * [WoW lua 的 Api](./files/api_files/lua_wow.api)

* Make / makefile

    * 默认情况下已启用加亮和折叠

* markdown

    * 要启用加亮和折叠，打开 `SciTEGlobal.properties`，查找 `imports.exclude=`，删除 `markdown`，然后保存并重启 SciTE
    * 一个用于 markdown 的替代的 [properties 文件](./files/api_files/markdown_alt.properties)

* Matlab

    * 默认情况下已启用加亮和折叠

* maxima

    * 要启用加亮和折叠，打开 `SciTEGlobal.properties`，查找 `imports.exclude=`，删除 `maxima`，然后保存并重启 SciTE

* Metapost

    * 要启用加亮和折叠，打开 `SciTEGlobal.properties`，查找 `imports.exclude=`，删除 `metapost`，然后保存并重启 SciTE

* MetaQuotes 语言 (MQL4, MQL5, MT4)

    * [MQL4, MQL5 的 properties](./files/api_files/mql.properties)
    * [scite-mql](https://github.com/ylw633/scite-mql) 项目添加了语法加亮、自动补全、参数提示和更多用于基于 MT4 的代码

* Microsoft SQL / MSSQL

    * 默认情况下已启用加亮和折叠
    * [使用这个替换 sql.properties，以获得更好的 MSSQL 支持](./files/api_files/mssql.properties)

* MMIXAL

    * 要启用加亮和折叠，打开 `SciTEGlobal.properties`，查找 `imports.exclude=`，删除 `mmixal`，然后保存并重启 SciTE

* Modula 3 (modula3)

    * 要启用加亮和折叠，打开 `SciTEGlobal.properties`，查找 `imports.exclude=`，删除 `modula3`，然后保存并重启 SciTE

* moonscript

    * [properties](./files/api_files/moonscript.properties)
    * 一个包含 SciTE, scintillua 和 moonscript 加亮的包可以在[这里](http://leafo.net/posts/getting_started_with_moonscript.html)找到

* Nimrod

    * 要启用加亮和折叠，打开 `SciTEGlobal.properties`，查找 `imports.exclude=`，删除 `nimrod`，然后保存并重启 SciTE

* nncron / nncrontab

    * 要启用加亮和折叠，打开 `SciTEGlobal.properties`，查找 `imports.exclude=`，删除 `nncrontab`，然后保存并重启 SciTE
    * [nncron api file](./files/api_files/nncron.api) 

* NSIS (nullsoft install)

    * 要启用加亮和折叠，打开 `SciTEGlobal.properties`，查找 `imports.exclude=`，删除 `nsis`，然后保存并重启 SciTE
    * [nsis api file](./files/api_files/nsis.api) 

* Objective C

    * 默认情况下已启用加亮和折叠

* OCaml 和 mli/sml

    * 默认情况下已启用加亮和折叠

* Octave

    * 默认情况下已启用加亮和折叠
    * [octave.api](./files/api_files/octave.api)

* Opal

    * 要启用加亮和折叠，打开 `SciTEGlobal.properties`，查找 `imports.exclude=`，删除 `opal`，然后保存并重启 SciTE

* Oracle 

    * 使用额外的关键字和标准包名称[扩展的 properties 文件](./files/api_files/sql_more.properties)
    * [sql plsql](./files/api_files/sql_plsql.api.zip) properties 文件

* OScript

    * 要启用加亮和折叠，打开 `SciTEGlobal.properties`，查找 `imports.exclude=`，删除 `oscript`，然后保存并重启 SciTE
    * [oscript.api.zip](./files/api_files/oscript.api.zip)

* Pascal

    * 默认情况下已启用加亮和折叠
    * Pascal [API](./files/api_files/pascal.api) 
    * Pascal [缩写](./files/api_files/pascal.abbrev) 

* Perl

    * 默认情况下已启用加亮和折叠
    * [Perl API](./files/api_files/perl.api)
    * [Parrot properties 文件](./files/api_files/parrot_properties.zip)

* PHP

    * 默认情况下已启用加亮和折叠
    * [php7.2.api](./files/api_files/php7.2.api) (包括 core, bundled, pecl 和外部函数)，由 [arjunae](https://github.com/arjunae/myScite/tree/devel/contrib/SciTE.apifiles/apiDogs) 贡献
    * [php.api, PHP 5](./files/api_files/php.api)
    * [php.api in Spanish, PHP 5](./files/api_files/php-es.api)
    * [PHP properties](./files/api_files/php.properties)

* PostScript

    * 要启用加亮和折叠，打开 `SciTEGlobal.properties`，查找 `imports.exclude=`，删除 `ps`，然后保存并重启 SciTE

* POV-Ray 

    * 要启用加亮和折叠，打开 `SciTEGlobal.properties`，查找 `imports.exclude=`，删除 `pov`，然后保存并重启 SciTE
    * [POV-Ray API](./files/api_files/pov.api)

* PowerPro

    * 要启用加亮和折叠，打开 `SciTEGlobal.properties`，查找 `imports.exclude=`，删除 `powerpro`，然后保存并重启 SciTE

* PowerShell (ps1/ps2)

    * 要启用加亮和折叠，打开 `SciTEGlobal.properties`，查找 `imports.exclude=`，删除 `powershell`，然后保存并重启 SciTE

* Progress

    * 在安装了下列属性文件后启用加亮和折叠
    * [Progress properties](./files/api_files/progress.properties)

* PureBasic

    * 要启用加亮和折叠，打开 `SciTEGlobal.properties`，查找 `imports.exclude=`，删除 `purebasic`，然后保存并重启 SciTE

* Python

    * 默认情况下已启用加亮和折叠
    * 适用于 [Python 3.8](./files/api_files/python38.api.zip), [Python 3.7](./files/api_files/python37.api.zip) 的 API 文件和关键字文件
    * [在未处理的异常上自动打印局部变量的内容](./files/api_files/python_print_vars.zip)
    * [numpy](./files/api_files/py_numpy.zip) 的 API 文件
    * [scipy](./files/api_files/py_scipy.zip) 的 API 文件
    * 较旧的 [Python API](./files/api_files/python.api)，包括 PIL, psycho

* R

    * 要启用加亮和折叠，打开 `SciTEGlobal.properties`，查找 `imports.exclude=`，删除 `r`，然后保存并重启 SciTE
    * 一个带有额额外关键字加亮的 [properties 文件](./files/api_files/r.properties)

* Rebol

    * 要启用加亮和折叠，打开 `SciTEGlobal.properties`，查找 `imports.exclude=`，删除 `rebol`，然后保存并重启 SciTE

* Registry

    * 默认情况下已启用加亮和折叠

* Ruby

    * 默认情况下已启用加亮和折叠
    * [Ruby API](./files/api_files/ruby.api)

* Rust

    * 要启用加亮和折叠，打开 `SciTEGlobal.properties`，查找 `imports.exclude=`，删除 `rust`，然后保存并重启 SciTE
    
* Scheme

    * 默认情况下已启用加亮和折叠

* scriptol

    * 要启用加亮和折叠，打开 `SciTEGlobal.properties`，查找 `imports.exclude=`，删除 `scriptol`，然后保存并重启 SciTE
    
* Smalltalk

    * 要启用加亮和折叠，打开 `SciTEGlobal.properties`，查找 `imports.exclude=`，删除 `smalltalk`，然后保存并重启 SciTE

* SORCUS Installation (sorcins)

    * 要启用加亮和折叠，打开 `SciTEGlobal.properties`，查找 `imports.exclude=`，删除 `sorcins`，然后保存并重启 SciTE

* Specman E (specman)

    * 要启用加亮和折叠，打开 `SciTEGlobal.properties`，查找 `imports.exclude=`，删除 `specman`，然后保存并重启 SciTE

* Spice

    * 要启用加亮和折叠，打开 `SciTEGlobal.properties`，查找 `imports.exclude=`，删除 `spice`，然后保存并重启 SciTE

* SQL 和 PLSQL <!--  https://github.com/arjunae/myScite 拥有一个带有更多要加亮的关键字的 sql.properties  -->

    * 默认情况下已启用加亮和折叠

* S-Record

    * 默认情况下已启用加亮和折叠

* Swift

    * 默认情况下已启用加亮和折叠

* TACL

    * 要启用加亮和折叠，打开 `SciTEGlobal.properties`，查找 `imports.exclude=`，删除 `tacl`，然后保存并重启 SciTE

* TADS3 

    * 在安装了下列属性文件后启用加亮和折叠
    * [TADS3 property 文件和展开](./files/api_files/tads3.zip)

* TAL

    * 要启用加亮和折叠，打开 `SciTEGlobal.properties`，查找 `imports.exclude=`，删除 `tal`，然后保存并重启 SciTE
    
* Tcl/Tk

    * 默认情况下已启用加亮和折叠

* txt2tags

    * 要启用加亮和折叠，打开 `SciTEGlobal.properties`，查找 `imports.exclude=`，删除 `txt2tags`，然后保存并重启 SciTE

* Vala

    * 默认情况下已启用加亮和折叠

* Verilog

    * 要启用加亮和折叠，打开 `SciTEGlobal.properties`，查找 `imports.exclude=`，删除 `verilog`，然后保存并重启 SciTE

* VHDL

    * 要启用加亮和折叠，打开 `SciTEGlobal.properties`，查找 `imports.exclude=`，删除 `vhdl`，然后保存并重启 SciTE

* Visual Basic

    * 默认情况下已启用加亮和折叠
    * 带有更多关键字的 vb [properties 文件](./files/api_files/vb.properties)

* VBScript

    * 默认情况下已启用加亮和折叠
    * [vbscript api](./files/api_files/vbscript.api)
    * vbscript [properties 文件](./files/api_files/vbscript.properties)
    * [vba api 文件](./files/api_files/vba.api)

* visualprolog

    * 要启用加亮和折叠，打开 `SciTEGlobal.properties`，查找 `imports.exclude=`，删除 `visualprolog`，然后保存并重启 SciTE

* Windows Scripting 

    * [Properties 文件](./files/api_files/windows_scripting.zip)
    * [更多文件和脚本](./files/api_files/windows_scripting_scripts.zip)，参考 readme.txt
    * [wsh.api](./files/api_files/wsh.api) 用于 vbscript 调用入 ActiveX 对象，如 Scripting.FileSystemObject

* XML

    * 默认情况下已启用加亮和折叠

* YAML

    * 默认情况下已启用加亮和折叠

Scintillua 项目为超过 120 种语言添加了高亮和折叠功能，但是它需要安装配置。 scintillua 可以从[这里](./files/api_files/scintillua.zip)下载，请查阅 doc/manual.md。 仍需要一个 .properties 文件来映射文件扩展名到词法分析器，更多信息[在这里](https://foicica.com/scintillua/README.html)。

要在这个列表中贡献文件，发送电邮给 scitewiki at gmail dot com 或提交一个 pull request。

如何安装上面下载的文件? 参考在本页顶部的链接了解说明。
