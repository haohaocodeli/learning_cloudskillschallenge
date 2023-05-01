# 面向 Web 开发人员的 Visual Studio Code 简介

Visual Studio Code 是一款开放源代码的轻型文本编辑器，不仅功能完善，还支持面向所有开发人员的多种扩展。 如果想深入探索 Web 开发中的宽广领域，Visual Studio Code 将是一款很有用的工具。 该工具内置诸如构建脚本、环境、调试等功能，再结合强大的文本编辑器的作用，对新开发人员特别有用。 Visual Studio Code 在一个环境中处理所有事务且无需旧的高度集成开发环境 (IDE)。

Visual Studio Code 基于名为 Electron 的平台构建，并且可用于 Windows、macOS 和 Linux。 该学习模块将尽可能独立于平台。 尽管一些屏幕截图可能来自特定平台，但该信息应通过一些小的调整（例如快捷键组合）转移到任何平台。

下面是 Visual Studio Code 的一些主要功能的列表：

* 轻型
* 多平台
* 颜色编码
* 内置调试程序
* 集成终端
* 集成 git 支持
* IntelliSense 自动完成
* 开源
* 可扩展

在此模块中，你将了解如何使用一些基本 Web 开发扩展来安装和使用 Visual Studio Code，然后使用这些功能构建一个非常简单的 Web 应用程序。 即使你从未编写过 Web 应用，也仍然可以成功使用此模块。 如果你是经验丰富的 Web 开发人员，仍可以在此处学到许多有用的内容，从而开始使用 Visual Studio Code。

# 安装并浏览 Visual Studio Code

**已完成**100 XP

* 10 分钟

首先，下载并本地安装 Visual Studio Code，然后快速导览用户界面 (UI) 和功能。 建议在安装时执行这些步骤，但如果愿意也可以阅读“教程”一节而无需遵循这些步骤。

## 下载

浏览到 [https://code.visualstudio.com](https://code.visualstudio.com/) 并选择适用于你的平台的稳定版本。 预览体验成员版本类似于使用下一次更新的 beta 测试版，但并不适用于此学习模块。 如果没有看到你指定的平台，请选择[其他下载](https://code.visualstudio.com/#alt-downloads)以查看当前所有支持的版本。

## 安装

在安装期间，请务必查看所提供的选项，选择任何你想要选择加入的功能。 这些选项主要是为了方便和个人偏好，以便可以接受默认设置以简化安装。 以下是 Windows 选项及其默认值。

![Windows installation options.](https://learn.microsoft.com/zh-cn/training/windows/develop-web-apps-with-vs-code/media/install-options.png)

首次运行时请花费片刻时间检查可用更新。 在 Windows 上，可使用“帮助”下拉菜单并选择“检查更新”轻松完成此步骤。 在其他平台上此选项可能显示在其他下拉菜单位置中。

## 教程

让我们看看用户界面的一些重要功能和 Visual Studio Code 的核心功能的简短教程。 首次运行 Visual Studio Code 时，应看到类似于下面的屏幕截图的“欢迎”页面。 如果没有看到欢迎页，可以使用“帮助”>“欢迎”下拉菜单项来访问它。

![First run after installation.](https://learn.microsoft.com/zh-cn/training/windows/develop-web-apps-with-vs-code/media/welcome.png)

### 用户界面

你注意到的第一件事可能是界面看起来是如此简单。 这是设计使然，但简单的界面却隐藏了此编辑器的真实强大功能。 现在，请了解主要 UI 组件。

![User interface components.](https://learn.microsoft.com/zh-cn/training/windows/develop-web-apps-with-vs-code/media/interface.png)

你很可能会发现一个相当有价值的 UI 功能 - 命令面板（在任何平台上为 F1，Windows 中为 Ctrl+Shift+P，并在“视图”下拉菜单中列出）。 如果你有一个想要在 Visual Studio Code 中执行的操作，但却无法回想起确切的操作方法，这是一个很好的起点。

![Command palette.](https://learn.microsoft.com/zh-cn/training/windows/develop-web-apps-with-vs-code/media/f1.png)

默认情况下，命令面板以命令模式出现，由 `>` 提示符表示。 此模式包括大多数 Visual Studio Code 功能，包括查找键盘快捷方式。 但是此模式中可用的功能远不止这些。 有关列表，请按 F1 + Backspace 以删除命令提示符 (`>`) 并键入问号 (`?`)。 如果愿意请花费片刻时间探索这些模块。

### 颜色主题

更改编辑器的外观对于我们大多数人来说是很重要的。 Visual Studio Code 使用主题让此操作变得简单。 在欢迎页上，选择“自定义”下的“颜色主题”，然后可看到如下的内容。

![Color themes list.](https://learn.microsoft.com/zh-cn/training/windows/develop-web-apps-with-vs-code/media/color-themes.png)

 备注

也可以使用其他方法转到此列表，例如命令面板、下拉菜单和键盘快捷方式。

利用此机会来试用不同的颜色主题。 如果你对默认主题不满意，还可使用许多扩展，为 UI 带来更多视觉功能。

### 工具和扩展

单击“自定义”下的“工具和语言”，将看到左侧窗格扩展并显示当前可用扩展的列表，与下图类似。 还可以使用“视图”菜单，然后选择“扩展”。 请注意，第一个选项会将筛选器 `@category:"programming languages"` 添加到扩展列表，以在该类别中仅显示扩展。 可自行编辑此筛选器，或使用“清除扩展输入”按钮（在下面的屏幕截图中突出显示）清除它。

![Tools and Languages Extensions.](https://learn.microsoft.com/zh-cn/training/windows/develop-web-apps-with-vs-code/media/tools-list.png)

现在我们不会安装这些扩展，但可以花点时间随意滚动列表来了解各种可用选项。 下一单元将更深入地探讨扩展。

# 使用和安装扩展

**已完成**100 XP

* 10 分钟

在本单元中，你将了解查找和安装 Visual Studio Code 扩展是如此的简单。 如上所述，Visual Studio Code 会安装许多内置扩展，但其不会与对所有开发语言和环境的支持绑定。 通过使用扩展市场，可以查找特定工作流或个人首选项所需的工具、语言和调试程序。 此外，Visual Studio Code 还提供许多功能强大的扩展，以实现更好的自定义和控制，提高效率，甚至增添乐趣。

## 扩展市场

在上一单元中，你看到了访问扩展市场时显示的默认列表。 现在我们来更深入地了解该表，并安装一些扩展。

### 搜索扩展

Visual Studio Code UI 左侧是活动栏。 如果没有看到活动栏，请导航下拉菜单序列，将其切换为开：“查看”>“外观”>“显示活动栏”。 “扩展”图标在下图中突出显示。

![Extensions Marketplace icon.](https://learn.microsoft.com/zh-cn/training/windows/develop-web-apps-with-vs-code/media/activity-icon-extensions.png)

默认情况下，显示所有活动图标。 如果看不到此图标，请右键单击活动栏的空白区域以查看可用图表列表，然后选择“扩展”。 通过选择如下所示的图标打开“扩展”列表。

 备注

扩展提供有键盘快捷方式。 将鼠标悬停在“扩展”图标可查看你的扩展（因平台而异）。

首次安装任何扩展时，将只能看见市场中的常用扩展列表。

![Example list of extensions.](https://learn.microsoft.com/zh-cn/training/windows/develop-web-apps-with-vs-code/media/default-extensions-list.png)

通过此列表浏览扩展是一种方式，但由于可用扩展很多，使用顶部的“搜索”框通常更快捷。

要了解给定扩展类别的多种可用选择，请在搜索框中键入“图标”。 应看到按默认顺序排序（安装次数和评分组合）的多页扩展。 可通过选择“扩展”区域右上角的省略号图标 (`...`) 排序方式进行更具体的排序。

### 安装和管理扩展

只需单击市场中扩展项上的“安装”按钮即可轻松安装。 让我们安装多个扩展。 使用“搜索”框查找下列扩展，然后使用每个扩展上的“安装”按钮（稍后将深入探讨每个扩展的功能）：

* Material Theme
* Prettier Now
* Bracket Pair Colorizer
* Live Server

安装、删除、禁用和启用扩展时，该按钮可能会变为“重载”按钮。 如果适用，请确保选择该按钮。

#### Material Theme

我们一起来玩一玩，娱乐一下。 安装完成且就绪后，调出颜色主题（请记住有多种方式可以打开颜色主题：通过下拉菜单序列、通过键盘快捷方式，以及通过欢迎页）。 我们使用直接快捷方式 Ctrl-K、Ctrl-T（macOS 上为 Cmd-K、Cmd-T）。 现在使用向上和向下键更改主题。 选择新主题时将立即看见此更改。 尝试列表中显示的材料主题以找到你喜欢的主题。 即使你现在没有选择喜欢的主题，如果你像我们中的许多人一样，你最终也会想要偶尔快速改变一下颜色主题。 添加许多选项有助于解决此问题，所以请随意添加更多主题。

此扩展在此处演示自定义功能。 如果不喜欢主题，可放心删除或禁用。

#### Prettier Now

此扩展是一个美化工具。 如果你尚不知道，该术语指的是编辑器可通过使用某种适用的规则来自动格式化代码，该规则被设计器确定为适合你所使用的代码类型，因此该工具用起来可能会比较微妙，但非常实用。 扩展市场中提供了许多美化工具，但只有这一个工具提供的选项最多并且易于使用。

同样，如果你不喜欢此扩展，请随意禁用或选择其他扩展。

#### Bracket Pair Colorizer

如同我们已经安装的美化工具和主题，此扩展通过视觉反馈有助于你提高编码效率，但并不是 Web 开发所必需的。 但是，此扩展的确可大量减少进行故障排除所用的时间，还可缓解你的视觉疲劳。

#### Live Server

此扩展为本地开发服务器提供静态和动态页面的实时重载功能。 它通过提供对 Web 浏览器中的内容的实时更新极大地简化了 Web 开发。 和大多数扩展一样，市场中还有此功能的其他选项，但我们目前只用这一个。

这是我们在后续单元中将使用的唯一扩展，其他模块可能也会指导你安装该扩展或类似的扩展。 接下来，我们将汇总一个简单网页，并将介绍的扩展的工作原理。

---

## 下一单元: 在 Visual Studio Code 中创建并自动生成文件

# 在 Visual Studio Code 中创建并自动生成文件

**已完成**100 XP

* 10 分钟

与大多数的 Visual Studio Code 功能一样，创建和管理文件的方法有许多种。 在本单元中，我们将创建和编辑文件。 建议在本地计算机上创建一个名为“intro-to-vscode”的文件夹，然后在其中进行操作。 尽管可以将此文件夹视为此模块的项目文件夹，但 Visual Studio Code 不会创建除此课程所需的指定文件以外的任何文件，除非创建一个工作区，该内容将在此单元的末尾进行讨论。

## 使用资源管理器管理文件

如下所示，“资源管理器”按钮可以打开和关闭侧栏中的资源管理器视图。

![Explorer icon.](https://learn.microsoft.com/zh-cn/training/windows/develop-web-apps-with-vs-code/media/activity-icon-explorer.png)

应看见此处所示的“打开文件夹”按钮。

![Open folder button.](https://learn.microsoft.com/zh-cn/training/windows/develop-web-apps-with-vs-code/media/open-folder-explorer.png)

选择此按钮，然后导航到之前创建的 intro-to-vscode 文件夹。

## 创建 HTML 文件

在此情况下可能尚无任何文件，因此文件夹是空的。 现在让我们解决此问题。 使用如下所示的“新建文件”按钮，在当前文件夹中创建新文件。 请注意，除非将鼠标光标悬停于资源管理器的某一处，否则此图标不会显示。

![New File icon.](https://learn.microsoft.com/zh-cn/training/windows/develop-web-apps-with-vs-code/media/new-file-icon.png)

将新文件命名为 `index.html`，然后按 Enter。

## 使用 Emmet 创建代码

现在应有一个名为 `index.html` 空文件在编辑器中打开并在资源管理器中列出。 如果开始键入有效的 HTML，在工作的同时将看见颜色编码。 不用手动输入所有内容，我们可以使用 Visual Studio Code 的内置 Emmet 支持来完成很多繁琐的工作。

在空白编辑器窗口 `index.html` 中，键入 `!`（感叹号），然后选择 Tab 键。 这将告知 Emmet 使用如下所示的默认值填写制作网页所需的最小 HTML。

![HTML added by Emmet.](https://learn.microsoft.com/zh-cn/training/windows/develop-web-apps-with-vs-code/media/emmet-html.png)

我们在此处采用了直接的行来创建 HTML，跳过了 Emmet 的可选功能。 例如，在键入 Tab 键之前键入感叹号，将看见如下所示的内容。

![Emmet info option.](https://learn.microsoft.com/zh-cn/training/windows/develop-web-apps-with-vs-code/media/emmet-info.png)

请注意右侧蓝色圆圈中的小 `i`，可以单击以获取更多信息。 此外，请务必记下 [Visual Studio Code 中的 Emmet](https://code.visualstudio.com/docs/editor/emmet) 中完整 Emmet 引用的位置。 此时你不需要知道所有详细信息，但了解 Emmet 的范围及其提高效率的功能是有用的。

现在让我们回到正在编辑的新文件上。 请注意添加内容后 UI 所发生的变化。

![Unsaved file indicators.](https://learn.microsoft.com/zh-cn/training/windows/develop-web-apps-with-vs-code/media/unsaved-file-indicators.png)

活动栏中的“资源管理器”图标上有一个数字 1，这意味着其中有一个文件打开且已更改，但未保存。 之后是资源管理器中未保存的更改计数，显示在“打开编辑器”标头旁边。 最后，打开编辑器列表中的文件名以及文件自身的编辑器选项卡都有一个大圆点。

所有这些不同的指示器都提供通知未保存的更改，因此无论决定隐藏或显示哪些 UI 部分，都会知道尚未保存。

手动保存文件的方式和平时没有差别，可通过“文件”菜单或使用键盘快捷方式完成。 Visual Studio Code 还提供了便捷的自动文件保存功能，可从“文件”菜单启用该功能。 （或者按 F1，开始键入“自动保存”，然后选择“文件: 切换为自动保存）。

## 内置扩展中的语法突出显示

让我们看看内置扩展列表。 这些是 Visual Studio Code 中预安装的扩展，且不会显示在常用已安装扩展列表中。 若要查看内置扩展，请选择“筛选器扩展”区域中的省略号图标 (`...`)，然后选择“显示内置扩展”。 此列表可能相当长！ 请花费片刻时间来滚动查看各种项以了解此处的内容。

 备注

这里有适用于多种语言的语法突出显示扩展，例如内置的 HTML。 使用 Emmet 添加 HTML 时，你可能已经注意到上一节中的这个特定扩展。

## 使用工作区来组织你的项目

尽管没有要求，但如果需要一次处理多个文件，可以选择在工作区构造中进行工作。 这只是一个工作环境，其中包含所需的针对给定项目的所有文件和设置。 如果创建新的工作区，你将需要为其命名并将其保存到选择的位置。 此处我们将不会详细讨论工作区。 如果想要了解详细信息，请参阅 [Visual Studio Code 文档](https://code.visualstudio.com/docs)中的[多根工作区](https://code.visualstudio.com/docs/editor/multi-root-workspaces)。

---

## 下一单元: 构建和预览基本的 Web 应用

# 构建和预览基本的 Web 应用

**已完成**100 XP

* 5 分钟

在最后一个单元中，创建自动生成的简单 HTML 文件 index.html。 让我们从中断的地方开始，创建一个可以在本地服务器上运行的 Web 应用。

## 首次测试：Hello World

对于查看可运行的最小代码的第一次测试，我们将添加一些内容来展示。 当我们在最后一个单元中留下新的 index.html 文件时，它看起来如下所示。

![HTML added by Emmet.](https://learn.microsoft.com/zh-cn/training/windows/develop-web-apps-with-vs-code/media/emmet-html.png)

现在，编辑此代码使其类似于以下屏幕截图的内容（相关内容使用红色边框突出显示）。

![Default HTML plus some new content.](https://learn.microsoft.com/zh-cn/training/windows/develop-web-apps-with-vs-code/media/first-html.png)

请注意 HTML IntelliSense 和颜色编码扩展如何在整个过程中为你工作。 可以在以后的模块中深入探索这一点，但请随意继续进行实验。 如果这样做，请务必尝试自动完成功能。

## 本地发布网页

现在即可本地运行 HTML。 选择底部右侧状态栏中的“继续操作”图标。

![GoLive icon.](https://learn.microsoft.com/zh-cn/training/windows/develop-web-apps-with-vs-code/media/go-live-button.png)

这将告知之前已安装的 Live Server 扩展启动默认 Web 浏览器以服务当前文件中的内容。 应在浏览器的标题栏中看见“Hello World 测试页”，并看见以大标题字体显示的“Hello, World!”。

恭喜！ 你刚刚创建了你的第一个网页。 当然，这是只有你可以看见的内容，因为该页面是由本地运行 Web 服务器（Live Server 扩展）创建的。 你会注意到 Web 地址是为本地计算机保留的 IP 地址。 如果想要让此网页联机可用，需要将其部署到连接到 Internet 的 Web 服务器。 这超出了本次课程模块的范围，但你可以在其他模块中了解此系列。

# 总结

**已完成**100 XP

* 5 分钟

本模块介绍了以下内容：

* Visual Studio Code 的主要功能。
* 如何下载并安装 Visual Studio Code。
* 如何安装基本 Web 开发的扩展。
* 如何使用 Visual Studio Code 的基本编辑器功能。
* 如何编写并测试简单的 Web 应用。

本模块仅提供简介，但可以继续学习更多模块以深入了解更多功能。 有关 Visual Studio Code 功能的完整详细介绍，请参阅下面提供的链接。

## 其他信息

* [Visual Studio Code 文档](https://code.visualstudio.com/docs)
* [入门视频](https://code.visualstudio.com/docs/getstarted/introvideos)
* [Visual Studio Code 可实现此目标](https://vscodecandothat.com/)
