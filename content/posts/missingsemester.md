+++
title = 'Missing semester学习'
date = 2024-12-24T16:47:26+08:00
categories = ["技术"] 
tags = ["网络课程","linux","shell"]
+++

### 感受
编程这件事，还是绝知此事要躬行。在实践中学习很重要，要将其中的技巧灵活地运用到平时的工作当中去。

### 资源出处
https://missing-semester-cn.github.io/2020/course-shell/
</br>MIT 2020
挖掘现有工具的潜力，并介绍一些新的工具。
</br>这是大多数计算机科学相关课程中缺少的重要一环。

### 1.The Shell
简单介绍了一下bash
</br>介绍了一些简单的指令

### 2.Shell工具和脚本
上节课介绍了简单的指令，这节课开始学着写Shell脚本
</br>shell还提供了一些工具，如man命令（查看手册），find命令（查找）

### 3.Vim
我的选择是在vscode中插入vim，进行插件管理
</br>
按下 <ESC>（退出键）从任何其他模式返回正常模式。</br>在正常模式，键入 i 进入插入模式，R进入替换模式，v 进入可视（一般）模式，V 进入可视（行）模式</br> (Ctrl-V, 有时也写作 ^V）进入可视（块）模式</br>: 进入命令模式

i 进入插入模式
</br>但是对于操纵/编辑文本，不单想用退格键完成
</br>O / o 在之上/之下插入行
</br>d{移动命令} 删除 {移动命令}
</br>例如，dw 删除词, d$ 删除到行尾, d0 删除到行头。
</br>c{移动命令} 改变 {移动命令}
</br>例如，cw 改变词
</br>比如 d{移动命令} 再 i
</br>x 删除字符（等同于 dl）
</br>s 替换字符（等同于 xi）
</br>可视化模式 + 操作
</br>选中文字, d 删除 或者 c 改变
</br>u 撤销, <C-r> 重做
</br>y 复制 / “yank” （其他一些命令比如 d 也会复制）
</br>p 粘贴

</br>感觉非常复杂（>_<）,慢慢积累吧</br>有一个vim自带的游戏可以先玩一下,Vimtutor
</br>先学到了基本的用法就可以了

### 4.数据整理
#### 正则表达式

### 5.命令行环境
#### 终端多路复用
执行多个应用时，可以选择开多个终端，也可以采用终端多路复用，且后者的效果会更好

#### 配置文件
以“点文件”形式的配置文件来完成,我自己写了一个dotfile文件，专门存放对bash文件的自己配置和安装脚本，以后就算是在不同的服务器上也可以方便地从github上面拉取下来进行安装。

#### ssh
简单介绍了ssh，密钥公钥之类的

### 6.git版本控制
笑死，丑陋的顶层设计，优雅的底层设计，和我的感觉一模一样
#### git的数据模型
基本概念，快照</br>快照可能会有多个父辈，因为可能是两个分支合并而来</br>在 Git 中，我们当前的位置有一个特殊的索引，它就是 “HEAD”</br> “暂存区（staging area）”的机制，它允许您指定下次快照中要包括那些改动。
#### 如何编写好的提交信息
简短的标题，详细说明部分
#### 其他
github中的PR操作
#### 课后作业
2.克隆本课程网站的仓库</br>git log --oneline --graph --all(将版本历史可视化)</br>git log -p README.md
(查找最后修改 README.md 文件的人)

7.Fork 本课程网站的仓库，找找有没有错别字或其他可以改进的地方，在 GitHub 上发起拉取请求（Pull Request）
</br>Fork 仓库,打开课程网站仓库的 GitHub 页面,点击右上角的 Fork 按钮，将仓库复制到你的 GitHub 账户下
</br>克隆 Fork 后的仓库到本地,在你的本地机器上运行命令
</br>创建新分支,为你的改动创建一个新的分支， git checkout -b newname
</br>查找错别字或需要改进的地方,在本地编辑器中打开仓库，仔细阅读代码、文档、README 文件等，寻找问题
</br>提交更改,将修改后的文件添加到暂存区,git add <修改的文件> 提交更改：git commit -m "Fix typos in documentation and improve clarity"
</br>推送分支到 GitHub,将你的更改推送到远程仓库的 fix-typos 分支,git push origin fix-typos
</br>发起 Pull Request，打开你 Fork 的仓库页面。点击 Compare & pull request 按钮。在 Pull Request 页面填写：
标题：简要概述你的更改（如 "Fix typos in README and documentation"）。
描述：详细说明你的更改内容，例如修复的具体问题或改进的地方。
点击 Create pull request 提交你的请求。

我自己给自己提交了一个PR

### 7.调试与性能分析
#### 打印调试法与日志
“最有效的 debug 工具就是细致的分析，配合恰当位置的打印语句” — Brian Kernighan, Unix 新手入门。
</br>另外一个方法是使用日志
#### 调试debug
如使用pdb等等
