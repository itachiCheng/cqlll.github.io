---
title: Git
date: 2022-03-06 22:54:42
tags:
---


### Git History
[Todo]
### Git Basics
[Todo]
#### Git Repository
Git仓库是存取文件快照的地方，所有和版本控制相关的指令操作都需要在仓库中进行管理。

获得repository环境有两种方式：
- 本地环境`git init`初始化
- 外部环境`git clone`到本地环境
  
`git init`：创建一个.git文件夹，`git status`：显示当前的内容状态（建议多多输入查看）。

`git clone url <file_name>`：值得注意的是，这个指令pull down所有版本数据得同时，创建一个repository，其中就包含了各个版本的快照。


- 所在分支（ex. On branch master)

- commits信息（No commits yet）

- changes信息（Changes to be committed）

- untracked信息（Untracked files:...）

#### Recording Changes to the Repository

- Two states——tracked or untracked
- untracked 空文件(删除形成)或者新文件
- tracked 除了空文件（删除形成）或者新文件以外的所有文件状态
  
`git add`：untracked --> tracked，从机理上理解，`git add`将改动进行缓存，但此时的改动文件变为tracked状态,但还没有在repository上形成存储实体。

`git commit`：tracked --> working tree clean,代表没有额外需要记录的改动，这些改动在repository中已经”纯净“地保存为存储实体。


使用Git可以使我们不必关心更改的内容，但需要更加留意”更改“这件事。如果我们对文件状态变化非常熟悉，那么就能很好地操作版本管理。
[Todo planuml]
![The lifecycle of the status of your files](http://www.plantuml.com/plantuml/proxy?cache=no&src=https://raw.github.com/CQLLL/cqlll.github.io/source/source/_posts/Git/Status_Transfer.puml)
