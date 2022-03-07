---
title: Git
date: 2022-03-06 22:54:42
tags:
---


### Git History

### Git Basics

#### Git Repository
Git仓库是存取文件快照的地方，所有和版本控制相关的指令操作都需要在仓库中进行管理。

获得git repository环境有两种方式：
- 本地环境git init
- 外部环境git clone到本地环境

	git init

创建一个.git文件夹，`git status`显示当前的内容状态。

- 所在分支（ex. On branch master)

- commits信息（No commits yet）

- changes信息（Changes to be committed）

- untracked信息（Untracked files:...）

	git add
untracked --> tracked，从机理上理解，`git add`将改动进行缓存，但此时的改动文件变为tracked状态,但还没有在repository上形成存储实体。

	git commit
tracked --> working tree clean,代表没有额外需要记录的改动，repository中只有各个版本的快照。

	git clone <file_name>
值得注意的是，这个指令pull down所有数据并创建一个repository进行囊括。


#### Recording Changes to the Repository

- Two states——tracked or untracked
- untracked 空文件(删除形成)或者新文件
- tracked 除了空文件（删除形成）或者新文件以外的所有文件状态


