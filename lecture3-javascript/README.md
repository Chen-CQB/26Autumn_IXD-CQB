# Lecture 3：JavaScript 课堂练习

练习内容：变量、prompt 输入、alert 输出，以及用 + 拼接字符串。

## 运行方式

下载本文件夹，用 Chrome 或 Edge 打开 index.html，点击“开始练习”。GitHub 的文件预览页只展示代码，不会直接运行网页。

## 老师的四行代码

```javascript
var question = "What is your name?";
prompt(question);
var response = prompt(question);
alert("Hello " + response + ", have a nice day!");
```

- 第一行把问题保存到 question。
- 第二行弹出输入框，但没有把返回的回答赋给变量。
- 第三行再次弹出输入框，把回答保存到 response。
- 第四行使用第二次的回答拼接并显示问候语。

例如，第二次输入 Chen，弹窗显示 Hello Chen, have a nice day!。

老师的写法会询问两次。若只想问一次，可以删除第二行 prompt(question);。

## “保存代码”和“保存回答”的区别

GitHub 保存的是这两个文件以及它们的修改历史。运行时输入的名字仅保存在浏览器中的临时变量里，不会被提交到仓库，也不会在刷新后自动保留。

控制台中最后出现 undefined，是因为 alert 没有具体返回值，不表示 response 没有保存回答。网页版本将代码放在按钮事件函数中，response 是该函数内的局部变量。