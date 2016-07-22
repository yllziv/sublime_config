## 我的 Sublime3 配置

我使用的操作系统是 Mac OS，不同的操作系统，在 Sublime 配置上会有微小的差别。

### 安装步骤

－ 在新系统上 Sublime 安装好之后执行下面语句
```console
subliem2: cd ~/Library/Application\ Support/Sublime\ Text\ 2/Packages/User/
sublime3: cd ~/Library/Application\ Support/Sublime\ Text\ 3/Packages/User/
git clone git@github.com:yllziv/sublime_config.git
mv sublime_config/* .
rm -rf sublime_config
```

### Sublime 安装插件
我使用 [Package
Control](https://packagecontrol.io/installation)，所有我安装的包在 [Package
Control.sublime-settings 文件](https://github.com/yllziv/sublime_config/blob/master/Package%20Control.sublime-settings)
 中都列出了。

安装 package Control
复制这一段到控制台（Ctrl+~）（或者在View/Show Console）：
```python
import urllib.request,os; pf = 'Package Control.sublime-package'; ipp = sublime.installed_packages_path(); urllib.request.install_opener( urllib.request.build_opener( urllib.request.ProxyHandler()) ); open(os.path.join(ipp, pf), 'wb').write(urllib.request.urlopen( 'http://sublime.wbond.net/' + pf.replace(' ','%20')).read())
```

安装完成后重新启动Sublime，按下快捷键Ctrl + Shift + P; 输入install，选择Install Package并回车

删除插件
Ctrl + Shift + P; 输入remove install

### 简单说一下用到的几个插件

- Doc​Blockr : 自动生成注释： /** ,然后按tab
- ConvertToUTF8：解决sublime text2中不能显示中文的问题
- AutoFileName ： 插入文件，自动提示
- Bracket​Highlighter——括号高亮匹配；
- Pretty JSON——JSON美化扩展
- JavaScript Snippets js代码自动提示
- Emmet 是一个插件，它可以让你更快更高效地编写HTML和CSS
- AllAutocomplete 插件会搜索所有打开的文件来寻找匹配的提示词
- JS 格式化插件 JsFormat: 快捷键：ctrl+alt+f
- SyncedSideBar，支持当前文件自动在左侧面板中定位
- sass，高亮sass代码

### 在mac命令行中启动 Sublime
vim /etc/profile ，vim ~/.bashrc 设定 alias 内容：
```bash
alias subl=\''/Applications/Sublime Text.app/Contents/SharedSupport/bin/subl'\'
```
需要打开（如果没有的话先创建）文件：
~/.bash_profile
在里面加入一行：
source ~/.bashrc
souce /etc/profile 

### 注册 Sublime3 
```bash
—– BEGIN LICENSE —–
Ryan Clark
Single User License
EA7E-812479
2158A7DE B690A7A3 8EC04710 006A5EEB
34E77CA3 9C82C81F 0DB6371B 79704E6F
93F36655 B031503A 03257CCC 01B20F60
D304FA8D B1B4F0AF 8A76C7BA 0FA94D55
56D46BCE 5237A341 CD837F30 4D60772D
349B1179 A996F826 90CDB73C 24D41245
FD032C30 AD5E7241 4EAA66ED 167D91FB
55896B16 EA125C81 F550AF6B A6820916
—— END LICENSE ——
```

### 备注
更新 Github Sublime 配置
```bash
cp ~/Library/Application\ Support/Sublime\ Text\ 3/Packages/User/* ~/code/sublime_config
```

