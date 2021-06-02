## 将包变成全局命令的步骤
- 先创建可执行的脚本：#! /usr/bin/env node
> #! /usr/bin/env node 这个配置的意思是用当前系统的环境node去执行这个文件
- 配置package.json中的bin字段
- npm link 链接到本地环境(默认以package.json的name为基准,CMD就可以运行name属性对应的值，或者配置映射表), npm link 会自动产生执行命令
> link 相当于将目前本地模块连接到npm目录下，这个npm目录可以直接访问，所以当前包也就可以直接访问了
`
C:\Users\咸蛋小乐乐\AppData\Roaming\npm\zhu -> C:\Users\咸蛋小乐乐\AppData\Roaming\npm\node_modules\cli-learn\bin\zhu
C:\Users\咸蛋小乐乐\AppData\Roaming\npm\cli-learn -> C:\Users\咸蛋小乐乐\AppData\Roaming\npm\node_modules\cli-learn\bin\zhu
C:\Users\咸蛋小乐乐\AppData\Roaming\npm\node_modules\cli-learn -> D:\咸蛋小乐乐\前端视频\2021年珠峰\练习\cli-learn
`

## 四步实现命令行功能
- 1、配置可执行命令 commander => npm install commander
- 2、要实现脚手架，先做一个命令行交互功能 inquirer
- 3、将模板下载下来 download-git-repo
- 4、根据用户的选择动态的生成内容 metalsmith