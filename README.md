# yilou

运行 
```bash
npm start
```
即可启动项目

## 步骤一：初始化项目
在命令行中导航到你计划创建项目的目录，然后运行以下命令以创建一个新的 Node.js 项目：

```bash
npm init -y
```

这将会自动生成一个 `package.json` 文件。

## 步骤二：安装相关依赖

安装 `http-server`， 这是一个简单的零配置命令行 HTTP 服务器：

```bash
npm install --save-dev http-server
```

同时我们也需要安装 `bootstrap` 来使用 Bootstrap 5：

```bash
npm install bootstrap@next
```

## 步骤三：创建 HTML 文件

在项目根目录下创建一个 `index.html` 文件，并添加以下内容到该文件：

```html
<!doctype html>
<html lang="en">
  <head>
    <!-- Required meta tags -->
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width, initial-scale=1">

    <!-- Bootstrap CSS -->
    <link href="node_modules/bootstrap/dist/css/bootstrap.min.css" rel="stylesheet">

    <title>Hello, Bootstrap 5!</title>
  </head>
  <body>
    <h1 class="text-center">Hello, Bootstrap 5!</h1>

    <!-- Optional JavaScript; choose one of the two! -->

    <!-- Option 1: Bootstrap Bundle with Popper -->
    <script src="node_modules/bootstrap/dist/js/bootstrap.bundle.min.js"></script>

  </body>
</html>
```

## 步骤四：设置服务器

在 `package.json` 文件中，添加一个新的脚本命令来启动服务器。这里我们使用 `http-server` 并设定端口为 `8080`（你也可以选择其他端口）：

```json
"scripts": {
  "start": "http-server -p 8080"
}
```

## 步骤五：启动服务

现在你可以通过 npm 在命令行中启动服务器：

```bash
npm start
```
你应该能看到类似于以下的输出：

```bash
Starting up http-server, serving ./
Available on:
  http://127.0.0.1:8080
  http://192.168.1.3:8080
Hit CTRL-C to stop the server
```

打开浏览器，访问 http://localhost:8080 或者是你电脑的 IP 加上 :8080（例如：http://192.168.1.3:8080），你就能看到你的 Bootstrap 5 网页了。
