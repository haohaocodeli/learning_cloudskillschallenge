# Visual Studio Code 中的 Python 入门

# 简介

**已完成**100 XP

* 1 分钟

使用任何编程语言的第一步都是设置所需的工具。 大部分开发人员都使用 Visual Studio Code 之类的代码编辑器，因为这些工具为代码提供自动完成功能并突出显示语法错误。 代码编辑器还提供对一组丰富的加载项的访问权限，以进一步增强开发体验。

在此模块中，你将设置 Python 开发环境。 你将使用此空间来学习 Python 和构建多个应用程序。 你还将了解如何使用 Visual Studio Code 创建和运行 Python 文件。

完成本模块后，你安装了实现使用 Python 生成应用程序的目标所需的工具。

## 学习目标

学完本模块后，你将能够：

* 安装 Python 3。
* 在计算机上安装并配置 Visual Studio Code 和扩展。
* 创建 Python 文件。
* 在 Visual Studio Code 中编写并运行 Python 代码。

## 先决条件

* 能够在本地安装程序。
* 了解如何从命令或终端窗口打开和运行命令。
* 基本了解编程。

# 验证你的 Python 版本和安装

**已完成**100 XP

* 5 分钟

选择操作系统[ ] Linux[X] Mac[ ] Windows

你需要先在本地计算机上安装几个工具，然后才能开始编写 Python 代码。 你将需要编译和运行代码的 Python 解释器，以及包含可帮助你编写 Python 代码的功能的代码编辑器。 在本模块中，你将安装并配置所需的工具。

## Python 版本

在本模块中，我们将努力区分 Python 版本 2 和 Python 版本 3。 我们进行这种区分是因为 [Python 2](https://www.python.org/doc/sunset-python-2/) 已在 2020 年停止使用。 关键理念是要从现在开始使用 Python 3。

 备注

为什么强调需要使用 Python 3 十分重要？ 一些系统可能预安装了 Python 2，因此你需要执行额外步骤来安装 Python 3。

### 如何知道我的计算机上是否已安装了 Python 3？

计算机可能已安装 Python 3。 有时，应用程序会在你不知情的情况下安装 Python 3。

在此页面顶部，选择表示你操作系统的选项卡。

### macOS

若要确定 macOS 计算机是否已安装 Python 3，请执行以下操作：

1. 按 Command + 空格组合键打开终端应用，使用 Spotlight 进行搜索。
2. 在搜索框中，输入“终端”。 在结果集中选择“终端应用”，然后按 Return 启动应用。
3. 在命令提示符处，输入下列命令：
   **Bash**复制

   ```
   python3 --version
   ```

   备注

   运行 `python3 --version` 可能会返回一条错误消息，指出“找不到命令”。 这表示 iOS 系统上未安装 Python 3。

   你可能会看到返回输出包含 `Python` 一词，后跟一组由 `.` 字符分隔的数字，例如：
   **输出**复制

   ```
   Python 3.10.0
   ```

只要第一个数字是 `3`，就表示计算机上已安装 Python 3。 即使没有最新版本，也能够遵循 Microsoft Learn 上的任何初级 Python 模块。

如果收到错误消息，则需要安装 Python 3。 我们将在下一个单元中演练如何安装 Python 3。

## 回顾

本单元的主要要点是：

* 不应再使用 Python 版本 2。 应使用 Python 版本 3 编写任何新代码。
* 使用 Python 的 `--version` 标志可确保你知道所使用的 Python 版本。

# 安装 Python 3

**已完成**100 XP

* 5 分钟

选择操作系统[ ] Linux[X] Mac[ ] Windows

在上一个练习中，你运行了命令以确定是否安装了 Python 3。 如果需要安装 Python 3，请在此页面顶部选择操作系统，然后按照以下说明进行操作。

确定安装了 Python 3 后，可以滚动到此页面底部，然后选择“继续”。

编写本模块时，Python 3.11 是可用的最新版本，因此，以下说明将引用该版本。 安装适用于你的操作系统的最新版 Python。 如果安装了不同版本，则你看到的按钮标签和文件名可能与安装说明中的内容略有不同。

## 在 macOS 上安装 Python

请按照以下步骤从 Python 网站下载 Python 安装程序。

 备注

可以使用 Homebrew 安装 Python 和 Visual Studio Code。 有关说明，请参阅 [Homebrew 文档](https://docs.brew.sh/Homebrew-and-Python?azure-portal=true)。

1. 从 [Python 下载页面](https://www.python.org/downloads/macos)下载安装程序。
   网站应自动将你定向到专门用于 macOS 的页面。 选择最新版本。
   你可能会看到一个对话框，提示你允许从 python.org 进行下载。选择“允许”。
   片刻之后，名为 python-3.10.2-macos11.pkg 的文件（或类似文件）应下载到你的 Dock 中的 Downloads 堆栈。
2. 若要启动安装程序，请双击下载的 .pkg 文件。 Python 安装程序将提示你安装、验证并接受各种选项和许可协议。 花些时间阅读这些提示，以了解安装程序将在计算机上执行的操作。
   安装过程完成时，将出现 Finder 窗口，其中显示 Python 文件夹的内容和祝贺屏幕。 选择“关闭”以关闭这些窗口。
   如果系统提示将 Python 安装程序移动到回收站，则可以这样做。
3. 在终端窗口中运行 `python3.10 --version` 来验证安装：
   **Bash**复制

   ```
   python3.10 --version
   ```

   输出包括 `Python` 一词，以及一组由 `.` 字符分隔的数字，例如：

   **输出**复制

   ```
   Python 3.10.0
   ```

   只要第一个数字是 `3`，便表示已成功安装 Python 3。

现在，你已在本地系统上成功安装了 Python。

---

# 安装 Visual Studio Code

**已完成**100 XP

* 5 分钟

选择操作系统[ ] Linux[X] Mac[ ] Windows

在系统上安装 Python 后，就可以将注意力转向编写 Python 代码的工具。 如本模块简介中所述，虽然你可以使用纯文本编辑器来创建或编辑 Python 应用程序，但使用代码编辑器（如 Visual Studio Code）将提供更高级别的支持。

让我们来了解通过 Visual Studio Code 提供的工具包以及安装方法。

## 用于编写 Python 代码的工具

通常会在文本文件中编写 Python 语法，并将它保存到本地硬盘。

可以使用简单的文本文件编辑器（如 Windows 中的记事本）编写代码。 记事本可编辑 ASCII 文本（一种标准文本文件格式）。

你希望避免使用任何具有格式设置选项（如粗体、下划线或斜体）的文本编辑器或是任何其他具有字处理功能的程序。 因此，不应在 Microsoft Word 或 macOS 上的 TextEdit 中编写代码。 这些程序包含 Python 编译器无法理解的格式设置指令。

你希望使用最适合于独有代码编写挑战的工具。 有很多选项可供选择，但许多开发人员依赖于 Visual Studio Code 或 VS Code。 它是免费的，可在 Windows、macOS 和 Linux 上使用。 它具有许多功能，使你可以轻松地导航和编译所有编程语言的代码。

Microsoft 提供了适用于 Visual Studio Code 的 Python 扩展。 此扩展可提供语法突出显示、代码导航和代码格式设置支持等功能。 特别是一种名为 IntelliSense 的功能在你刚开始使用时会非常有用。 Intellisense 可在你键入时提供自动完成功能和上下文帮助。 你将在下一个单元中安装该工具。

## 在 macOS 上安装 Visual Studio Code

此部分将指导你完成下载并安装 Visual Studio Code 的过程。

1. 在浏览器中，导航到 [Visual Studio Code 下载页面](https://code.visualstudio.com/Download?azure-portal=true)。
   该网页会显示 Windows、Linux 和 Mac 的徽标。
2. 下载 Mac 版本。 大多数浏览器会提供将文件保存到本地计算机（通常是在 Downloads 文件夹中）或立即运行文件的选项。
   你应将文件先移动到 Applications 文件夹，然后再打开它，如后续步骤所述。
3. 打开 Finder。 在 Finder 中将 Visual Studio Code 文件从 Dock 上的 Downloads 堆栈拖动到 Applications 文件夹。
4. 在 Applications 文件夹中双击“Visual Studio Code”应用。
   重要

   你可能会看到一个警告，指示无法打开 Visual Studio Code，因为 Apple 无法检查它是否为恶意软件。 如果发生这种情况，请选择“确定”关闭消息，然后，在“Applications”文件夹中右键单击“Visual Studio Code”，并选择“打开菜单”。 Visual Studio Code 应打开，而不会出现任何其他问题。

# 安装 Python 扩展

**已完成**100 XP

* 5 分钟

选择操作系统[ ] Linux[X] Mac[ ] Windows

安装 Visual Studio Code 后，可以安装 Python 扩展，还可以选择设置其他工具和设置。

## 安装适用于 Visual Studio Code 的 Python 扩展

Visual Studio Code 既是一种功能强大的代码编辑器，也是一种轻型通用[集成开发环境](https://wikipedia.org/wiki/Integrated_development_environment?azure-portal=true) (IDE)，具有多种扩展，可提供使用各种编程语言的功能。 适用于 Visual Studio Code 的 Python 扩展提供了视觉提示（如颜色编码和自动完成）和调试工具，可帮助编写更好的 Python 代码并更快地编写代码。 本练习将 Python 扩展安装到现有 VS Code 应用程序。

1. 在 Visual Studio Code 中，选择“查看”>“扩展”以打开“扩展”视图。
   ![“扩展”视图的菜单选项的屏幕截图。](https://learn.microsoft.com/zh-cn/training/modules/python-install-vscode/media/visual-studio-code-extensions-open.png)
   Visual Studio Code 的“扩展”视图列出了已安装的扩展和市场中最受欢迎的推荐扩展。
2. 若要筛选可用扩展列表，请在“扩展”视图顶部的搜索框中输入 python。
3. 选择 Microsoft 发布的“Python”扩展（描述为 IntelliSense (Pylance)，通常是列表中的第一个）。 有关该扩展的详细信息将出现在右侧的选项卡式面板中。
4. 在“扩展”面板或主面板中，选择“安装”。
   ![macOS 的“扩展”面板中搜索结果的屏幕截图，其中突出显示了“Python 安装”。](https://learn.microsoft.com/zh-cn/training/modules/python-install-vscode/media/visual-studio-code-extensions-install.png)

   安装完成后，“安装”按钮更改为“扩展”视图中的“设置 ⚙️”图标或主面板中的两个按钮，即“禁用”和“卸载”。 此消息使你知道已成功安装了适用于 macOS 的 Python 扩展。

   重要

   安装 Python 扩展之后，你可能会看到一个对话框，询问你是否要安装命令行开发人员工具。 应选择“安装”。 需要同意命令行工具许可协议。 安装过程可能需要长达 20 分钟或更长时间，具体取决于 Internet 连接。 安装完成之后，你会看到一个对话框，指出已安装了软件。 选择“完成”以继续操作。

## 摘要

你已成功安装适用于 Visual Studio Code 的 Python 扩展。 让我们来创建第一个 Python 应用程序！

# 创建首个 Python 应用程序

**已完成**100 XP

* 5 分钟

选择操作系统[ ] Linux[X] Mac[ ] Windows

安装 Python 和 Python 工具后，可以创建第一个 Python 应用程序！ 在本练习中，你将创建一个空文件夹，在 Visual Studio Code 中打开该文件夹，然后创建你的第一个应用程序。

## 步骤 1 - 在项目文件夹中启动 VS Code

许多项目都是从一个空文件夹开始的，这就是你创建自己项目的方式。

1. 使用命令提示符或终端，创建名为“hello-world”的空文件夹，导航到该文件夹，然后输入以下命令，打开该文件夹 (.) 中的 VS Code（代码）：

   1. 创建一个名为 hello-world 的新文件夹：
      **Bash**复制

      ```
      mkdir hello-world
      ```

   2. 导航到 hello-world 文件夹：
      **Bash**复制

      ```
      cd hello-world
      ```

   3. 在该文件夹中打开 Visual Studio Code：
      **Bash**复制

      ```
      code .
      ```

   提示

   以管理员身份打开命令提示符或终端以运行 `code .`

   或者，可以通过操作系统 UI 运行 VS Code，然后使用“文件”>“打开文件夹”打开项目文件夹。

## 步骤 2 - 创建新 Python 文件并添加代码

现在，打开 Visual Studio Code 并创建空文件夹后，你将创建一个 Python 文件以显示消息“Hello, World”。

1. 在“资源管理器视图”HELLO_WORLD 面板中，将鼠标悬停在标题栏上，然后选择“新建文件”。
   ![Visual Studio Code“资源管理器”窗口的屏幕截图，其中突出显示了“新建文件”。](https://learn.microsoft.com/zh-cn/training/modules/python-install-vscode/media/visual-studio-code-new-file.png)
2. 在新文本框中输入新文件名称 hello.py，然后按 Enter，对其进行命名。
   ![“资源管理器”窗口的屏幕截图，其中为新文件输入了名称 hello.py。](https://learn.microsoft.com/zh-cn/training/modules/python-install-vscode/media/visual-studio-code-name-file.png)
   通过使用 `.py` 文件扩展名，可以告诉 VS Code 将此文件解释为 Python 程序，以便它使用 Python 扩展名来评估内容。
3. 在编辑器面板中输入以下 Python 代码。 运行应用程序时，此命令使用 `print` 函数来显示文本“Hello, World!”。
   **Python**复制

   ```
   print('Hello, World!')
   ```

4. 通过选择“文件”和“保存”（或 Ctrl+S）保存文件。
   ![突出显示了“保存”的文件菜单的屏幕截图。](https://learn.microsoft.com/zh-cn/training/modules/python-install-vscode/media/visual-studio-code-save-file.png)

## 步骤 3 - 运行应用程序

由于它是单行程序，因此实际上可以从 Visual Studio Code 内部运行应用程序。

1. 选择“视图”和“终端”，打开 Visual Studio Code 中的内置终端。
   ![突出显示了“终端”的视图菜单的屏幕截图。](https://learn.microsoft.com/zh-cn/training/modules/python-install-vscode/media/visual-studio-code-open-terminal.png)
2. 在新的终端窗口中，运行以下命令以运行 Python 代码。
   **Bash**复制

   ```
   python3 hello.py
   ```

   ![运行 Python 代码的屏幕截图。](https://learn.microsoft.com/zh-cn/training/modules/python-install-vscode/media/visual-studio-code-run-code.png)
   *Hello, World!* 在终端窗口中显示。 祝贺你！ 你已创建了 Python 应用程序！

## 知识检查

**1.** 当前支持的 Python 主要版本是什么？

[ ] Python 1

[ ] Python 2

[ ] Python 3

正确！ 当前支持的 Python 版本为 Python 3。

**2.** 用于在屏幕上显示信息的 Python 函数有哪些？

[ ] `len`

[ ] `print`

正确！ 在屏幕上显示信息的 Python 函数是 `print`。

[ ] `open`

**3.** Python 文件通常使用什么文件扩展？

[ ] Python

[ ] p

[ ] py

正确！ .py 是 Python 文件的标准扩展名。

# 摘要

**已完成**100 XP

* 1 分钟

我们的目标是创建一个开发环境，以开始编写 Python 代码。

你安装了 Python 3、Visual Studio Code 和适用于 Visual Studio Code 的 Python 扩展。 你还创建了你的第一个 Python 应用程序。

你已迈出了学习 Python 的第一步。 接下来，你将会编写程序和脚本来分析数据、运行网站以及许多其他应用程序。
