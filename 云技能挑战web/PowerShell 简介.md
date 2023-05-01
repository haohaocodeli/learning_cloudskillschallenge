# PowerShell 简介

了解 PowerShell 的基础知识。 此跨平台命令行 shell 和脚本语言是专为任务自动化和配置管理设计的。 你将了解一些基础知识，例如 PowerShell 的涵义、它的用途以及使用方法。

## 学习目标

完成此模块后，你将能够：

* 了解 PowerShell 的涵义及其用途。
* 使用命令自动执行任务。

[开始](https://learn.microsoft.com/zh-cn/training/modules/introduction-to-powershell/1-introduction/)添加

## 先决条件

* 基本熟悉如何使用命令行 shell（如命令提示符或 Git Bash）
* 已安装 Visual Studio Code
* 能够安装 Visual Studio Code 扩展
* 如果不使用 Windows 操作系统，则能够在计算机上安装软件

## 此模块属于这些学习路径

* [使用 PowerShell 自动执行管理任务](https://learn.microsoft.com/training/paths/powershell/)
* [简介](https://learn.microsoft.com/zh-cn/training/modules/introduction-to-powershell/1-introduction)1 分钟
* [什么是 PowerShell？](https://learn.microsoft.com/zh-cn/training/modules/introduction-to-powershell/2-what-is-powershell)4 分钟
* [练习 - 运行你的第一段 PowerShell 命令](https://learn.microsoft.com/zh-cn/training/modules/introduction-to-powershell/3-exercise-powershell)1 分钟
* [查找命令](https://learn.microsoft.com/zh-cn/training/modules/introduction-to-powershell/4-cmdlets)3 分钟
* [练习 - 查找命令](https://learn.microsoft.com/zh-cn/training/modules/introduction-to-powershell/5-exercise-cmdlets)2 分钟
* [知识检查](https://learn.microsoft.com/zh-cn/training/modules/introduction-to-powershell/6-knowledge-check)4 分钟
* [总结](https://learn.microsoft.com/zh-cn/training/modules/introduction-to-powershell/7-summary)1 分钟

# 简介

PowerShell 是一种命令行 shell 和脚本语言一体化工具。 它被设计为任务引擎，使用 cmdlet 来包装用户需要执行的任务。 在 PowerShell 中，可以在本地或远程计算机上运行命令。 可以执行管理用户和自动执行工作流等任务。

无论你是运营团队的成员还是采用 DevOps 原则的开发团队的成员，均可使用 PowerShell。 你可以使用它来处理各种任务，如管理云资源以及持续集成和持续交付 (CI/CD)。 PowerShell 提供了许多有用的命令，但你可以通过安装模块随时扩展其功能。

安装 PowerShell 时，可以评估其功能是否适合你的团队。

## 学习目标

完成此模块后，你将能够：

* 了解 PowerShell 的涵义及其用途
* 使用命令自动执行任务

## 先决条件

* 基本熟悉如何使用命令行 shell（如命令提示符或 Git Bash）
* 已安装 Visual Studio Code
* 能够安装 Visual Studio Code 扩展
* 如果不使用 Windows 操作系统，则能够在计算机上安装软件

# 什么是 PowerShell？

PowerShell 由命令行 shell 和脚本语言两部分组成。 它最初是一种框架，用于在 Windows 中自动执行管理任务。 PowerShell 现已发展为一种跨平台工具，用于执行多种任务。

命令行 shell 缺少图形界面，让你无法使用鼠标与图形元素进行交互。 相反，你需要在计算机控制台中键入文本命令。 下面是使用控制台的一些优点：

* 与控制台交互通常比使用图形界面快。
* 在控制台中，可以运行成批命令，因此它非常适合用于持续集成管道的任务自动化。
* 你可使用控制台与云资源和其他资源交互。
* 可在文本文件中存储命令和脚本，并使用源代码管理系统。 这可能是最大的优点之一，因为你的命令可重复且可审核。 在许多系统（特别是政府系统）中，必须跟踪和评估或审核一切内容。 审核涵盖了从数据库更改到脚本所做的更改的所有内容。

## 功能

PowerShell 通过传统 shell 共享某些功能：

* 内置帮助系统：大多数 shell 都有一些帮助系统，你可以在其中了解有关命令的详细信息。 例如，你可以了解命令的作用以及它支持的参数。 PowerShell 中的帮助系统提供有关命令的信息，并与联机帮助文章集成。
* 管道：传统 shell 使用管道按顺序运行多个命令。 一个命令的输出是下一个命令的输入。 PowerShell 实现了传统 shell 传达的这种概念，但它又有所不同，因为它对文本上的对象进行操作。 本模块稍后会详细介绍此功能。
* **别名** ：别名是可用于运行命令的替代名称。 PowerShell 支持使用常见别名，如 `cls`（清除屏幕）和 `ls`（列出文件）。 因此，对于熟悉的命令，新用户可利用其对其他框架的知识，而不必记住 PowerShell 名称。

PowerShell 不同于传统的命令行 shell，具体体现在以下几方面：

* **它对文本上的对象进行操作。** 在命令行 shell 中，你必须运行输出和输入可能不同的脚本，因此你最终会对输出进行格式化并提取所需的数据。 而在 PowerShell 中，可以使用对象作为输入和输出。 这意味着格式设置和数据提取所需时间会更少。
* **它具有 cmdlet。** PowerShell 中的命令称为 cmdlet（念作 commandlet）。 与其他许多 shell 环境不同，在 PowerShell 中，cmdlet 是在常见运行时而不是单独的可执行文件上生成的。 此特性在参数分析和管道行为方面提供了一致的体验。
  Cmdlet 通常采用对象输入并返回对象。 PowerShell 中的核心 cmdlet 是在 .NET Core 中生成的，采用的是开放源代码形式。 你可以使用来自社区和其他来源的更多 cmdlet、脚本和函数来扩展 PowerShell，也可以在 .NET Core 或 PowerShell 中生成自己的 cmdlet。
* **它具有多种类型的命令。** PowerShell 中的命令可以是本机可执行文件、cmdlet、函数、脚本或别名。 运行的每个命令都属于这些类型之一。 由于 cmdlet 是一种命令，因此，命令和 cmdlet 通常可互换使用。

## 安装

在此模块中，你将练习如何在计算机上使用 PowerShell。 PowerShell 可用于多种平台，但如果你使用的计算机运行的是 Linux、macOS 或早期版本的 Windows，则需要安装它。

每个 OS 对安装 PowerShell 的说明各不相同。 在继续之前，请花几分钟时间安装 PowerShell 或验证 PowerShell 安装。 此模块的下一个单元将介绍如何验证你的安装。

### Windows

如果运行的是 Windows 8 或更高版本，则应已安装名为 Windows PowerShell 的 PowerShell 版本。 此版本与最新的 PowerShell 版本略有不同，但它可用于学习目的。

可从“开始”菜单打开 Windows PowerShell。

### 其他操作系统

如果你的计算机运行的不是 Windows 8 或更高版本，则需要安装 PowerShell。 若要查找针对你的 OS 的安装说明，请参阅[安装各种版本的 PowerShell](https://learn.microsoft.com/zh-cn/powershell/scripting/install/installing-powershell)。

### 适用于 Visual Studio Code 的 PowerShell 扩展

建议你使用[适用于 Visual Studio Code 的 PowerShell 扩展](https://marketplace.visualstudio.com/items?itemName=ms-vscode.PowerShell)来创作 PowerShell 脚本和运行此模块中的命令。 使用此扩展，可运行命令，还有助于执行代码片段、完成代码以及突出显示语法。

# 练习 - 运行你的第一段 PowerShell 命令

Microsoft Learn 需要许可才能创建 Azure 资源。

有关详细信息，请参阅[疑难解答指南页](https://learn.microsoft.com/en-us/training/support/troubleshooting)。

[检查权限](https://login.microsoftonline.com/redeem?rd=https%3a%2f%2finvitations.microsoft.com%2fredeem%2f%3ftenant%3d604c1504-c6a3-4080-81aa-b33091104187%26user%3dacd6979b-0e34-4537-9794-5fc2ea5aa472%26ticket%3dfkzUTOYe2iPRPXrNrRilxYN%25252fUHzjtjAnqPt6IGUesjs%25253d%26ver%3d2.0)

在本单元中，你将使用 Azure Cloud Shell 作为 Linux 终端。 也可通过 Azure 门户或 [Cloud Shell 登录](https://shell.azure.com/)访问 Cloud Shell。 无需在电脑或笔记本电脑上安装任何资源即可使用 Cloud Shell。

 备注

在本模块中，你将使用右侧的 Cloud Shell，但在实际情况下，还可以使用 Visual Studio Code 中的集成终端，方式如下：选择“终端”>“新建终端”，然后在“终端”窗口左上角的下拉菜单中选择“Powershell”。

开始本练习之前，请务必先激活沙盒。

1. 在 Cloud Shell 中运行以下命令，然后按 Enter 验证系统是否已设置为使用 PowerShell。 `$PSVersionTable` 将验证安装情况。
   **PowerShell**复制

   ```
   $PSVersionTable
   ```

   输出如下表所示：

   **输出**复制

   ```
    Name                           Value
    ----                           -----
    PSVersion                      7.1.4
    PSEdition                      Core
    GitCommitId                    7.1.4
    OS                             Linux 5.4.0-1058-azure #60~18.04.1-Ubuntu SMP Tue Aug 31 20:34:4…
    Platform                       Unix
    PSCompatibleVersions           {1.0, 2.0, 3.0, 4.0…}
    PSRemotingProtocolVersion      2.3
    SerializationVersion           1.1.0.1
    WSManStackVersion              3.0
   ```

   输出提供有关 PowerShell 版本以及平台和版本的信息。
   有关仅限于你的 PowerShell 版本的信息，可运行修改后的 `$PSVersionTable` 版本。
2. 在 Cloud Shell 中运行以下命令，然后按 Enter。
   **PowerShell**复制

   ```
   $PSVersionTable.PSVersion
   ```

   输出现在如下表所示：

   **输出**复制

   ```
   Major  Minor  Patch  PreReleaseLabel BuildLabel
   -----  -----  -----  --------------- ----------
   7      1      4  
   ```

   此输出提供更多有关 PowerShell 版本的详细信息。

运行 `$PSVersionTable` 会导致输出类似于一个表，但实际上是一个对象。 因此，可使用句点 (`.`) 访问 `PSVersion` 等特定属性。

# 查找命令

cmdlet（发音为“command-let”）是已编译的命令。 可在 .NET 或 .NET Core 中开发 cmdlet，并在 PowerShell 中将其作为命令进行调用。 PowerShell 安装中提供了数千个 cmdlet。 难点在于了解它们是什么，以及它们能为你解决什么问题。

Cmdlet 根据动词-名词命名标准命名。 此模式可帮助你了解它们的作用以及搜索它们的方式。 它还有助于 cmdlet 开发人员创建一致的名称。 可通过使用 `Get-Verb` cmdlet 来查看已批准的动词的列表。 动词按活动类型和功能进行组织。

下面是运行 `Get-Verb` 的输出部分：

**输出**复制

```
Verb        AliasPrefix Group          Description
----        ----------- -----          -----------
Add         a           Common         Adds a resource to a container, or atta…
Clear       cl          Common         Removes all the resources from a contai…
```

此列表显示动词及其说明。 cmdlet 开发人员应使用已批准的动词，同时确保动词说明符合其 cmdlet 的功能。

下面的三个核心 cmdlet 可让你深入了解存在哪些 cmdlet 以及它们的作用：

* **Get-Command** ：`Get-Command` cmdlet 列出系统上的所有可用 cmdlet。 筛选列表以快速找到所需的命令。
* Get-Help：运行 `Get-Help` 核心 cmdlet，以调用内置帮助系统。 还可以运行别名 `help` 命令来调用 `Get-Help`，但通过对响应进行分页来改善读取体验。
* **Get-Member** ：调用命令时，响应是包含多个属性的对象。 运行 `Get-Member` 核心 cmdlet 向下钻取到该响应并了解其详细信息。

## 使用 Get-Command 查找命令

在 Cloud Shell 中运行 `Get-Command` cmdlet 时，将获取 PowerShell 中安装的每个命令的列表。 由于安装了上千个命令，因此需要一种方法来筛选响应，以便可以快速找到所需的命令。

要筛选列表，请记住 cmdlet 的动词-名词命名标准。 例如，在 `Get-Random` 命令中，`Get` 是动词，`Random` 是名词。 使用标志来定位所需命令中的动词或名词。 指定的标志应为一个字符串值。 你可将模式匹配字符添加到该字符串，以确保你明确这样做，例如标志的值应以特定字符串开头或结尾。

以下示例演示如何使用标志来筛选命令列表：

* **-Noun** ：`-Noun` 标志以与名词相关的命令名称部分为目标。 也就是说，它的目标是连字符 (`-`) 后面的所有内容。 下面是命令名称的典型搜索：
  **PowerShell**复制

```
  Get-Command -Noun a-noun*
```

  此命令搜索名词部分以 `a-noun` 开头的所有 cmdlet。

* **-Verb** :`-Verb` 标志以与动词相关的命令名称部分为目标。 可结合使用 `-Noun` 标志和 `-Verb` 标志来创建更详细的搜索查询和类型。 下面是一个示例：
  **PowerShell**复制

```
  Get-Command -Verb Get -Noun a-noun*
```

  现在已缩小搜索范围，以指定动词部分需要匹配 `Get`，名词部分需要匹配 `a-noun`。
