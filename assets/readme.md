## BAT 中的语法高亮显示

`bat`使用[syntect](https://github.com/trishume/syntect)库，以高亮显示源代码. 作为基础,syntect 使用[Sublime Text](https://www.sublimetext.com/)中的语法定义`.sublime-syntax`格式.

为了增加新的语法`bat`，请遵循以下步骤:

1.  查找给定语言的 Sublime Text 语法,最好是在单独的 Git 存储库中,该存储库可以作为子模块包含 (在`assets/syntaxes`)

2.  如果 Sublime Text 语法只能作为`.tmLanguage`文件,以 Sublime Text 打开文件，并将其转换为`.sublime-syntax`文件通过*Tools*>_Developer_>_New Syntax from XXX.tmLanguage..._. 将新文件保存在`assets/syntaxes`文件夹.

3.  运行`create.sh`脚本. 它会运行`bat cache --init`解析所有可用的`.sublime-syntax`文件，并将它们序列化为`syntaxes.bin`文件 (在本文件夹中) .

4.  重新编译`bat`. 在编译时,`syntaxes.bin`文件将存储在`bat`二进制中.

### 故障排除

确保本地缓存，不干扰内部存储的语法和主题 (`bat cache --clear`)

### 手工修改

下列文件在从`.tmLanguage`文件转换后，手动修改:

- `VimL.sublime-syntax`=>增加`.vimrc`文件类型.
- `Dart.sublime-syntax`=>删除包含的`#regex.dart`,
