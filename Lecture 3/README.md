# Lecture 3：JavaScript 课堂练习

本课练习 JavaScript 变量、输入输出、函数、按钮事件、DOM 操作和返回值。

## 文件与练习内容

| 文件 | 内容 |
| --- | --- |
| [index.html](index.html) | 基础问候练习：使用变量保存问题与回答，通过 `prompt()` 输入名字，通过 `alert()` 显示问候语。 |
| [exercise6.html](exercise6.html) | 练习 6 的页面结构：标题、带有 `id="demo"` 的段落，以及两个交互按钮；通过 `<script src="script.js"></script>` 引入外部脚本。 |
| [script.js](script.js) | 练习 6 的交互逻辑：`sayHello()`、`showTopic()`、`add(a, b)`，以及两次控制台输出。 |

## 练习一：变量与问候语

打开 `index.html`，点击“开始练习”。

保留老师课堂演示的四行代码：

```javascript
var question = "What is your name?";
prompt(question);
var response = prompt(question);
alert("Hello " + response + ", have a nice day!");
```

1. `question` 保存要询问的问题。
2. 单独调用 `prompt(question)`，只弹出输入框，没有将回答赋给变量。
3. `var response = prompt(question)` 再次询问，并保存第二次的回答。
4. 使用 `+` 拼接字符串，将回答加入问候语，再通过 `alert()` 显示。

第二次输入 `Chen`，会显示 `Hello Chen, have a nice day!`。该版本会询问两次；若只想询问一次，可以删除第二行独立的 `prompt(question);`。

## 练习二：按钮交互与函数（Exercise 6）

打开 `exercise6.html`；它与 `script.js` 必须放在同一文件夹。

### 1. Click me：调用 sayHello()

点击 **Click me**，按钮的 `onclick` 调用 `sayHello()`：

- 弹出 `What is your name?`，询问一次名字。
- 用局部变量 `response` 保存回答。
- 输入 `Chen` 后，弹出 `Hello, Chen, have a good day!`。

### 2. Press me：调用 showTopic()

点击 **Press me**，按钮调用 `showTopic()`：

- `document.getElementById('demo')` 找到页面中指定的段落。
- `x.style.fontSize = "25px"` 将字号改为 25 像素。
- `x.style.color = "red"` 将文字颜色改为红色。

这项练习展示了 JavaScript 如何通过 DOM 修改网页元素的样式。

### 3. add(a, b)：参数与返回值

`add(a, b)` 接收两个参数，通过 `return a + b;` 返回相加结果。

脚本加载时会自动运行：

```javascript
console.log(add(20, 30));   // 50
console.log(add(100, 30));  // 130
```

打开浏览器开发者工具的 **Console** 查看结果。这里的 50 和 130 输出在控制台，不会直接显示在网页正文里。

## 如何运行与检查

1. 下载本文件夹，或在 VS Code 中打开它。
2. 使用 Chrome / Edge 打开对应 HTML；也可以右键 HTML 文件，选择 **Open with Live Server**。
3. 运行 `index.html` 时，确认两次输入框和最后的问候弹窗正常。
4. 运行 `exercise6.html` 时，分别测试两个按钮，并在 Console 中查看 50、130。
5. 如果按钮没有反应，检查 `script.js` 是否与 HTML 在同一目录，再查看 Console 是否有报错。

GitHub 的文件预览页展示源码，不会直接运行 HTML。

## 保存代码与保存回答

GitHub 保存的是文件和提交历史。输入的名字仅在浏览器运行时临时保存在变量中；本练习没有数据库或本地存储，也不会将回答上传到 GitHub。

控制台中的 `undefined` 可以是 `alert()` 或 `console.log()` 的返回值，不表示变量保存失败。`response` 在这两个网页版本中均为函数内的局部变量，不能直接从函数外读取。
