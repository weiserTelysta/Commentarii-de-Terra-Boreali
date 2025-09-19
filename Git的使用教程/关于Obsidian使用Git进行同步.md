>本文部分参考了https://pwa.sspai.com/post/97316博客的内容
# Git安装
###### 下载安装
前往Git官网，安装这一版本控制工具。
```
https://git-scm.com/downloads
```
###### 初始化
输入下面两行内容，将后面部分进行替换。
```
git config --global user.name  "你的名字"
git config --global user.email  "你的邮箱@example.com"
```
###### 插件安装
在黑曜石的第三方市场下载Git插件，直接搜索即可获得。
**配置插件**
在`Custom Git Binary Path`这里填上git.exe的路径。git.exe位于解压后文件夹的`bin`目录下。
如果是安装版本，那就是安装路径内的Bin目录。
```
"C:\Program Files\Git\bin\git.exe"
```
# 初始化
使用`Ctrl+P`调用obsidian命令行。
初始化仓库，文件夹里面会出现`.git`的隐藏文件，这是git的基本文件。
```
git init
```
同步远程仓库，输入
```
git clone
```
然后输入远程仓库的URL
```
git@github.com:weiserTelysta/Commentarii-de-Terra-Boreali.git
```
然后输入你要放置文件夹的名字即可。
**插件设置**
点击齿轮按钮，进入git插件。
**message设置**
首先在`Automatic`内最后一行`Commit message on auto commit-and-sync`内输入。
```
{{date}},{{hostname}},{{numFiles}},{{files}}
```
然后进入`Commit message`，在第一行同样输入一样的内容。
**hostname设置**
为了方便查看是谁提交的内容。
需要在`Commit message`内写入你的ID。
**同步内容限制**
此时你如果希望只同步笔记内容，不同步设置、插件以及主题等内容的话你就需要要求Git不同步仓库根目录上的`.obsidian`文件夹。搜索命令`Git: Edit .gitignore`，在里面加上一行`.obsidian`即可。
# 提交
我个人推荐手动提交，因为你可以手动输入自己的提交信息。
**手动提交**
通过`Ctrl+P`打开命令行，输入
```
git commit with spefic message
```
一般你输入`git commit with`的时候就已经只有一个选项了。然后输入你想要写的内容后。
再次通过`Ctrl+P`打开命令行，输入
```
git push
```
或是通过`Git`提供的Push按钮。
**自动提交**
点击`bar`内的`Git`按钮，然后点击`commit`然后再点击`push`按钮即可。
用自动提交必须填写必要的信息，不然找不到是谁提交的。
**开启自动提交询问message按钮**
进入`git`，找到`Automatic`倒数第二行，`Specify custom commit message on auto commit-and-sync`，关闭即可。
此后再每次点击`commit and sync`时，会跳出信息，在后部输入必要信息即可。
> 注意 目前GitHub需要注册账号并使用ssh认证。