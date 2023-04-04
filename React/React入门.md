# React 简介

React 是一种开源框架，用于创建用户界面。 它最常用于创建 Web 应用程序。 不过，我们可以通过 React Native 使用 React 生成移动或桌面应用程序。 React 主要处理[模型-视图-控制器](https://en.wikipedia.org/wiki/Model%E2%80%93view%E2%80%93controller)中的“视图”部分。 因此，你可以对路由、管理状态以及访问 API 使用其他库。

此模块介绍 React 的核心概念。 它引入了 JavaScript XML (JSX)、组件和显示数据。

## 模块目标

* 了解 React 的核心概念
* 生成 React 应用程序
* 创建组件

## Project

在此模块中，我们将创建一个 React 初学者项目。 我们将介绍 JSX 和使用 Web 捆绑程序的必要性。 我们会创建第一个组件，并介绍项目结构。

## 先决条件

若要完成此模块，需要了解以下内容：

* HTML、CSS 和 JavaScript 的免费 Web 框架。
* Node.js 和 npm 中的包管理功能。
* Git。

确保已在本地计算机上安装以下软件：

* [Node.js](https://nodejs.org/)
* 代码编辑器，如 [Visual Studio Code](https://code.visualstudio.com/)
* [Git](https://git-scm.com/)

# JSX 简介

React 使用一种名为 JavaScript XML (JSX) 的特殊语法。 借助 JSX，你可将 HTML（或可能会创建的自定义组件）和 JavaScript 集成到一个文件中，甚至可以集成到单个代码行中。 通过使用 JSX，你可以依赖 JavaScript 语法来实现逻辑。 Visual Studio Code 为 JSX 文件提供 IntelliSense 功能，使用 React 时此工具会非常有用。

 备注

JSX 依赖于可扩展标记语言 (XML)。 XML 的语法类似于 HTML。 许多情况下，你可能都不会注意到二者之间的差异。 但是，XML 对语法有几点重要的限制：

* 所有元素都必须放置在一个父元素内。
* 必须结束所有元素。

## 生成过程

浏览器本机不支持 JSX。 因此，必须从 JSX 文件生成 JavaScript 和 HTML，才能由浏览器呈现它们。 有几种捆绑程序和其他工具可以执行所需完成的任务。 这些工具包括 [Webpack](https://webpack.js.org/)、[](https://parceljs.org/) 和 [](https://www.snowpack.dev/)。 我们将使用 Snowpack，因为它不需要代码，也不需要额外编写脚本。

## 组件

React 开发基于组件完成。 组件是自包含显示和工作单元。 它们可在应用程序中重复使用。 你可使用它们将应用程序按逻辑分解为更小的区块（或组件）。

# 创建初学者项目

我们将使用初学者项目，这样就可以快速开始编写代码。 初学者项目包含开始使用 Snowpack 开发 React 应用程序所需的最小结构：

* 两个文件
* 两个空目录

## 克隆存储库并安装包

1. 打开终端或命令窗口，并运行以下命令：
   **Bash**复制

   ```
   # Linux or macOS
   git clone https://github.com/MicrosoftDocs/mslearn-react
   cd mslearn-react/code/0-starter

   # Windows
   git clone https://github.com/MicrosoftDocs/mslearn-react
   cd mslearn-react/code/0-starter
   ```

2. 在同一个终端或命令窗口中使用以下命令，以安装所需的包：
   **Bash**复制

   ```
   npm install
   ```

3. 通过运行以下命令在 Visual Studio Code 中打开目录：
   **Bash**复制

   ```
   code .
   ```

## 浏览初学者项目

我们来浏览一下初学者项目中的文件夹和文件：

* package.json 包含包和脚本的列表：
  * 包：
    * React 包表示 React
    * ReactDOM 包用于将应用程序载入浏览器
  * 脚本：
    * dev 用于从 Snowpack 运行开发服务器：
      * 它几乎会生成所有 JavaScript 和 HTML 文件。
      * 当文件更改时，它将承载并自动重启服务器。
    * build 用于生成部署所需的生产文件
* snowpack.config.js 包含 Snowpack 的核心配置。
  * mount 将为 Snowpack 服务器创建两个虚拟目录。
    * public 包含所有静态文件（HTML、CSS 和图像等）。 它托管为 `/`。
    * src 包含所有 JSX 文件和关联的 React 文件。 它托管为 `dist`。
* public 包含所有静态文件。
* src 包含所有 React 文件。

---

# Hello, world

启动任何编程课程的最常见方式是显示文本“Hello，world！”，按照此传统，接下来我们将使用 React 显示这句著名的文本。

我们将创建两个项目，作为项目的基础：

* index.html 文件用于托管 React 应用程序。
* index.jsx 文件载入应用程序。

## 创建应用程序主机

1. 在 Visual Studio Code 中，从 public 文件夹新建一个文件。 将其命名为 index.html。
2. 添加以下 HTML：
   **HTML**复制

   ```
   <!DOCTYPE html>
   <html lang="en">
   <head>
       <title>Recipes</title>
   </head>
   <body>
       <div id="app"></div>
       <script type="module" src="/dist/index.js"></script>
   </body>
   </html>
   ```

### 浏览代码

请注意 HTML 中非常重要的两行：

* `<div id="app"></div>`
  * 此行创建用于托管 React 应用程序的 HTML 元素。
  * 我们通过该元素的 ID 调用它，来呈现应用程序。
* `<script type="module" src="/dist/index.js"></script>`
  * 此行用于加载 JavaScript。

 备注

要导入的文件的名称是 index.js。 我们不使用 index.jsx，因为浏览器无法呈现 JSX 文件。 我们始终需要使用捆绑程序（如 Snowpack）来生成 JavaScript。 我们要引用 JavaScript，而非 JSX。

通过 `type="module"` 属性，我们可以在 JavaScript（或 JSX）中使用 `import` 语句。 对于浏览器而言，此功能相对较新。 它可帮助我们导入必要的包和组件。

## 创建 React 应用程序的入口点

我们需要使用代码，以便在 HTML 内呈现 React 应用程序。 通常，我们使用 index.jsx 文件呈现此应用程序。

1. 在 src 文件夹中创建一个新文件。 将其命名 index.jsx。
2. 添加以下代码：
   **jsx**复制

   ```
   import React from 'react';
   import ReactDOM from 'react-dom';

   ReactDOM.render(
       <h1>Hello, world!</h1>,
       document.getElementById('app')
   );
   ```

### 浏览代码

index.jsx 文件启动时会导入两个重要的库。 第一个库是 `React`，它可允许我们使用 JSX。 我们创建的每个组件或 JSX 文件都会导入它。 第二个库是 `ReactDOM`，它将在 HTML 中呈现应用程序。

`render` 采用两个参数：

* 要显示的 HTML。 在本示例中，HTML 为 `h1` 标题。
* 要用于显示 HTML 的 HTML 元素。 我们将使用 ID 为 `app` 的元素。 在此之前，我们已创建此元素。

能够在 JavaScript 编码中使用 HTML，这是 JSX 的功能之一。

## 查看页面

我们已生成代码，现在我们来看看网站的实际运行状况！

1. 选择“视图”>“终端”，或选择 Ctrl+`，从 Visual Studio Code 中打开集成终端。 在 Mac 上，改为选择 Cmd+`。
2. 使用以下命令启动 Snowpack 的开发服务器：
   **Bash**复制

   ```
   npm start
   ```

默认浏览器应自动打开并显示你的页面。 如果此页面未自动显示，请打开浏览器并转到 [http://localhost:8080](http://localhost:8080).。 现在你应该看到了你的页面！

![显示“Hello, world!”页面的屏幕截图。](https://learn.microsoft.com/zh-cn/training/modules/react-get-started/media/hello.png)

### 浏览生成的代码

我们的 JSX 代码将转换为相应的 HTML 和 JavaScript，以便显示在浏览器中。 打开 Snowpack 生成的 JavaScript 文件：[http://localhost:8080/dist/index.js.。](http://localhost:8080/dist/index.js.%E3%80%82) 你将看到以下代码：

**JavaScript**复制

```
import React from "../web_modules/react.js";
import ReactDOM from "../web_modules/react-dom.js";
ReactDOM.render(/* @__PURE__ */ React.createElement("h1", null, "Hello, world!"), document.getElementById("app"));
```

将焦点置于生成 `h1` 元素的代码行，并在其中放置文本：

**JavaScript**复制

```
React.createElement("h1", null, "Hello, world!")
```

使用此代码类似于通过 Vanilla JavaScript 使用 `document.createElement`。 借助 Snowpack 和其他捆绑程序提供的工具，我们能够使用 JSX 自动生成适当的对浏览器友好的代码。

# 显示动态数据

借助组件，可将一个应用程序分解为多个逻辑片段。 在本单元中，我们将为食谱标题生成一个组件，以便了解此功能。 我们将生成组件，并将其导入 `App`。 我们还将探讨如何动态显示数据。

## 显示动态数据

若要在组件中显示动态数据，请使用语法 `{ }`，有时人们称之为 handlebar。 此类语法相对较常见于 HTML 模板化工具。 使用这些 handlebar 时，可有效切换到 JavaScript 模式，并可运行几乎所有有效的 JavaScript。

例如，若要显示当前时间，可以使用以下代码：

**JavaScript**复制

```
<div>{ Date.now() }</div>
```

## 创建 RecipeTitle 组件

在本示例中，我们将为食谱标题创建一个组件。 我们要将一个 JavaScript 变量用于标题，以演示 React 如何显示动态数据。 我们会在未来的单元中介绍如何使用更复杂的数据。

1. 在 src 文件夹中创建一个新文件。 将其命名为 RecipeTitle.jsx。
2. 将以下代码添加到 RecipeTitle.jsx：
   **jsx**复制

   ```
   import React from 'react';

   function RecipeTitle() {
       const title = 'Mashed potatoes';
       return (
           <h2>{ title }</h2>
       )
   };
   export default RecipeTitle;
   ```

### 浏览代码

请注意，我们创建了一个名为 `title` 的常量。 然后，我们使用 handlebar 语法 `{ }`，来告知 React 我们要在 `<h2>` 元素内显示 `title` 的值。 借助 JSX 的此功能，我们能够将 JavaScript 和 HTML 混合在一起。

## 使用 RecipeTitle 组件

让我们将 `RecipeTitle` 添加到 `App`，以便在应用程序中显示它。

1. 打开 src/App.jsx。
2. 在内容为 `import React from 'react';` 的行（应是第 2 行）下面，添加以下代码：
   **JavaScript**复制

   ```
   import RecipeTitle from './RecipeTitle'
   ```

3. 在内容为 `<h1>Recipe Manager</h1>` 的语法下面添加以下代码，以将 `RecipeTitle` 用作一个 HTML 元素：
   **jsx**复制

   ```
   <RecipeTitle />
   ```

### 浏览代码

现在，src/App.jsx 文件的完整内容如下所示：

**jsx**复制

```
import React from 'react';
import RecipeTitle from './RecipeTitle'

function App() {
    return (
        <article>
            <h1>Recipe Manager</h1>
            <RecipeTitle />
        </article>
    )
}

export default App;
```

我们像使用 HTML 一样使用了 `<App />`，我们也可以通过几乎相同的方式使用 `RecipeTitle`。 此示例说明了创建 React 应用程序的本质：创建并使用组件来生成应用程序。

## 查看结果

保存所有文件。 浏览器应自动刷新并显示已更新的页面。 页面顶部应显示标题“Mashed potatoes”。

![显示食谱标题的网页屏幕截图。](https://learn.microsoft.com/zh-cn/training/modules/react-get-started/media/title.png)

# 创建第一个组件

React 开发基于组件完成。 这些自包含单元旨在实现重用和模块化。 React 项目通常包含多个组件。

组件可以是函数，也可以是类。 多数 React 开发人员都倾向于使用函数创建组件，因此我们将重点介绍这种类型。

应用程序一般具有一个核心组件，我们通常称之为 `App`。 `App` 充当应用程序的根。 首先，我们将创建 `App` 组件。

## 创建组件

1. 打开 Visual Studio Code。
2. 在 src 中创建一个新文件。 将其命名为 App.jsx。
3. 添加以下代码：
   **JavaScript**复制

   ```
   import React from 'react';

   function App() {
       return (
           <article>
               <h1>Recipe Manager</h1>
           </article>
       )
   }

   export default App;
   ```

### 浏览代码

通过导入 `React` 启动 App.jsx 文件，这样就可以使用 JSX 语法。 然后创建一个名为 `App` 的函数，方法如同采用 JavaScript 创建任何其他函数。 最后，使用标准 JavaScript 语法导出该函数。 组件的核心包含在 `return` 语句之中。

请注意，我们使用的是嵌入 JavaScript 的 HTML（严格来说是 XML）。 此功能显示了 JSX 的作用。 我们可以使用 JavaScript 的逻辑和功能创建自包含工作单元（组件）。

函数（或组件）返回的 HTML 显示在页面上。 标题包含文本“Recipe Manager”。

 备注

`h1` 元素嵌套在 HTML 5 `article` 元素内。 由于 JSX 使用 XML，因此我们必须有一个根元素。 `article` 元素是此组件的根。 借助此结构，我们能够随着应用程序扩展添加 HTML 和其他 React 组件。

## 将应用程序更新为使用核心组件

让我们将应用程序更新为使用新的组件。

1. 打开 index.jsx。
2. 在内容为 `import ReactDOM from 'react-dom';` 的行（应是第 3 行）之后，添加以下代码：
   **JavaScript**复制

   ```
   import App from './App';
   ```

3. 找到内容为 `<h1>Hello, world!</h1>` 的代码。 将此初始消息替换为对 `App` 组件的调用：
   **jsx**复制

   ```
   <App />
   ```

### 浏览代码

现在，index.jsx 的完整内容如下所示：

**jsx**复制

```
import React from 'react';
import ReactDOM from 'react-dom';
import App from './App';

ReactDOM.render(
    <App />,
    document.getElementById('app')
);
```

`import` 语句用于导入组件，其使用的语法与我们用于任何其他模块的语法相同。 现在，可以像使用 HTML 一样使用该组件。

 备注

由于 JSX 使用 XML 语法，所以我们必须结束 `App` 标记。 我们可以使用长格式语法 `<App></App>` 或“自结束”的速记 `<App />`，来实现此目的。 两个选项的作用相同，但多数开发人员使用速记选项。

## 查看结果

保存所有文件。 浏览器自动刷新并返回结果！

![浏览器窗口中的“食谱管理器”标题的屏幕截图。](https://learn.microsoft.com/zh-cn/training/modules/react-get-started/media/recipe-manager.png)

# 添加样式

使用 React 时，你就是在创建 HTML。 创建方法有所不同，但浏览器仍会呈现 HTML、CSS 和 JavaScript。

我们甚至可以向组件添加 CSS，以向它们应用样式。 若要向组件添加 CSS，我们将按照导入任何其他 JavaScript 依赖关系的相同方式引用它。

## 添加 CSS

1. 向 src 文件夹添加一个新文件。 将其命名 index.css。
2. 将以下样式添加到此文件：
   **css**复制

   ```
   article {
       margin-left: 10%;
       margin-right: 10%;
       font-family: Verdana, Geneva, Tahoma, sans-serif;
       font-size: 18px;
   }
   ```

   根据需要自定义此样式吧！

## 导入 CSS

1. 打开 App.jsx 文件。
2. 在此文件的顶部添加以下代码行：
   **JavaScript**复制

   ```
   import './index.css'
   ```

3. 返回到浏览器并刷新。 网站将更新为新样式！

# 从头开始创建 React 项目

在此模块中，我们使用了初学者项目，以便快速掌握并运用新技能。 通过这种设置，我们可以重点关注 React 和一些新语法。 你可以根据需要使用初学者项目完成自己的工作。

你有可能会想要从头开始生成项目。 若要从空文件夹开始生成，请按照此单元中的步骤操作。 如同在初学者项目中的操作一样，这些步骤也使用 Snowpack。

此单位是可选单元。 如果不需要创建自己的项目，请继续学习下一个单元。

## 了解项目结构

核心设置包含两个用于存储代码的主文件夹：

* **public**
  * 包含任何 HTML、CSS、图像或其他静态文件
  * 存储 index.html 和 index.css 文件
* **src**
  * 包含需要呈现的任何文件
  * 存储所有 .jsx 文件

我们还将创建两个文件，用于配置应用程序：

* package.json：包含用于应用程序的包和脚本的列表
* snowpack.config.js：包含 Snowpack 的配置选项

我们的应用程序需要三个主程序包：

* Snowpack：用于将 JSX 呈现为 HTML 和 JavaScript
* React：用于创建组件
* React-DOM：用于载入应用程序

## 创建初始结构

在空目录中，首先使用 npm 安装必要的组件。 然后配置 Snowpack 并将脚本添加到 package.json 文件。

1. 打开终端或命令窗口。 然后运行以下命令，为 npm 创建目录和 package.json。 在 Mac 或 Linux 上，使用 `mkdir`，在 Windows 上，使用 `md` 创建目录。
   **Bash**复制

   ```
   # Windows
   md react-recipes && cd react-recipes
   md src
   md public
   touch package.json
   echo "{}" > package.json

   # Linux or macOS
   mkdir react-recipes && cd react-recipes
   mkdir src
   mkdir public
   touch package.json
   echo "{}" > package.json
   ```

2. 在同样的终端或命令窗口中运行以下代码。
   **Bash**复制

   ```
   npm install --save-dev snowpack
   npm install react react-dom
   ```

   备注

   Snowpack 是一个开发依赖项。 也就是说，它不是生产所必需的，它用于在生成过程中生成所需的 JavaScript 和 HTML 文件。
3. 通过运行以下命令在 Visual Studio Code 中打开目录。
   **Bash**复制

   ```
   code .
   ```

## 设置 Snowpack

Snowpack 等工具大多数时候会自行完成配置，这是它们的优点之一。 不过，我们需要显示代码的文件夹结构。 为显示文件夹结构，我们将设置 snowpack.config.js 文件中的选项。

1. 在 Visual Studio Code 中，选择“文件”>“新建文件”，以创建一个新文件。
2. 将该文件命名为 snowpack.config.js。
3. 将以下代码添加到此新文件。
   **JavaScript**复制

   ```
   module.exports = {
       mount: {
           'public': '/',
           'src': '/dist'
       }
   }
   ```

此代码将指示 Snowpack 使用 public 文件夹作为应用程序的根。 它还将 src 目录设置为它将生成的 JavaScript 文件和 HTML 文件所在的虚拟位置。

## 创建 npm 脚本

我们将两个脚本与 Snowpack 一起使用，以便支持开发工作。 第一个脚本用于启动开发服务器。 应用程序发生修改时，此操作会自动刷新页面。 当我们准备好生成部署所需的所有文件时，将用到第二个脚本。

1. 在 Visual Studio Code 中，打开 package.json 文件。
2. 在文件底部的最后一个花括号 (`}`) 上方，添加以下代码。 此代码创建启动和生成脚本。
   **JSON**复制

   ```
   {
       "scripts": {
           "start": "snowpack dev",
           "build": "snowpack build"
       }
   }
   ```

   整个文件现在应如以下代码所示。

   **JSON**复制

   ```
   {
     "devDependencies": {
       "snowpack": "^2.18.5"
     },
     "dependencies": {
       "react": "^17.0.1",
       "react-dom": "^17.0.1"
     },
     "scripts": {
         "start": "snowpack dev",
         "build": "snowpack build"
     }
   }
   ```

3. 选择“文件”>“全部保存”，以保存所有文件。

现在，你已完成设置初学者项目！ 可以添加 index.html、App.jsx 和其他文件，就像前面单元中的操作方法一样。

---

## 下一单元: Hello, world

# 知识检查

为每个问题选择最佳答案。 然后选择“核对答案”。

**1.** 什么是 JSX？

[ ] JavaScript 与 XML 的组合

正确。 JSX 由 JavaScript 和 XML 组合而成。

[ ] 一种新的 JavaScript 版本

[ ] React 项目的输出

**2.** 为什么要使用 JSX 来创建 React 应用程序？

[ ] JSX 是唯一受支持的创建 React 应用程序的方法。

[ ] JSX 有助于管理代码。 它使用 HTML 注入所需的逻辑。

正确。 你可以通过 JSX 将逻辑和 HTML 组合在一起。 它是用于创建 React 组件和应用程序的首选方式。

[ ] 所有浏览器都支持 JSX。

**3.** 捆绑程序在 Web 开发过程中有什么作用？

[ ] 生成 JSX

[ ] 将 JSX 和其他资源转换为 JavaScript

正确。 捆绑程序将 JSX 和其他文件类型转换为浏览器可以读取的 JavaScript 代码。

[ ] 启动应用程序

# 总结

React 是最热门的前端 JavaScript 框架。 你可以使用它来创建基于浏览器的应用程序和本地安装的应用程序。 React 引入了一个名为 JSX 的新语法来控制用户界面。

在此模块中，我们首先了解了 React 的基本概念。 我们目睹了 React 是如何帮助生成 Web 应用程序的。 我们探究了安装选项，以及如何使用捆绑程序来管理 JSX 文件。 创建第一个项目和组件后，我们在本地运行了代码。 我们还提到了 React 可帮助生成的其他应用程序类型。

你已了解如何执行以下操作：

* 了解 React 的核心概念。
* 生成 React 应用程序。
* 创建组件。
