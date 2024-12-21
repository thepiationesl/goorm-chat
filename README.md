```
┌───────────────────────────────────────────────┐
                                       _
     __ _  ___   ___  _ __ _ __ ___   (_) ___
    / _` |/ _ \ / _ \| ‘__| ‘_ ` _ \  | |/ _ \
   | (_| | (_) | (_) | |  | | | | | |_| | (_) |
    \__, |\___/ \___/|_|  |_| |_| |_(_)_|\___/
    |___/
			      𝘼𝙣𝙮𝙤𝙣𝙚 𝙘𝙖𝙣 𝙙𝙚𝙫𝙚𝙡𝙤𝙥!
└───────────────────────────────────────────────┘
```
# goormIDE
欢迎使用 goormIDE！
goormIDE 是一个功能强大的云端 IDE 服务，旨在最大限度提高开发者和团队的生产力。
**卓越开发，非凡体验**
`祝您编码愉快！—— goormIDE 团队`

## 创建一个定制的聊天网页
* 技术栈
	* 该项目使用了 `React.js`、`socket.io`、`materialUI` 和 `express`。
* 适用人群
	* 想学习 React 的人。
	* 想体验使用 socket.io 的 WebSocket 魅力的人。
	* 正在寻找有趣主题的 Web 项目的人。
	* 想定制并完成自己的聊天室的人。
* 项目描述
	* 已实现通过 socket.io 进入聊天室并发送/接收消息的功能。
        * 使用了诸如 JOIN_ROOM、SEND_MESSAGE、UPDATE_MESSAGE 等事件名称。
        * 默认未连接数据库。
        * 可以通过设置 MongoDB 连接、禁用 `server/src/index.js` 文件中的注释处理并在配置文件中进行设置，启用默认的数据库设置。
    * 通过实际将消息存入数据库、为每位用户添加个人资料以及创建聊天室列表，打造属于自己的 Goormee-Talk！

* 文件结构
```
.
|-- exit.sh
|-- start.sh
|-- client
|   |-- node_modules
|   |-- package-lock.json
|   |-- package.json
|   |-- .env.development
|   |-- public
|   `-- src
|			|-- components
|			|   |-- Chat
|			|   |-- ChatRoomEntry
|			|   `-- Message
|			|-- containers
|			|   |-- Chat.jsx
|			|   `-- ChatRoomEntry.jsx
|			|-- contexts
|			|   `-- SocketContext.jsx
|			|-- index.js
|			`-- pages
|			    |-- chat.jsx
|			    |-- main.jsx
|			    `-- page.module.scss
`-- server
    |-- config
    |   `-- default.js
    |-- node_modules
    |-- package-lock.json
    |-- package.json
    `-- src
        |-- controllers
        |-- middlewares
        |    `- index.js
        |-- models
        |    |--sample
        |    `--index.js
        |-- routes
        |-- services
        |-- index.js
        `-- sample.js

```

## 🎨 使用方法
1. 检查 URL 和端口
   1. 点击顶部菜单栏中的 `CONTAINER > Running URL and Port`。
   2. 注册客户端和服务器的域名，分别使用 3000 和 3001 端口。
   3. 当项目运行时，客户端将运行在 3000 端口，服务器将运行在 3001 端口。

2. 环境变量和配置设置
    1. 在客户端路径的 `.env.development` 文件中添加以下内容：
    ```
    REACT_APP_SERVER_URL = 你在步骤1中设置的服务器域名
    ```
    2. 在服务器路径的 `config/default.js` 文件中进行以下设置：
    ```
    module.exports = {
        db: { // 如果使用 MongoDB Atlas，请设置此处。
           mongoUrl: ""
        },
        port: 3001, // 设置为与步骤1中服务器端口一致。
        client: "" // 设置为与步骤1中客户端 URL 一致。
    }
    ```

3. 检查依赖项
    1. 在底部终端中输入以下命令以安装客户端和服务器所需的模块：
    ```
    cd client && npm i && cd ../server && npm i && cd ..
    ```

4. 运行项目
   * 点击 IDE 右上角的执行命令以运行项目：
       * 点击 `run client and server`。
   * 访问运行的 URL（容器 > 执行 URL 和端口）：
       * 打开客户端端口注册的 URL。
   * 尝试应用：
       * 如果输入相同的 CHATROOM ID，就可以聊天了。

## 🔧 提示与指南
* 命令功能
	* 通过右上角的快捷图标，您可以轻松运行脚本。
	* 在左侧菜单栏中的 `Commands > Common/Build/Run/Test/Deploy Command` 可以查看更多信息。

* 获取 URL 和端口
	* 点击顶部菜单栏中的 `CONTAINER > Running URL and Port`。
	* 可以查看默认的 URL/Port，并在顶部菜单中添加 URL/Port。

* 实用快捷键

| 快捷键名称        | Mac 命令         | Windows 命令       |
| ------------------ | :-----------: | :--------------: |
| 终端复制          | ⌘ + C         | Ctrl + Shift + C |
| 终端粘贴          | ⌘ + V         | Ctrl + Shift + V |
| 文件搜索          | ⌥ + ⇧ + F     | Alt + Shift + F  |
| 切换终端          | ⌥ + ⇧ + B     | Alt + Shift + B  |
| 新建终端          | ⌥ + ⇧ + T     | Alt + Shift + T  |
| 代码格式化        | ⌥ + ⇧ + P     | Alt + Shift + P  |
| 显示所有快捷键    | ⌘ + H         | Ctrl + H         |

## 支持与文档
访问 [https://ide.goorm.io](https://ide.goorm.io) 了解更多 goormIDE 的使用信息。
若需观看使用指南，请访问 [https://help.goorm.io/en/goormide](https://help.goorm.io/en/goormide)。
