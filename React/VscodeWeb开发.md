1. [开始使用 Visual Studio Code 进行 Web 开发](https://learn.microsoft.com/zh-cn/training/modules/get-started-with-web-development/)

# 简介

现今通过网站所能实现的事情令人印象深刻。 可以生成在所有设备上运行的 Web 体验，包括各种媒体内容、执行复杂的计算，甚至创建类似于原生应用程序的应用。

如果对立即启动 Web 开发感兴趣，你可能会面临一系列令人眼花缭乱的选项。 本模块将展示网站的基本组件和一些可用于启动 Web 开发的工具。 你将结合使用 HTML、CSS 和 JavaScript 来生成网站。 你还将使用浏览器中的开发人员工具来了解当前发生的情况。

掌握这一基础知识后，你将有一个更好的背景，可用于将来在生成网站时做出决策。 例如，是否应选择 JavaScript 框架或通过创建自己的 JavaScript 函数来生成网站。

首先，让我们看一下想要达到哪种效果。

## 场景

假设你是一名 Web 开发人员，你的工作任务是让贵公司的网站吸引到范围更广泛的客户。 为了实现让客户自定义网站体验，你决定添加对浅色和深色主题的支持。 你将创建一个简单的概念证明网站来演示对使用 CSS 的主题的支持，并编写 JavaScript 函数在这些主题之间进行切换。

完成后，在选择深色主题时，网站就会如本例所示：

[![显示启用深色主题的完整网站的屏幕截图。](https://learn.microsoft.com/zh-cn/training/windows/get-started-with-web-development/media/themed-website.png)](https://learn.microsoft.com/zh-cn/training/windows/get-started-with-web-development/media/themed-website.png#lightbox)

## 网页中有哪些内容？

内容、样式和交互逻辑分别分为 HTML、CSS 和 JavaScript 文件。 新式编程中的设计原则是分离关注点。 有很多原因会导致分离关注点，其中两种是简单和重复使用。 例如，通过使用 CSS 设置 HTML 元素的样式，可以简化 HTML 代码。 无需对每个元素的外观进行编码，而是将 CSS 样式应用于页面上的所有元素，而不考虑页面的复杂性。 此外，还可以将多个 HTML 页面链接到单个 CSS 文件，这有助于简化整个网站的一致外观。

# 练习 - 设置 Web 应用的结构

创建和管理网站项目有各种方法。 根据你所拥有的特定工具以及组织偏好，会有所不同。 创建网站时，由于项目结构愈发复杂，项目结构随时间变化是常见现象。 关键在于保持组织相似，以下是可以帮助你执行此操作的常见策略。 大型项目通常需要更高程度的谨慎和专注，以便许多人能够理清所有内容。

在本单元中，你将使用 Visual Studio Code 创建一个简单的项目结构。 该项目将包含三个文件：一个 HTML 文件、一个 CSS 文件和一个 JavaScript 文件。 你还会添加一个 Visual Studio Code 扩展，以简化在浏览器中运行网站的工作。

## 为网站新建一个文件夹

1. 打开 Visual Studio Code。
   打开 Visual Studio Code 时，会打开“欢迎”页。 请注意，可以在“开始”列表中创建新文件或打开文件夹。
   [![Visual Studio Code 入门页的屏幕截图。](https://learn.microsoft.com/zh-cn/training/windows/get-started-with-web-development/media/vs-code-get-started.png)](https://learn.microsoft.com/zh-cn/training/windows/get-started-with-web-development/media/vs-code-get-started.png#lightbox)
   如果看不到“欢迎”页，可以通过在菜单上选择“帮助”>“欢迎”来显示它。 （或者，可以通过使用键盘快捷方式 Shift+Ctrl+P（在 Windows 计算机上）或 Shift+Cmd+P（在 macOS 上）打开“命令面板”或者通过从 Visual Studio Code 菜单中选择“查看”>“命令面板”来显示“欢迎”页面。当显示“命令面板”时，在搜索字段中输入“>帮助: 欢迎”打开“欢迎”页面。）
2. 在“欢迎”页的“开始”列表中选择“打开文件夹”，或者从 Visual Studio Code 菜单中选择“文件”>“打开文件夹”。
   [![Windows 操作系统文件夹打开对话框的屏幕截图。](https://learn.microsoft.com/zh-cn/training/windows/get-started-with-web-development/media/vs-code-open-folder.png)](https://learn.microsoft.com/zh-cn/training/windows/get-started-with-web-development/media/vs-code-open-folder.png#lightbox)
   打开文件夹时，操作系统会提供用于创建新文件夹的菜单选项。
3. 导航到要在其中为网站创建新文件夹的位置，然后选择“新建文件夹”。
4. 将文件夹命名为 simple-website，然后选择“选择文件夹”。
   重要

   如果出现“Visual Studio Code”对话框，请选择“信任父文件夹中所有文件的作者”；这是工作区信任功能，可让你决定项目文件夹是应允许还是限制自动执行代码。 你刚刚创建了文件夹，因此它是安全的。

## 创建一些文件

1. 创建新文件时，从菜单中选择“文件”>“新建文件”，或在 Windows 上使用 Control+N，或在 macOS 上使用 Command+N。
2. 在 Windows 上选择 Control+S，或在 macOS 上选择 Command+S 来保存文件。
3. 输入 `index.html` 作为文件名，然后选择“保存”。
4. 重复上述步骤，再创建两个文件，`main.css` 和 `app.js`。 完成后，在 Visual Studio Code 资源管理器中，会看到项目文件夹 simple-website 包含以下文件，它们构成网站：

   * index.html
   * main.css
   * app.js

   [![Visual Studio Code 资源管理器视图中文件的屏幕截图。](https://learn.microsoft.com/zh-cn/training/windows/get-started-with-web-development/media/vs-code-explorer-view.png)](https://learn.microsoft.com/zh-cn/training/windows/get-started-with-web-development/media/vs-code-explorer-view.png#lightbox)

生成网站时，可以在单个文件中包括所有 HTML、CSS 样式和 JavaScript 代码。 但是，在本练习中，你将使用 HTML 文件作为内容结构，使用 CSS 文件进行样式设置，并使用 JavaScript 文件实现交互性。

设置三个文件有助于组织网站项目。 将内容、样式和逻辑分开可以体现渐进式增强。 即使 JavaScript 未启用或不受客户支持，CSS 和 HTML 将仍旧有效。 但是，如果客户不支持 CSS，则至少会显示 HTML 内容。

### 安装扩展或包

可以使用扩展市场扩展 Visual Studio Code 的功能。 请注意，这些扩展是社区开发的资源，对于同一类型的功能，通常存在若干解决方案。 可以在编辑器中逐个安装扩展，也可以使用命令行同时安装多个扩展。

对于 Web 开发，你现在只需“pen-in-browser”。 此扩展可帮助你在默认浏览器中快速打开网站，而不是将文件 URL 复制并粘贴到浏览器中。

若要安装此扩展，请使用以下步骤：

1. 选择垂直“活动栏”（左窗格）上的“扩展”图标。
2. 在搜索框中输入“打开方式”，然后选择 TechER 发布的“在浏览器中打开”扩展。
3. 选择“安装”，Visual Studio Code 将安装扩展。
   [![显示 Visual Studio Code 扩展侧边栏的屏幕截图，搜索字段中有“打开位置”字样，下面是一列匹配的扩展。](https://learn.microsoft.com/zh-cn/training/windows/get-started-with-web-development/media/vs-code-get-extension.png)](https://learn.microsoft.com/zh-cn/training/windows/get-started-with-web-development/media/vs-code-get-extension.png#lightbox)
4. 单击“活动栏”中的顶部图标，或在 Windows 上使用 Control+Shift-E，或在 macOS 上使用 Command+Shift-E 切换回“资源管理器”。

我们继续！ 安装和设置需要一些额外的时间，但你只需安装和设置一次。 现在可以开始创建网站。

# 练习 - 将基本 HTML 添加到 Web 应用

目前，你的网站中有一个空的 HTML 文件。 接下来添加一些代码！ 目标是使用超文本标记语言 (HTML) 来描述客户的浏览器应显示的 Web 页面。 拥有一个初始模板不是很好吗？ 使用编辑器方便填写一些典型样板文件或 HTML 结构。

在本单元中，你将添加基本的 HTML 内容，在浏览器中打开 HTML 页面，并第一次看到开发人员工具。

## 添加一些 HTML 代码

Visual Studio Code 为即学即会的 HTML 编程提供基本支持。 其中包括语法突出显示、IntelliSense 的智能完成功能以及可自定义的格式设置。

1. 在 Visual Studio Code 中打开你的网站，然后在“资源管理器”中选择 `index.html` 文件来打开 `index.html` 文件。
2. 在 `index.html` 页中键入 `html:5`，然后选择 Enter。 HTML5 模板代码将添加到文件中。
   备注

   如果未将 HTML5 模板代码添加到 `index.html` 文件中，请尝试关闭并重新打开该文件。
3. 按如下所示修改代码。 在 Windows 上选择 Control+S，或在 macOS 上选择 Command+S 来保存文件。
   **HTML**复制

   ```
   <!DOCTYPE html>
   <html lang="en">
   <head>
     <meta charset="UTF-8">
     <meta http-equiv="X-UA-Compatible" content="IE=edge">
     <meta name="viewport" content="width=device-width, initial-scale=1.0">
     <title>Document</title>
   </head>
   <body>

   </body>
   </html>
   ```

HTML 有各种版本。 doctype `<!DOCTYPE html>` 指示此 HTML 文档包含 HTML5 代码。

虽然我们不打算深入探讨所有 HTML 元素的含义，但我们将指出一些重要的事项。 `meta` 标记表明通常不会对查看者可见的元数据信息，除非查看者查看浏览器中的源代码。 元元素或标记提供关于网页的描述性信息。 例如，它们可帮助搜索引擎处理网页中要在搜索结果中返回的信息。

UTF-8 字符集 (`charset`) 可能看似无关紧要，但对于确定计算机如何解释字符至关重要。 如果缺少字符集的元数据，可能会导致安全受到影响。 字符集属性背后有很多历史记录和技术信息，但本练习重要的一点是，VS Code 样板提供一些合理的默认值。

## 编辑标头

HTML 代码中的 `<head>` 元素包含浏览器标签页中不可见的网站相关信息。

元数据定义有关 HTML 文档的数据，例如字符集、脚本以及在其中打开网页的浏览器。

网页的标题显示在浏览器窗口的顶部，在某些方面具有重要意义。 例如，标题用于搜索引擎并在其中显示。 我们来添加标题。

 重要

从现在开始，省略号 (…) 表示之前声明的代码居前或居后。 应该提供足够的代码作为上下文，以便对工作进行必要的更改或更新，但不应将省略号复制并粘贴到代码中。

1. 在编辑器中，修改 `<title>` 元素，使其类似于以下示例。
   **HTML**复制

   ```
   ...
   <head>
     <meta charset="utf-8">
     <meta http-equiv="X-UA-Compatible" content="IE=edge">
     <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Simple website</title>
   ...
   ```

若要向网页上的 HTML 元素应用样式，可以直接在网页的标头中编写 CSS 代码。 在 HTML 页面中编写 CSS 称为“内部 CSS”。 但是，最好将 HTML 结构与 CSS 样式分离。 获得一个称为“外部 CSS”的单独 CSS 页面。 代码简洁且已划分时，往往更易于阅读。 可以使用一个或多个外部样式表为多个 Web 页面提供服务。 无需使用重复的 CSS 代码更新每个 HTML 页面，可以对单个 CSS 文件进行更改，并将这些更新应用到所有相关网页。 接下来链接到外部样式表。

1. 在“VS Code”编辑器中，在 `<title>` 元素后面添加一个空白行，键入 `link`，然后选择 Enter。 VS Code 应将以下行添加到 `index.html` 文件中。
   **HTML**复制

   ```
   <link rel="stylesheet" href="">
   ```

2. 将 `href=` 更新为 `href="main.css"`，并选择 Control+S (Windows) 或 Command+S (macOS) 保存文件。
   **HTML**复制

   ```
   ...
   <head>
     <meta charset="utf-8">
     <meta http-equiv="X-UA-Compatible" content="IE=edge">
     <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Task List</title>
     <link rel="stylesheet" href="main.css">
   </head>
   ...
   ```

## 编辑正文

接下来立即开始填写 `<body>` 元素。

`<body>` 元素包含你的客户在其浏览器中可见的网站内容。

1. 添加一个 *标题* `<h1>`元素，后跟一个 *段落* `<p>`元素，然后创建一个包含多个 *列表项* `<li>`元素的 *无序列表* `<ul>`。
2. 编辑代码或复制并粘贴，使其类似于以下示例。
   **HTML**复制

   ```
   <!DOCTYPE html>
   <html lang="en">
     <head>
       <meta charset="utf-8">
       <meta http-equiv="X-UA-Compatible" content="IE=edge">
       <meta name="viewport" content="width=device-width, initial-scale=1.0">
       <title>Simple website</title>
       <link rel="stylesheet" href="main.css">
     </head>
     <body>
       <h1>Task List</h1>
       <p id="msg">Current tasks:</p>
       <ul>
         <li class="list">Add visual styles</li>
         <li class="list">Add light and dark themes</li>
         <li>Enable switching the theme</li>
       </ul>
     </body>
   </html>
   ```

ID 属性（在 `<p>` 元素中使用）可用于样式化单个元素，而类属性（在 `<li>` 元素中使用）用于样式化同一类的所有元素。

在继续下一步之前，请确保选择 Control+S 或 Command+S 保存文件。

## 用浏览器打开

可以通过在浏览器中打开 HTML 文件在本地预览网页。 你的浏览器指向的不是以 `https://` 开头的网站地址，而是指向与 `C:/dev/simple-website/index.html` 类似的本地文件路径。

* 若要使用 Visual Studio Code 进行预览，请右键单击 `index.html` 并选择“使用默认浏览器打开”，或选择 `index.html` 文件并使用键盘快捷方式 Alt+B。
  [![Visual Studio Code 中的“在浏览器中打开”上下文菜单项的屏幕截图。](https://learn.microsoft.com/zh-cn/training/windows/get-started-with-web-development/media/vs-code-open-in-browser.png)](https://learn.microsoft.com/zh-cn/training/windows/get-started-with-web-development/media/vs-code-open-in-browser.png#lightbox)
  重要

  如果遇到问题，请确保直接右键单击文件名图标或文本。 如果出现“Visual Studio Code”对话框，请选择“是，我信任作者”；这是工作区信任功能，可让你决定项目文件夹是否应允许或限制自动执行代码。 你刚刚创建了文件，因此它是安全的。

  使用默认浏览器打开网页。

## 使用开发人员工具查看页面

可以通过使用浏览器中的开发人员工具检查网页。 一起来试一试。

1. 右键单击网页并选择“检查”以打开开发人员工具，或尝试以下快捷方式：

   * 按“开发人员工具”的键盘快捷方式 F12。
   * 在 Windows 和 Linux 上按 Ctrl+Shift+I，在 Mac 上按 Option+Command+I。

   这些键盘快捷方式适用于 Microsoft Edge、Chrome 和 Firefox。 如果你使用的是 Safari，请参阅 [Web 开发工具](https://developer.apple.com/safari/tools/)。 安装后，选择“Safari”>“偏好设置”，然后选择“高级”。 在窗格底部，选择“在菜单栏中显示开发菜单”复选框。 选择“开发”>“显示 Web 检查器”。 有关详细信息，请查看 Safari Web 检查器文档。
   要了解有关打开开发人员工具和主要可用功能的更多信息，请查看 [DevTools 工具概述](https://learn.microsoft.com/zh-cn/microsoft-edge/devtools-guide-chromium/overview)一文。
2. 选择“元素”选项卡。
   [![显示带有网站的浏览器窗口的屏幕截图，其中选择了“元素”选项卡旁边的开发人员工具。](https://learn.microsoft.com/zh-cn/training/windows/get-started-with-web-development/media/developer-tools-elements-tab.png)](https://learn.microsoft.com/zh-cn/training/windows/get-started-with-web-development/media/developer-tools-elements-tab.png#lightbox)
3. 将鼠标移到“元素”选项卡中显示的 HTML 元素上，然后展开各种元素的内容。

开发人员工具中的“元素”选项卡将显示在浏览器中呈现的文档对象模型 (DOM)。 调试时，查看浏览器如何解释你的源代码通常十分重要。

检查浏览器中的页面可提供各种有用信息，有助于排查问题。 还可以使用检查器查看 CSS 的详细信息，如下一节所示

# 练习 - 使用 CSS 设置 HTML 样式

使用级联样式表 (CSS) 可以指定页面外观。 基本思想就是定义在 HTML 页面中使用的元素的样式。 HTML 元素定义内容，而 CSS 样式定义此内容的样式。

例如，你可以应用圆角或为元素提供渐变背景。 或者，你可以使用 CSS 来指定超链接在你与它们交互时的样式和响应方式。 你还可以执行复杂的页面布局和动画效果。

你可以将样式应用于特定元素、特定类型的所有元素，或使用类来设置许多不同元素的样式。

在本练习中，你将对 HTML 页面元素应用 CSS 样式并添加一些 CSS 代码来定义你的浅色和深色主题。 你还将在浏览器的开发人员工具中检查结果。

## 外部 CSS

在关于 HTML 的上一个单元中，你已从 HTML 链接到外部 CSS 文件。

**HTML**复制

```
...
<head>
  <meta charset="utf-8">
  <meta http-equiv="X-UA-Compatible" content="IE=edge">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Task Timeline</title>
  <link rel="stylesheet" href="main.css">
...
```

外部 CSS 的一个优势就是多个 HTML 页面可以链接到同一 CSS 文件。 如果对 CSS 进行了更改，则每个页面的样式都将更新。 将 HTML 文件用于页面内容、将 CSS 文件用于样式设置、将 JavaScript 文件用于交互称为“关注点分离”。

如前所述，还可以直接在 HTML 中编写名为“内部 CSS”的 CSS。 即使是基础网站，也存在很多能够使 HTML 页面很快变得混乱的 CSS 规则。 如果是多个页面，通常会重复使用同一个 CSS 并且难以管理。

## CSS 规则

CSS 规则是你将样式应用于 HTML 元素的方式。 CSS 规则有一个选择器，用于表示应将样式应用于哪个或哪些元素。

在 Visual Studio Code 中，打开 `main.css` 文件并输入以下内容。

**css**复制

```
body {
    font-family: monospace;
}

ul {
    font-family: helvetica;
}
```

上面的代码片段包含两个规则。 每个规则都有：

* 一个选择器。 `body` 和 `ul` 是两个规则的选择器，用于选择样式应用于哪些元素。
* 左大括号 (`{`)。
* 一个样式声明列表，用于确定所选元素的样式。
* 右大括号 (`}`)。

例如，`ul` 选择器选择页面中的 `<ul>` HTML 元素，以对其应用样式。 声明为 `font-family: helvetica` 并确定样式应该是什么。 “属性名称”为 `font-family`，“值”为 `helvetica`。

接下来你将注意到，你可以为元素自定义名称。

## 选择器

ID 和类选择器使你能够将样式应用于 HTML 中的自定义属性名称。 ID 用于设置一个元素的样式，而类可用于设置多个元素的样式。

1. 将以下代码复制到 CSS 文件中，放在你先前添加的 `ul` 选择器的右大括号后面。
   **css**复制

   ```
   li {
     list-style: circle;
   }

   .list {
     list-style: square;
   }

   #msg {
     font-family: monospace;
   }
   ```

   前面的代码包含三个 CSS 规则，最后两个规则使用自定义属性来选择元素：`.list` 和 `#msg`。

   * `.list` 是一个类选择器。 每个包含设置为 `list` 的 `class` 属性的 HTML 元素都将获得在此选择器中定义的样式。
   * `#msg` 是一个 ID 选择器。 将其 `id` 属性设置为 `msg` 的 HTML 元素将获得在此选择器中定义的样式。

   用于选择器的名称可以是任意的，只要与 HTML 中的已定义名称匹配即可。
2. 在 Windows 上选择 Control+S，或在 macOS 上选择 Command+S 来保存工作。

## 在浏览器中查看

1. 若要使用 VS Code 进行预览，请右键单击文件名 `index.html`，然后选择“使用默认浏览器打开”。
   重要

   即使只是在编辑 `main.css` 文件，若要预览更改，你也应选择 `index.html` 文件。

   使用默认浏览器打开网页。
   [![应用了字体样式的网站屏幕截图。](https://learn.microsoft.com/zh-cn/training/windows/get-started-with-web-development/media/applied-font-styles.png)](https://learn.microsoft.com/zh-cn/training/windows/get-started-with-web-development/media/applied-font-styles.png#lightbox)

字体样式是你所希望看到的类型吗？ 有趣的是，应用于 `<body>` 的样式是如何在 `<h1>` 元素上继承的。 我们没有为 `<h1>` 定义任何内容，但它仍然获得了在 `<body>` 上定义的字体。 这种从父元素到子元素的继承机制是 CSS 的关键方面之一。 但是，`<li>` 元素具有不同的字体，会覆盖 `<body>` 上的字体集，因为它们也是你为其定义样式的 `<ul>` 元素的子元素。

请注意，使用 VS Code 中的“在默认浏览器中打开”，每次都会在浏览器中打开一个新标签页。 要避免打开新标签页，可以重新加载已包含网站的标签页。

要重新加载标签页，请按 F5，这是刷新键盘快捷方式，或者在 Windows 或 Linux 上按 Ctrl+R，在 Mac 上按 Command+R。

## 添加浅色主题

接下来，将为你的网站添加对颜色主题的支持。 首先使用十六进制颜色代码定义浅色主题。

1. 在 CSS 文件中，将下面的代码添加到文件末尾。
   **css**复制

   ```
   .light-theme {
     color: #000000;
     background: #00FF00;
   }
   ```

   在本示例中，`#000000` 指定字体颜色为黑色，`#00FF00` 指定背景色为绿色。
2. 在 HTML 文件中，更新类名为 `light-theme` 的 `<body>` 元素，以使浅色主题的类选择器正确应用样式。
   **HTML**复制

   ```
   <body class="light-theme">
   ```

## 在浏览器中查看

* 要使用 Visual Studio Code 进行预览，请右键单击 `index.html`，然后选择“在默认浏览器中打开”或按 F5 重新加载上一个标签页。
  请注意，会出现使用绿色背景的浅色主题。
  [![应用了浅色主题的网站截图。](https://learn.microsoft.com/zh-cn/training/windows/get-started-with-web-development/media/light-theme.png)](https://learn.microsoft.com/zh-cn/training/windows/get-started-with-web-development/media/light-theme.png#lightbox)

## 查看应用的 CSS

1. 在浏览器视图中，打开“开发人员工具”。
   右键单击页面并选择“检查”，或者选择快捷方式 F12 或 Ctrl+Shift+I。
2. 选择“元素”选项卡，然后在“元素”选项卡中选择“样式”选项卡（默认应该已经选中）。
3. 将鼠标悬停在各种 HTML 元素上，当你选择一些元素时，请注意开发人员工具如何在“样式”中显示应用到它们的样式。
4. 选择 `<body>` 元素。 请注意应用的 `light-theme`。
5. 选择无序列表 `<ul>` 元素。 请注意 `font-family: helvetica;` 的自定义样式，该样式将覆盖 `<body>` 元素的样式。

[![应用了浅色主题的网站屏幕截图，旁边的开发人员工具显示带有 HTML 和 CSS 代码的元素面板。](https://learn.microsoft.com/zh-cn/training/windows/get-started-with-web-development/media/light-theme-in-dev-tools.png)](https://learn.microsoft.com/zh-cn/training/windows/get-started-with-web-development/media/light-theme-in-dev-tools.png#lightbox)

要了解有关在开发人员工具中查看 CSS 样式的更多信息，请查看[开始查看和更改 CSS](https://learn.microsoft.com/zh-cn/microsoft-edge/devtools-guide-chromium/css/) 一文。

## 添加深色主题

对于深色主题，需要设置基础结构以为下一个单元做好准备，在该单元中，将在网页上启用主题切换。

若要向 CSS 添加对深色主题的支持，请使用以下步骤。

1. 向 CSS 文件顶部的页根添加一些常量。
   **css**复制

   ```
   :root {
     --green: #00FF00;
     --white: #FFFFFF;
     --black: #000000;
   }
   ```

   `:root` 选择器表示 HTML 页面中的 `<html>` 元素。 对于此类任务，最佳做法是使用 `:root` 选择器在 CSS 规则中定义一组全局 CSS 变量。 在本例中，你定义了三个颜色变量。 接下来，你将能够在其他 CSS 规则中使用这些变量。
2. 在 CSS 文件的末尾，将 `light-theme` 规则替换为以下代码，以更新它并添加 `dark-theme` 选择器。
   **css**复制

   ```
   .light-theme {
     --bg: var(--green);
     --fontColor: var(--black);
   }
   .dark-theme {
     --bg: var(--black);
     --fontColor: var(--green);
   }
   ```

   在上面的代码中，你定义了 `bg` 和 `fontColor` 这两个新变量，它们指定背景和字体颜色。 这些变量使用 `var` 关键字将其属性值设置为之前在 `:root` 选择器中指定的变量。
3. 接下来，在 CSS 文件中，将当前的 `body` 选择器替换为以下代码。
   **css**复制

   ```
   body {
     background: var(--bg);
     color: var(--fontColor);
     font-family: helvetica;
   }
   ```

   在此示例中，你使用 `body` 选择器来设置 `background` 和 `color` 属性，并且由于网页上可见的元素都在 `<body>` 元素内，它们将继承 `<body>` 上设置的颜色。
4. 在 CSS 文件中，使用 `#msg` 和 `ul` 选择器删除规则，让它们也从 `<body>` 继承相同的字体。
5. 要查看深色主题，请打开文件 `index.html`，并手动将 `<body>` 类属性中的默认主题编辑为深色主题 (`dark-theme`)，然后在浏览器中重新加载页面。
   [![应用了深色主题的网站的屏幕截图以及旁边的开发人员工具。](https://learn.microsoft.com/zh-cn/training/windows/get-started-with-web-development/media/dark-theme.png)](https://learn.microsoft.com/zh-cn/training/windows/get-started-with-web-development/media/dark-theme.png#lightbox)
6. 编辑 `<body>` 类属性以将默认值切换回浅色主题。

在下一个单元中，你将使用 JavaScript 来提供交互性，并支持切换主题。

# 练习 - 使用 Javascript 添加交互性

**已完成**100 XP

* 10 分钟

JavaScript（或 ECMAScript）是有助于向网页添加交互性的编程语言。

例如，你可以使用 JavaScript 来定义用户选择按钮时将发生的行为；例如，打开一个弹出窗口。 使用 JavaScript，无需重载即可从网页添加或删除内容。

在本单元中，你将为网页设置一个示例 JavaScript 文件。 你将创建一个按钮来在浅色和深色主题之间切换。 然后将按钮附加到执行实际主题切换的 JavaScript 代码。 最后，你将使用浏览器的开发人员工具检查完成的项目。

## 链接到 JavaScript

与 CSS 一样，你可以将 JavaScript 直接添加到 HTML 文件中，但推荐的最佳做法是将 JavaScript 保存在单独的文件中。 将 JavaScript 代码添加到单独的文件中可以更轻松地在多个网页中重复使用它。 例如，可以通过在网页正文中的任意位置添加 `<script>alert('Hello World')</script>` 来创建弹出警报；但是，最好将 JavaScript 代码添加到一个单独的文件中，方便链接到每个需要自定义功能的文件。

使用 HTML 脚本标记 `<script>` 可以链接到外部 JavaScript 文件，这是本练习中配置 Web 应用的方法。

1. 在 VS Code 中，打开 `index.html` 文件。
2. 在 `</body>` 结束元素之前的新行中输入 `script:src`，然后选择 Enter。 脚本的开始标记和结束标记将被添加到代码中。
3. 修改 `<script>` 元素以加载 `app.js` 文件（如以下示例所示），并确保它位于列表的 `</ul>` 结束元素之后。
   **HTML**复制

   ```
   ...
   <ul>
     <li class="list">Add visual styles</li>
     <li class="list">Add light and dark themes</li>
     <li>Enable switching the theme</li>
   </ul>
   <script src="app.js"></script>
   ...
   ```

`<script>` 元素可以放在 `<head>` 中或 `<body>` 中的其他位置。 但是，通过将 `<script>` 元素放在 `<body>` 部分的末尾，可以先在屏幕上显示所有页面内容，然后再加载脚本。

## 添加容错功能

1. 在 HTML 文件中的 `</script>` 结束标记之后添加 `<noscript>` 元素，该元素可用于在停用 JavaScript 时显示消息。
   **HTML**复制

   ```
   <script src="app.js"></script>
   <noscript>You need to enable JavaScript to view the full site.</noscript>
   ```

   添加 `<noscript>` 元素是容错或故障弱化的一个示例。 通过使用 `<noscript>` 元素，代码可以检测并规划功能何时不受支持或不可用。
2. 使用键盘快捷方式 Control+S (Windows) 或 Command+S (macOS) 保存更改。

## 设置严格模式

JavaScript 旨在简化学习，它允许开发人员犯一些错误。 例如，使用拼写错误的变量时，JavaScript 不会引发错误，而是创建新的全局变量。 当你开始学习 JavaScript 时，虽然错误更少这一点很吸引人，但它可能会导致编写的代码更难让浏览器优化，也更难调试。

切换到严格模式，在出错时获得更有用的错误。

* 在 VS Code 中，打开 `app.js` 文件并输入以下内容。
  **JavaScript**复制

  ```
  'use strict';
  ```

## 添加按钮

你需要通过一种方式让用户在你的网页中的浅色和深色主题之间切换。 在本练习中，你将使用 HTML `<button>` 元素实现该功能。

1. 在 HTML 文件中，添加一个 `<button>` 元素。 将按钮置于 `<div>` 元素内的列表的末尾。
   **HTML**复制

   ```
   ...
   <ul>
     <li class="list">Add visual styles</li>
     <li class="list">Add light and dark themes</li>
     <li>Enable switching the theme</li>
   </ul>
   <div>
     <button class="btn">Dark</button>
   </div>
   <script src="app.js"></script>
   ...
   ```

   请注意，本示例中的 `<button>` 元素具有你将用于应用 CSS 样式的类属性。
2. 在 CSS 文件中，为 HTML 按钮添加一个带有 `.btn` 类选择器的新规则。 要使按钮颜色不同于一般的浅色或深色主题颜色，请在此规则中设置 `color` 和 `background-color` 属性。 它们将替代 CSS 文件的 `body` 规则中设置的默认设置。
   **css**复制

   ```
   .btn {
     color: var(--btnFontColor);
     background-color: var(--btnBg);
   }
   ```

3. 接下来，修改 `.btn` 规则，为按钮的大小、形状、外观和位置添加一些样式。 以下 CSS 在页面标题的右侧创建一个圆形按钮。
   **css**复制

   ```
   .btn {
     position: absolute;
     top: 20px;
     left: 250px;
     height: 50px;
     width: 50px;
     border-radius: 50%;
     border: none;
     color: var(--btnFontColor);
     background-color: var(--btnBg);
   }
   ```

4. 接下来，更新浅色和深色主题的 CSS。 定义一些新的变量，`--btnBg` 和 `--btnFontColor`，以指定特定于按钮的背景色和字体颜色。
   **css**复制

   ```
   .light-theme {
     --bg: var(--green);
     --fontColor: var(--black);
     --btnBg: var(--black);
     --btnFontColor: var(--white);
   }

   .dark-theme {
     --bg: var(--black);
     --fontColor: var(--green);
     --btnBg: var(--white);
     --btnFontColor: var(--black);
   }
   ```

## 添加事件处理程序

若要在选择按钮时执行某些操作，需要在 JavaScript 文件中提供一个事件处理程序。 事件处理程序是一种在页面上发生事件时运行 JavaScript 函数的方法。 对于按钮，让我们为 `click` 事件添加一个事件处理程序；事件处理程序函数在 `click` 事件发生时运行。

添加事件处理程序之前，需要对按钮元素的引用。

1. 在 JavaScript 文件中，使用 `document.querySelector` 获取按钮引用。
   **JavaScript**复制

   ```
   const switcher = document.querySelector('.btn');
   ```

   `document.querySelector` 函数使用你在 CSS 文件中使用的相同 CSS 选择器。 `switcher` 现在是对页面中按钮的引用。
2. 接下来，为 `click` 事件添加事件处理程序。 在以下代码中，你将为 `click` 事件添加一个侦听器，并定义一个事件处理程序函数，以便在 `click` 事件发生时由浏览器执行。
   **JavaScript**复制

   ```
   switcher.addEventListener('click', function() {
       document.body.classList.toggle('light-theme');
       document.body.classList.toggle('dark-theme');
   });
   ```

在上述代码中，你使用 `toggle` 方法修改了 `<body>` 元素的类属性。 此方法会自动添加或删除 `light-theme` 和 `dark-theme` 类。 此代码在单击时应用深色样式而不是浅色样式，如果再次单击，则应用浅色样式而不是深色样式。

但是，还需要更新按钮的标签以显示正确的主题，因此需要添加一个 `if` 语句来确定当前主题并更新按钮标签。

完整的 JavaScript 代码应如下所示。

**JavaScript**复制

```
'use strict';

const switcher = document.querySelector('.btn');

switcher.addEventListener('click', function() {
    document.body.classList.toggle('light-theme');
    document.body.classList.toggle('dark-theme');

    const className = document.body.className;
    if(className == "light-theme") {
        this.textContent = "Dark";
    } else {
        this.textContent = "Light";
    }
});
```

对于包含多个单词的变量名，JavaScript 通常使用驼峰式大小写，例如，变量 `className`。

## 控制台消息

作为 Web 开发人员，你可以创建不会显示在网页上的隐藏消息，但你可以在开发人员工具的“控制台”选项卡中阅读这些消息。使用控制台消息有助于查看代码的结果。

* 在 `if` 语句之后但在事件侦听器内添加对 `console.log` 的调用。
  **JavaScript**复制

  ```
  switcher.addEventListener('click', function() {
      document.body.classList.toggle('light-theme');
      document.body.classList.toggle('dark-theme');

      const className = document.body.className;
      if(className == "light-theme") {
          this.textContent = "Dark";
      } else {
          this.textContent = "Light";
      }

      console.log('current class name: ' + className);
  });
  ```

如果位于 JavaScript 文件中，可以在 VS Code 中通过输入 `log`，然后按 Enter 来为 `console.log` 使用自动完成功能。

可以在文本中用单引号或双引号定义文本字符串。

## 在浏览器中打开

1. 要预览，请选择 `index.html`，然后选择“在默认浏览器中打开”，或按 F5 重新加载同一浏览器标签页。
   [![显示“新建”按钮的网站的屏幕截图。](https://learn.microsoft.com/zh-cn/training/windows/get-started-with-web-development/media/light-theme-with-button.png)](https://learn.microsoft.com/zh-cn/training/windows/get-started-with-web-development/media/light-theme-with-button.png#lightbox)
2. 选择新的“深色”按钮可切换为深色主题。
   [![切换为深色主题后的网站的屏幕截图。](https://learn.microsoft.com/zh-cn/training/windows/get-started-with-web-development/media/dark-theme-with-button.png)](https://learn.microsoft.com/zh-cn/training/windows/get-started-with-web-development/media/dark-theme-with-button.png#lightbox)
3. 确保一切看起来正确且按预期方式运行。 否则，应查看前面的步骤，确定是否遗漏了某些内容

## 检查开发人员工具中的页面

1. 打开开发人员工具。
   * 右键单击并选择“检查”，或使用键盘快捷方式 F12。 或者，在 Windows 或 Linux 上使用 Ctrl+Shift+I 快捷方式，在 macOS 上使用 Option+Command+I。
2. 选择“元素”选项卡，然后在“元素”选项卡内选择“样式”选项卡。
3. 选择 `<body>` 元素。 在“样式”选项卡中，查看应用的主题。 如果当前主题为深色，则应用 `dark-theme` 样式。
   请确保选中深色主题。
4. 选择“控制台”选项卡以查看 `console.log` 消息：`current class name: dark-theme`。

[![网站和开发人员工具控制台打开的浏览器窗口的屏幕截图，其中显示控制台消息。](https://learn.microsoft.com/zh-cn/training/windows/get-started-with-web-development/media/console-output.png)](https://learn.microsoft.com/zh-cn/training/windows/get-started-with-web-development/media/console-output.png#lightbox)

使用控制台，可以从 JavaScript 代码中获取有趣的见解。 添加更多控制台消息，以了解代码的哪些部分正在执行并了解其他变量的当前值。

要了解有关控制台的更多信息，请查看[控制台概述](https://learn.microsoft.com/zh-cn/microsoft-edge/devtools-guide-chromium/console/)一文。

## 知识检查

**1.** HTML 的主要用途是什么？

[ ] HTML 用于提供网页结构。

正确！ HTML 提供网页的结构性构建基块。

[ ] HTML 用于设置网页样式。

[ ] 用户交互或事件。

***2.** 以下哪个选项是将代码放入不同文件的设计原则？*

[ ] 渐进式增强。

不正确。 渐进式增强是指从基本内容开始，如果支持再添加更多功能。

[ ] 分离关注点。

正确！ 整理文件，以便每个文件或节都能处理单独的关注点。

[ ] 故障弱化。

**3.** 在 HTML 和 CSS 中，`#msg` 和 `.list` 是哪种类型实体的示例？

[ ] 元素。

[ ] 键值对。

[ ] 选择器。

正确！ `#msg` 是 ID 选择器，`.list` 是类选择器。

**4.** 在 Web 开发环境中，控制台有什么作用？

[ ] 用于在远程用户的计算机上打开命令 shell。

[ ] 用于将调试消息发送到 Web 浏览器。

正确！ 开发人员可以使用控制台将消息发送到浏览器开发人员工具。

[ ] 用作预览 Web 内容的插件。

# 总结

**已完成**100 XP

* 2 分钟

在本模块中，你为 Web 开发设置了工作环境。 还创建了网站，并测试了用于 Web 浏览器的所有功能。 让我们来看看你已经完成的内容：

* 下载并安装了 Web 开发所需工具，使用基本包自定义了编辑器。
* 创建了项目目录和用于构建网站的文件。
* 创建了标题和其他页面元素，然后链接到了外部文件并在浏览器中测试了页面。
* 为不同元素应用了样式，在浏览器中测试了网站，并添加了对使用 CSS 的主题的支持。
* 添加了 JavaScript，以启用与页面的自定义交互并在主题之间切换。
* 你了解了如何创建和使用控制台消息在代码中进行速览。

你作为 Web 开发人员正在收集工具和构建基础。 你可以将网站重用作未来项目的模板。 随着技能和知识的增长，你将更具实现网站愿景的能力。 同时也为想法变成现实提供了可能性。

## 了解详细信息

### Web 开发概念

* [容错（故障弱化）](https://wikipedia.org/wiki/Fault_tolerance)
* [Separation of concerns](https://wikipedia.org/wiki/Separation_of_concerns)（分离关注点）
* [Progressive enhancement](https://wikipedia.org/wiki/Progressive_enhancement)（渐进式增强）

### Web 开发参考

#### HTML5

* [W3C - HTML 历史记录](https://www.w3.org/TR/html52/introduction.html#introduction-history)
* [Webhint - 使用字符集“Utf-8”](https://webhint.io/docs/user-guide/hints/hint-meta-charset-utf-8/)
* [MDN Web 文档 - 标头中有什么？](https://developer.mozilla.org/docs/Learn/HTML/Introduction_to_HTML/The_head_metadata_in_HTML)
* [MDN Web 文档 - HTML 元素参考](https://developer.mozilla.org/docs/Web/HTML/Element)

#### CSS

* [MDN Web 文档 - CSS：级联样式表](https://developer.mozilla.org/docs/Web/CSS)

#### JavaScript

* [MDN Web 文档 - 严格模式](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Strict_mode)
* [MDN Web 文档 - JavaScript 参考](https://developer.mozilla.org/docs/Web/JavaScript/Reference)

### Web 开发技术

#### Microsoft Edge 文档

* [Microsoft Edge Developer Tools](https://learn.microsoft.com/zh-cn/microsoft-edge/devtools-guide-chromium/landing/)（Microsoft Edge 开发人员工具）
* [使用“元素”工具检查、编辑和调试 HTML 和 CSS](https://learn.microsoft.com/zh-cn/microsoft-edge/devtools-guide-chromium/elements-tool/elements-tool)
* [控制台概述](https://learn.microsoft.com/zh-cn/microsoft-edge/devtools-guide-chromium/console/)

#### Azure 静态 Web 应用

部署网站的一种方法是使用 Azure Static Web Apps。

* [Azure Static Web Apps 的学习路径](https://learn.microsoft.com/zh-cn/training/paths/azure-static-web-apps/)
* [Azure Static Web Apps 文档](https://learn.microsoft.com/zh-cn/azure/static-web-apps)

#### Visual Studio Code 文档

* [User interface](https://code.visualstudio.com/docs/getstarted/userinterface)（用户界面）
* [Emmet in Visual Studio Code](https://code.visualstudio.com/docs/editor/emmet)（Visual Studio Code 中的 Emmet）
