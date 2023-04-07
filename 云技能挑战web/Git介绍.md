# Git介绍

# 简介

假设你是刚加入一家为商业客机编写航空电子软件的公司的软件开发人员。 质量控制非常重要，开发人员以小型团队方式协作，使用 Git 进行版本控制。 你听说过版本控制，但从未使用过 Git，因此你迫不及待地想要体验！

你决定构建一个网站，你和朋友可利用它来共享猫的图片，这样一来，在将 Git 的相关知识运用到工作之前，可以先在有趣的学习环境中了解它。 你开始构建该网站，使用 Git 跟踪更改并对所有源代码文件进行备份以防服务器发生故障。 但在深入了解 Git 之前，必须先了解基础知识。

此模块中提供有关版本控制和 Git 的简介。 起初 Git 可能稍显晦涩，甚至有时还会带来挫败感。 但如果你逐步学习，就会发现为何它能如此快速地成为世界上最常用的版本控制系统 - 不仅适用于软件开发人员，也适用于编写文档和协作处理其他工作的团队。

### 观看视频

有关本模块中的练习的概述，请参阅视频 [Git 介绍回顾](https://www.youtube.com/watch?v=9uGS1ak_FGg%3Fazure-portal%3Dtrue)。

## 学习目标

在本模块中，你将：

* 了解什么是版本控制
* 了解分布式版本控制系统，如 Git
* 确定 Git 和 GitHub 之间的区别，以及它们在软件开发生命周期中扮演的角色

## 先决条件

无。

# 什么是版本控制？

版本控制系统 (VCS) 是跟踪文件集合更改的程序或程序集。 VCS 的一个目标是轻松撤回至单个文件或整个项目的较早版本。 另一个目标是支持多个团队成员同时处理同一个项目（甚至是相同的文件），而不会影响各自的工作。

VCS 的另一个名称是软件配置管理 (SCM) 系统。 这两个术语通常可以互换使用，实际上，Git 的官方文档位于 [git-scm.com](https://git-scm.com/)。 从技术上讲，版本控制只是 SCM 中涉及的一种做法。 VCS 可用于除软件之外的项目（包括书籍和在线教程）。

你可以使用 VCS 执行以下操作：

* 查看对项目所做的所有更改、更改时间和更改者。
* 为每条更改添加一条消息，解释更改原因。
* 检索整个项目或单个文件的以前版本。
* 创建“分支”，可在其中进行试验性的更改。 通过此功能，可同时（由不同的人）处理多个不同的更改集（例如，功能或 bug 修复），而不会影响主分支。 稍后，可以将所需更改合并到主分支。
* 将标记附加到版本 - 例如，用于标记新版本。

Git 是一种快速、通用、高度可缩放的免费开源 VCS。 它的主要作者是 Linux 的创建者 Linus Torvalds。

## 分布式版本控制

较早的 VCS 实例（包括 CVS，Subversion (SVN) 和 Perforce）使用集中式服务器来存储项目的历史记录。 这种集中意味着一台服务器也可能是单一故障点。

Git 是分布式的，这意味着项目的完整历史记录同时存储在客户端和服务器上。 可以在没有网络连接的情况下编辑文件、在本地签入文件，并在连接可用时与服务器同步。 如果服务器出现故障，你仍拥有该项目的本地副本。 从技术上讲，你甚至不必拥有服务器。 更改可以通过电子邮件传递或使用可移动媒体共享，但实际上没有人这样使用 Git。

## Git 术语

要了解 Git，必须了解相关术语。 以下是 Git 用户常用的术语的简短列表。 目前不必关注各术语的详细解释；在完成本模块中的练习的过程中，你会逐渐熟悉所有的术语。

* 工作树：包含正在处理的项目的嵌套目录和文件集。
* 存储库 (repo)：位于工作树的顶级的目录，Git 在其中保留了项目所有的历史记录和元数据。 存储库 (Repository) 一般称为 repo。 “空存储库”不属于工作树；它用于共享或备份。 空存储库通常是名称以 .git 结尾的目录，例如 project.git。
* 哈希：哈希函数生成的数字，它将文件或其他对象的内容表示为固定长度的数字。 Git 使用 160 位长度的哈希。 使用哈希的一个好处是，Git 可以通过对文件内容进行哈希处理并将结果与先前的哈希进行比较，从而判断文件是否已更改。 如果文件的时间日期戳已更改，但文件哈希未更改，则 Git 知道文件内容未更改。
* 对象：一个 Git 存储库包含四种类型的“对象”，每种对象均由 SHA-1 哈希进行唯一标识。 blob 对象包含普通文件。 “树”对象表示目录；它包含名称、哈希和权限。 “提交”对象表示工作树的特定版本。 “标记”是附加到提交的名称。
* 提交：用作动词时，“提交”的意思是生成提交对象。 此操作的名称来自对数据库的提交。 它的意思是你正在提交所做的更改，让其他人最终也可以看到它们。
* 分支：分支是一系列已命名的关联提交。 分支上的最新提交称为“头”。 初始化存储库时创建的默认分支称为 `main`，在 Git 中通常名为 `master`。 当前分支的头称为“`HEAD`”。 分支是 Git 的一项非常有用的功能，因为通过它，开发人员可在分支中独立（或协同）工作，然后将其更改合并到默认分支中。
* 远程库：远程库是对另一个 Git 存储库的已命名引用。 创建存储库时，Git 会创建一个名为“`origin`”的远程库，这是用于推送和拉取操作的默认远程库。
* 命令、子命令和选项：Git 操作通过 `git push` 和 `git pull` 等命令执行。 `git` 是命令，`push` 或 `pull` 是子命令。 子命令指定需要 Git 执行的操作。 命令通常带有选项，这些选项使用连字符 (-) 或双连字符 (--)。 例如 `git reset --hard`。

你很快就会熟悉以上术语（例如“`push`”和“`pull`”）。 但是你需要从某个部分开始学习，完成本模块后，再回顾此术语表可能对你有所帮助。

## Git 命令行

有一系列可用于 Git 的不同 GUI，包括 GitHub Desktop。 许多程序编辑器（如 Microsoft [Visual Studio Code](https://code.visualstudio.com/)）也具有与 Git 的接口。 它们的工作方式各异，局限性也各不相同。 它们都不能实现 Git 的所有功能。

本模块中的练习使用 Git 命令行 - 具体来说，是在 Azure Cloud Shell 中执行的 Git 命令。 但是，无论使用哪种操作系统，Git 的命令行接口的工作方式都相同。 另外，借助该命令行，可以利用 Git 的全部功能。 仅通过 GUI 查看 Git 的开发人员有时会遇到无法解决的错误消息，因此他们必须使用命令行才能解决问题。

## Git 和 GitHub

使用 Git 时，你可能想知道它提供的功能与 [GitHub](https://github.com/) 上提供的功能之间的区别。

如前文所述，Git 是一种分布式版本控制系统 (DVCS)，多名开发人员和其他参与者可通过它共同处理同一项目。 它提供了一种方法来处理一个或多个本地分支，然后将它们推送到远程存储库。

GitHub 是将 Git 用作其核心技术的云平台。 GitHub 简化了协作处理项目的过程，提供了网站、更多命令行工具，以及可使开发人员和用户一起工作的总体流程。 GitHub 充当先前提到的“远程存储库”。

GitHub 提供的主要功能包括：

* 问题
* 讨论
* 拉取请求
* 通知
* 标签
* 操作
* 前叉
* 项目

若要详细了解 GitHub，请参阅 [GitHub 简介](https://learn.microsoft.com/zh-cn/training/modules/introduction-to-github)、Microsoft Learn 模块或 [GitHub 入门](https://docs.github.com/free-pro-team@latest/github/getting-started-with-github)帮助文档。

下一步是你亲自试用 Git！

# 练习 - 试用 Git

必须使用沙盒，才能完成此模块。

通过使用[沙盒](https://learn.microsoft.com/en-us/training/support/faq?pivots=sandbox)，可访问免费资源。 个人订阅将不会收费。 沙盒仅限用于在 Microsoft Learn 上完成培训。 禁止将沙盒用于任何其他目的，否则可能会导致永远无法使用沙盒。

Microsoft 出于教育目的提供此实验室体验和相关内容。 提供的所有信息均归 Microsoft 所有，仅用于学习本 Microsoft Learn 模块中涵盖的产品和服务。

激活沙盒

在创建第一个存储库之前，必须确保已安装并配置 Git。 Git 已随 Azure Cloud Shell 预安装，因此我们可以在右侧的 Cloud Shell 中使用 Git。

## 配置 Git

1. 在 Cloud Shell 中，要再次确认已安装 Git，请键入 `git --version`：

   ```
   git --version
   ```

   提示

   可以使用“复制”按钮将命令复制到剪贴板。 要粘贴，请右键单击 Cloud Shell 终端中的新行，然后选择“粘贴”，或使用 Shift+Insert 键盘快捷方式（在 macOS 上为 ⌘+V）。
2. 应当会看到与以下示例类似的输出：

   ```
   git version 2.7.4
   ```

3. 要配置 Git，必须定义一些全局变量：`user.name` 和 `user.email`。 这两者都是进行提交所必需的。
4. 在 Cloud Shell 中，用以下命令设置你的名称。 将 `<USER_NAME>` 替换为要使用的用户名。

   ```
   git config --global user.name "<USER_NAME>"
   ```

5. 现在，使用此命令创建 `user.email` 配置变量，并将 `<USER_EMAIL>` 替换为你的电子邮件地址：

   ```
   git config --global user.email "<USER_EMAIL>"
   ```

6. 运行以下命令以检查更改是否成功：

   ```
   git config --list
   ```

7. 确认输出包含类似以下示例的两行。 你的用户名和电子邮件地址将与示例中显示的内容不同。

   ```
   user.name=User Name
   user.email=user-name@contoso.com
   ```

## 设置 Git 存储库

Git 的工作方式是：检查特定文件夹内文件的更改。 我们会创建一个文件夹作为“工作树”（项目目录），并将其告知 Git，以便可以开始跟踪更改。 我们将 Git 存储库初始化到该文件夹中来告知 Git 开始跟踪更改。

首先为项目创建一个空文件夹，然后在该文件夹内初始化 Git 存储库。

1. 创建名为“Cats”的文件夹。 此文件夹将为项目目录（也称为“工作树”）。 项目目录是存储所有与项目有关的文件的位置。 在此练习中，它是存储你的网站和创建该网站的文件及其内容的位置。

   ```
   mkdir Cats
   ```

2. 使用 `cd` 命令切换到项目目录：

   ```
   cd Cats
   ```

3. 现在，初始化新存储库，并将默认分支的名称设置为 `main`：
   如果你运行的是 Git 版本 2.28.0 或更高版本，请使用以下命令：

   ```
   git init --initial-branch=main
   git init -b main

   ```

   对于 Git 的较早版本，请使用以下命令：

   ```
   git init
   git checkout -b main

   ```

   运行初始化命令后，应当会看到与以下示例类似的输出：

   ```
   Initialized empty Git repository in /home/<user>/Cats/.git/

   Switched to a new branch 'main'
   ```

4. 现在使用 `git status` 命令以显示工作树的状态：

   ```
   git status
   ```

   Git 用此输出进行响应，这表示 `master` 为当前分支。 （它也是唯一分支。）到目前为止，一切顺利。

   ```
    On branch master

    No commits yet

    nothing to commit (create/copy files and use "git add" to track)  
   ```

5. 使用 `ls` 命令以显示工作树的内容：

   ```
   ls -a
   ```

   确认目录包含一个名为“.git”的子目录。 （将 `-a` 选项与 `ls` 结合使用非常重要，因为 Linux 通常会隐藏以句点开头的文件和目录名称。）此文件夹为 Git 存储库 - Git 用于存储工作树的元数据和历史记录的目录。

   你通常无需直接对“.git”目录执行任何操作。 在工作树的状态发生更改时，Git 会更新元数据，以跟踪文件中的更改。 此目录无需你执行任何操作，但它对于 Git 非常重要。

## 从 Git 获取帮助

与大多数命令行工具一样，Git 具有内置的帮助功能，可用于查找命令和关键字。

1. 键入以下命令，获取 Git 相关的操作帮助：

   ```
   git --help
   ```

2. 此命令显示以下输出：

   ```
   usage: git [--version] [--help] [-C <path>] [-c name=value]
          [--exec-path[=<path>]] [--html-path] [--man-path] [--info-path]
          [-p | --paginate | --no-pager] [--no-replace-objects] [--bare]
          [--git-dir=<path>] [--work-tree=<path>] [--namespace=<name>]
          <command> [<args>]

   These are common Git commands used in various situations:

   start a working area (see also: git help tutorial)
      clone      Clone a repository into a new directory
      init       Create an empty Git repository or reinitialize an existing one

   work on the current change (see also: git help everyday)
      add        Add file contents to the index
      mv         Move or rename a file, a directory, or a symlink
      reset      Reset current HEAD to the specified state
      rm         Remove files from the working tree and from the index

   examine the history and state (see also: git help revisions)
      bisect     Use binary search to find the commit that introduced a bug
      grep       Print lines matching a pattern
      log        Show commit logs
      show       Show various types of objects
      status     Show the working tree status

   grow, mark and tweak your common history
      branch     List, create, or delete branches
      checkout   Switch branches or restore working tree files
      commit     Record changes to the repository
      diff       Show changes between commits, commit and working tree, etc
      merge      Join two or more development histories together
      rebase     Forward-port local commits to the updated upstream head
      tag        Create, list, delete or verify a tag object signed with GPG

   collaborate (see also: git help workflows)
      fetch      Download objects and refs from another repository
      pull       Fetch from and integrate with another repository or a local branch
      push       Update remote refs along with associated objects

   'git help -a' and 'git help -g' list available subcommands and some
   concept guides. See 'git help <command>' or 'git help <concept>'
   to read about a specific subcommand or concept.
   ```

请通读适用于 Git 的各种选项，并注意，每个命令都有各自的帮助页面，可供你深入了解时使用。 并不是所有这些命令你都能看懂，但是如果你有使用 VCS 的经验，可能会对一些命令感到熟悉。

在下一课中，你将详细了解你刚试用过的命令以及 Git 的基本知识。

# 基本 Git 命令

Git 的工作方式是记住对文件所做的更改，就像它对文件系统拍摄快照一样。

我们将介绍一些基本命令，用于开始跟踪存储库中的文件。 然后，你将保存 Git 的第一个“快照”以进行比较。

### git status

首先是最常用的 Git 命令 `git status`。 你在前面的练习中已使用过一次，目的是查看是否已正确初始化 Git 存储库。

`git status` 显示工作树的状态（以及暂存区域的状态 - 后文会对此详细介绍）。 利用它可查看 Git 当前正在跟踪哪些更改，以便决定是否指示 Git 再拍摄一个快照。

### git add

`git add` 命令用于指示 Git 开始跟踪某些文件中的更改。

此操作的技术术语是“暂存”这些更改。 你将使用 `git add` 来暂存更改以准备提交。 已添加但尚未提交的文件中的所有更改都存储在“暂存区域”中。

### git commit

暂存要提交的某些更改后，可以通过调用 `git commit` 命令将工作保存到快照。

“提交”是动词也是名词。 在“提交到计划”或“将更改提交到数据库”中，“提交”的含义本质上是相同的。 作为动词，提交更改意味着将文件、目录或其他内容的副本作为新版本放置到存储库中。 作为名词，提交是一小部分数据，它为所提交的更改提供了唯一标识。 保存在提交中的数据包括作者姓名和电子邮件地址、日期、有关所执行操作（以及原因）的注释、可选数字签名和先前提交的唯一标识符。

### git log

使用 `git log` 命令，可查看先前提交的相关信息。 每个提交都附加有一条消息（提交消息），`git log` 命令输出有关最新提交的信息，如其时间戳、作者和提交消息。 此命令有助于跟踪你执行的操作和已保存的更改。

### git help

尽管你已使用过 `git help` 命令，但还是应该提醒你。 利用此命令，可以轻松获取到目前为止已了解的所有命令的相关信息和其他命令信息。

请注意，每个命令均附带自己的帮助页。 可以通过键入 `git <command> --help` 找到这些帮助页。 例如，`git commit --help` 会调出一个页面，其中包含有关 `git commit` 命令及其使用方法的详细信息。

# 知识检查

**1.** 以下哪种应用场景是版本控制系统的常见用例？

[ ] 删除项目或文件的较早版本，让你知道你只使用最新的文件或数据。

[ ] 在独立分支中对项目进行试验性的更改。

正确！ 使用分支创建项目的不同更改集是版本控制的一个关键用例。

[ ] 收集大型项目的功能要求，并将其传达给利益干系人。

**2.** 版本控制系统的另一个名称是什么？

[ ] 版本管理软件 (VMS)

[ ] 软件控制管理 (SCM) 系统

[ ] 软件配置管理 (SCM) 系统

正确！

**3.** Git 和 GitHub 之间有什么区别？

[ ] Git 让你可以处理一个或多个本地分支并将更改推送到远程存储库。 GitHub 充当远程存储库，可通过网站或命令行工具访问。

正确！ Git 是一种工具，可用于处理本地分支并将更改推送到远程存储库。 GitHub 充当远程存储库。

[ ] Git 是一种在云中运行的分布式版本控制系统 (DVCS)。 GitHub 是提供对 Git 技术的访问的一个接口层。

[ ] Git 供单个参与者使用。 GitHub 供多个参与者使用，可简化团队开发工作。

**4.** 哪个 Git 命令提供了有关 Git 用法的信息？

[ ] `git init`

[ ] `git status`

[ ] `git help`

正确！ `git help` 用于查看有关 Git 用法的信息。

# 总结

恭喜！ 在本模块中，你已了解使用 Git 的基础知识。

你已了解：

* 版本控制系统 (VCS) 的概述
* 重要的 Git 术语。
* Git 与 GitHub 之间的区别。
* 如何配置 Git。
* 一些基本 Git 命令。

你目前所掌握的 Git 相关知识已足够你针对基本项目自行使用版本控制。 版本控制的强大功能只有在与其他开发人员协作时才能明显显现。 有关与他人协作使用 Git 的详情，请查看本学习路径中的其他模块！

### 资源

如果要深入了解，请参阅以下资源：

* 运行 `git help tutorial` 和 `git help tutorial-2` 命令。
* 访问[每日 Git](https://git-scm.com/docs/everyday) 网站或使用 `git help everyday` 命令。
* 参阅 [Git 和 GitHub 学习资源](https://help.github.com/en/articles/git-and-github-learning-resources)。
* 观看 [Git 介绍回顾](https://www.youtube.com/watch?v=9uGS1ak_FGg%3Fazure-portal%3Dtrue)视频。
* 查看 [Git 官方网站](https://git-scm.com/)的[文档部分](https://git-scm.com/doc)。

---
