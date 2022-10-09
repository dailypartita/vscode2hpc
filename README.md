## 如何用vscode连接到华大的HPC超算集群

- 面向对象：
	HPC无法正常联网的用户

- 为什么用vscode，而不是putty、mobaxterm等终端：
	1. vscode可以直接在集群上可视化多种特殊文件，如PDF，xlsx，csv，markdown...
	2. vscode可以直接在集群上调试python、R代码
	3. vscode可以用常规IDE的书写方式代替VIM，还能自动补全
	......

- vscode本地配置：
	1. 下载，安装vscode
	2. 安装remote-SSH、简体中文拓展包

- vscode集群配置：
	1. 本地下载对应版本的vscode-server：由于集群的登陆节点无法联网，所以需要手动下载vscode-server。连接：https://update.code.visualstudio.com/commit:${commit_id}/server-linux-x64/stable
	2. 上传vscode-server到集群，解压，重命名，在常用的软件目录下创建.vscode-swever/bin目录，把刚才重命名后的目录放到bin目录下，在home目录下创建.vscode-server目录的软链接
	3. 打开vscode的远程资源管理器，配置登陆节点，用户名，输入密码、验证码连接到集群
	4. 下载常用拓展包：vscode-pdf、R拓展、python拓展、office拓展、markdown拓展
	5. 关闭vscode自动更新功能，防止由于vscode版本更新导致需要重新上传vscode-server




