
## BAT中的语法高亮显示

`bat`使用[syntect](https://github.com/trishume/syntect)库以突出显示源代码. 作为基础,SytECT使用[Sublime Text](https://www.sublimetext.com/)中的语法定义`.sublime-syntax`格式. 

为了增加新的语法`bat`遵循以下步骤: 

1.  查找给定语言的升华文本语法,最好是在单独的Git存储库中,该存储库可以作为子模块包含 (在`assets/syntaxes`) 

2.  如果崇高文本语法只能作为`.tmLanguage`文件,以崇高的文本打开文件并将其转换为`.sublime-syntax`文件通过*工具*>*开发商*>*XX.TMLUT的新语法ⅆ*. 将新文件保存在`assets/syntaxes`文件夹. 

3.  运行`create.sh`脚本. 它叫`bat cache --init`解析所有可用`.sublime-syntax`文件并将它们序列化为`syntaxes.bin`文件 (在这个文件夹中) . 

4.  重新编译`bat`. 在编译时,`syntaxes.bin`文件将存储在`bat`二元的. 

### 故障排除

确保本地缓存不干扰内部存储的语法和主题 (`bat cache --clear`) 

### 手工修改

下列文件在从A转换后手动修改`.tmLanguage`文件: 

-   `VimL.sublime-syntax`=增加`.vimrc`文件类型. 
-   `Dart.sublime-syntax`=删除`#regex.dart`包括,
