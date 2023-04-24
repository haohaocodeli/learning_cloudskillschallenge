[GitHub 简介](https://learn.microsoft.com/zh-cn/training/modules/introduction-to-github/)

# 简介

**已完成**100 XP

* 2 分钟

GitHub 是一个开发平台，使你能够与 5000 万开发人员一起托管和评审代码、管理项目以及构建软件。

为什么每个人都喜欢在 GitHub 上进行构建？ 因为它提供了各种规模的公司和组织在处理公共和私有项目时都需要的重要 DevOps 功能。 无论是规划功能、修复 Bug 还是协作处理更改，GitHub 都是全球软件开发人员齐聚一堂进行创造的最佳选择。 并能让他们发挥更好。

本模块将介绍如何使用主要 GitHub 功能，包括问题、通知、分支、提交和拉取请求。

## 学习目标

在本模块中，你将学习以下内容：

* 与项目社区就问题进行沟通
* 管理项目事件的通知
* 创建分支以并行管理工作
* 提交更新项目源
* 使用拉取请求引入更改
* 将网页部署到 GitHub Pages
* 确定 Git 和 GitHub 之间的区别，以及它们在软件开发生命周期中扮演的角色
* 介绍存储库分支及其与克隆的区别
* 解释存储库标签的功能，以及在问题和拉取请求中应用它们的位置

## 先决条件

* GitHub 帐户

# 什么是 GitHub？

本文将讨论你在管理和参与软件项目时每天都要使用的主要 GitHub 功能。

## GitHub 流

除了提供一个协作软件开发平台外，GitHub 还提供了一个工作流，旨在优化其各种功能的使用。 虽然本单元提供了重要平台组件的粗略概览，但建议你先查看[了解 GitHub 流](https://guides.github.com/introduction/flow/)。

## Git 和 GitHub

在使用 Git 和 GitHub 时，你可能会想知道这两者之间的区别。

Git 是一种分布式版本控制系统 (DVCS)，多名开发人员或其他参与者可通过它共同处理同一项目。 它提供了一种方法来使用一个或多个本地分支并将它们推送到远程存储库。 Git 负责在本地计算机上发生的与 GitHub 相关的所有操作。 Git 提供的主要功能包括：

* 已在本地计算机上安装和使用
* 处理版本控制
* 支持分支

若要了解有关 Git 的详细信息，请参阅[使用常用 Git 命令](https://docs.github.com/en/free-pro-team@latest/github/using-git/using-common-git-commands)。

GitHub 是一种将 Git 用作其核心技术的云平台。 它简化了协作处理项目的过程，提供了网络、命令行工具，以及可使开发人员和用户一起工作的总体流程。 GitHub 充当前面在 Git 部分中提到的“远程存储库”。

GitHub 提供的主要功能包括：

* 问题
* 讨论
* 拉取请求
* 通知
* 标签
* 操作
* 前叉
* 项目

若要了解有关 GitHub 的详细信息，请参阅 [GitHub 入门](https://docs.github.com/en/free-pro-team@latest/github/getting-started-with-github)。

## 问题

“问题”是项目使用者和开发团队之间进行大部分沟通的地方。 可以创建“问题”以讨论广泛的主题，包括 Bug 报告、功能请求、文档说明等。 创建问题后，可以将问题分配给所有者、标签、项目和里程碑。 你还可以将问题与拉取请求和其他 GitHub 项关联，以提供未来的可追溯性。

![就 bug 或功能建议向开发人员提供反馈的 GitHub 问题。](https://learn.microsoft.com/zh-cn/training/github/introduction-to-github/media/2-issue.png)

要了解 GitHub 问题，请参阅[掌握问题](https://guides.github.com/features/issues/)。

## 通知

作为一个协作平台，GitHub 为在给定工作流中发生的几乎每个事件都提供了通知。 可以根据自己的喜好来调整这些通知。 例如，可以订阅对项目的所有问题的创建和编辑，也可以只接收有关你提及的问题的通知。 你还可以决定是通过电子邮件还是 Web 和手机，或者通过这两者接收通知。 要跟踪不同项目的所有通知，请使用 [GitHub 通知仪表板](https://github.com/notifications)。

![GitHub 通知仪表板。GitHub 提供了一个收件箱，开发人员可用它来实时跟进存储库中的更改。](https://learn.microsoft.com/zh-cn/training/github/introduction-to-github/media/2-notifications.png)

要详细了解 GitHub 通知，请参阅[配置通知](https://help.github.com/github/managing-subscriptions-and-notifications-on-github/configuring-notifications)。

## 分支

分支是在 [GitHub 流](https://guides.github.com/introduction/flow/)中创建更改的首选方式。 它们提供隔离，以便多个人员可以同时以受控方式处理同一代码。 此模型可实现关键分支（如 `main`）之间的稳定性，同时允许开发人员完全自由地提交实现其目标所需的任何更改。 分支中的代码已准备好成为 `main` 分支的一部分后，可通过拉取请求合并代码。

![具有功能分支的 GitHub 流。对分支所做的更改可合并回到主分支中。](https://learn.microsoft.com/zh-cn/training/github/introduction-to-github/media/2-branching.png)

要详细了解 GitHub 分支，请参阅[关于分支](https://help.github.com/github/collaborating-with-issues-and-pull-requests/about-branches)。

## 提交

“提交”是分支上对一个或多个文件的更改。 每次创建提交时，都会分配唯一的 ID 并跟踪，以及时间和参与者。 这为查看文件或链接项（如问题或拉取请求）的历史记录的任何人提供了清晰的审核跟踪。

![GitHub 提交到主分支的内容列表。](https://learn.microsoft.com/zh-cn/training/github/introduction-to-github/media/2-commits.png)

要详细了解 GitHub 提交，请参阅[提交和查看项目的更改](https://help.github.com/desktop/contributing-to-projects/committing-and-reviewing-changes-to-your-project)。

## 拉取请求

“拉取请求”是用于表示一个分支的提交已准备好合并到另一个分支的机制。 提交拉取请求的开发人员通常会请求一名或多名审阅者验证代码并批准合并。 这些审阅者可以对更改发表评论、添加自己的更改或使用拉取请求本身进行进一步讨论。 更改获批后（如果需要审批），拉取请求的源分支（比较分支）可能会合并到基分支中。

![GitHub 拉取请求提供了一种方式来从一个分支提交到另一分支。](https://learn.microsoft.com/zh-cn/training/github/introduction-to-github/media/2-pull-request.png)

要详细了解 GitHub 拉取请求，请参阅[关于拉取请求](https://help.github.com/github/collaborating-with-issues-and-pull-requests/about-pull-requests)。

## 标签

标签提供了一种方法在存储库中对问题和拉取请求进行分类和整理。 创建 GitHub 存储库时，会自动为你添加多个标签，也可创建新标签。

标签示例包括：

* Bug
* 文档
* 重复
* 需要帮助
* 增强功能
* 问题

![GitHub 标签可用于对 GitHub 存储库问题和拉取请求进行分类。](https://learn.microsoft.com/zh-cn/training/github/introduction-to-github/media/2-labels.png)

若要详细了解 GitHub 标签，请参阅[关于标签](https://docs.github.com/en/free-pro-team@latest/github/managing-your-work-on-github/about-labels)。

## 操作

GitHub 操作在存储库中提供任务自动化和工作流功能。 操作可用于优化软件开发生命周期中的流程，并实现连续集成和连续部署 (CI/CD)。

GitHub Actions 由以下组件组成：

* **工作流** ：添加到存储库中的自动化流程。
* **事件** ：触发工作流的活动。
* **作业** ：在运行器上执行的一组步骤。
* **步骤** ：可运行一个或多个命令（操作）的任务。
* **操作** ：可合并到步骤中的独立命令。 可组合多个步骤来创建一个作业。
* **运行器** ：安装了 GitHub Actions 运行器应用程序的服务器。

![GitHub 操作提供了一种方法来自动执行软件开发生命周期。](https://learn.microsoft.com/zh-cn/training/github/introduction-to-github/media/2-actions.png)

若要详细了解 GitHub 操作，请参阅 [GitHub Actions 简介](https://docs.github.com/en/free-pro-team@latest/actions/learn-github-actions/introduction-to-github-actions)。

## 克隆和分支

GitHub 提供了多种复制存储库的方法供你使用。

* **克隆存储库** - 克隆存储库将在本地计算机上复制存储库及其历史记录。 如果你对存储库具有写入权限，可在更改完成时将更改从本地计算机推送到远程存储库（称为“原点”）。 若要克隆存储库，可使用 [`git clone [url]`](https://docs.github.com/en/free-pro-team@latest/github/using-git/getting-changes-from-a-remote-repository#cloning-a-repository) 命令或 GitHub CLI 的 [`gh repo clone [url]`](https://cli.github.com/manual/gh_repo_clone) 命令。
* **创建存储库分支**创建存储库分支会在 GitHub 帐户中生成存储库的副本。 父存储库被称为“上游”，分支副本称为“原点”。 一旦创建了存储库分支到 GitHub 帐户，就可将其“克隆”到本地计算机。 通过分支，可随意更改项目，而不会影响原始上游存储库。 若要将更改回馈到上游存储库，需要从已创建分支的存储库中创建一个“拉取请求”。 还可运行 `git` 命令，确保本地副本与上游存储库保持同步。

何时克隆存储库？何时又该创建存储库分支？ 如果正在使用存储库且具有写入权限，那么可将其克隆到本地计算机。 你可在此处进行修改，并将更改直接推送到原始存储库。

如果你需要使用由其他所有者（例如 `github/example`）创建的存储库，而且没有写权限，那么可将该存储库分支到 GitHub 帐户中，然后将该分支克隆到本地计算机上。 为了直观呈现这一点，假设你的 GitHub 帐户名为 `githubtraining`。 如果使用 GitHub 网站，可创建 `github/example` 或任何其他存储库分支到你的帐户。 在这里，可将存储库的分支版本克隆到本地计算机。 这些步骤如下图所示。

![创建存储库分支会在 GitHub 帐户中创建其副本。然后，可将存储库的分支副本克隆到本地计算机上。](https://learn.microsoft.com/zh-cn/training/github/introduction-to-github/media/2-fork-clone.png)

可对 `githubtraining/example` 的本地副本进行更改，然后将这些更改推送回到远程原始存储库 (`githubtraining/example`)。 接下来，可使用拉取请求将更改提交到 `github/example` 上游存储库，如下所示。

![可将本地更改推送到原始存储库，然后可创建一个拉取请求，将更改放入上游存储库。](https://learn.microsoft.com/zh-cn/training/github/introduction-to-github/media/2-fork-pullrequest.png)

若要了解详细信息，请参阅[创建存储库分支](https://docs.github.com/en/free-pro-team@latest/github/getting-started-with-github/fork-a-repo)。

## GitHub Pages

GitHub Pages 是一个托管引擎，内置于 GitHub 帐户中。 通过遵循一些约定并启用此功能，你可以构建你自己的从 HTML 中生成的静态站点，以及构建直接从存储库中拉取的 Markdown 代码。

![GitHub Pages 是 GitHub 帐户可用的托管引擎。它可用于托管从存储库生成的静态站点。](https://learn.microsoft.com/zh-cn/training/github/introduction-to-github/media/2-github-pages.png)

要了解详细信息，请参阅 [GitHub Pages](https://pages.github.com/)。

# 练习 - GitHub 的引导式教程

**已完成**100 XP

* 58 分钟

本练习检查有关 GitHub 关键功能的知识，包括提交分支、提交文件、打开拉取请求和合并拉取请求。

## 入门

单击下面的“在 GitHub 上开始练习”按钮后，将导航到一个公共 GitHub 模板存储库，该存储库会提示你完成一系列小挑战。 在开始本练习之前，请首先完成以下任务：

* 选择模板存储库中的“开始课程”按钮或“使用此模板”功能。 这会提示你创建新的存储库。 建议创建公共存储库，因为专用存储库会使用 Actions 分钟数。 通过模板创建自己的存储库后，请等待大约 20 秒，然后刷新。
* 按照存储库的 README 中的说明了解练习的工作原理、其学习目标以及如何成功完成练习。

在 GitHub 中完成练习后，请返回此处完成以下内容：

* 快速知识检查
* 浏览已学习内容的摘要
* 获得完成此模块的徽章

 备注

无需修改任何工作流文件即可完成本练习。 更改此工作流中的内容可能会破坏练习验证操作、提供反馈或对结果进行评分的功能。
