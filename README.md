# README

## About

https://github.com/HDT3213/rdb 是目前较为活跃工具，且支持redis7的离线分析工具，属于命令行工具，输出结果不够直观。

因此，本项目依赖HDT3213/rdb进行分析结果展示，是按照阿里云的redis离线分析rdb文件的功能做的。
![alt text](image.png)
![alt text](image1.png)
## Live Development（开发）

本项目使用 Wails，它是一个跨平台桌面应用开发框架，他允许开发者利用 Go 的性能优势，并结合任何前端技术栈，如 React、Vue 或 Svelte，来创建桌面应用。
开发环境搭建，可参考https://juejin.cn/post/7354075693947404351
 - 需要确保系统中已经安装了 Go 和 Node.js，因为 Wails 依赖这两者来构建桌面应用。
 - 安装 wails： go install github.com/wailsapp/wails/v2/cmd/wails@latest
   验证安装结果：wails version

To run in live development mode, run `wails dev` in the project directory. This will run a Vite development
server that will provide very fast hot reload of your frontend changes. If you want to develop in a browser
and have access to your Go methods, there is also a dev server that runs on http://localhost:34115. Connect
to this in your browser, and you can call your Go code from devtools.

## Building（打包）

To build a redistributable, production mode package, use `wails build`.

 在项目根目录，运行 wails build 即可打包当前环境下的应用程序。但是在开发模式下，已经有了一些缓存文件，可以配合 -clean 来清理 build/bin 目录：

wails build -clean

打包 Windows 程序：wails build -platform=windows/amd64

打包 macOS App：wails build -platform=darwin/amd64
