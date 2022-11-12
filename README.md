# jabletvdownload 简易教程

# 视频教程地址:https://youtu.be/j0o9EuEyqaw

1. 基本软件安装
	1. git:https://github.com/git-for-windows/git/releases/download/v2.38.1.windows.1/Git-2.38.1-64-bit.exe
	2. ffmpeg:https://www.gyan.dev/ffmpeg/builds/ffmpeg-release-full.7z
	3. python:https://www.python.org/ftp/python/3.11.0/python-3.11.0-amd64.exe

2. 配置个软件的环境变量

3. 配置[powershell](https://github.com/PowerShell/PowerShell/releases/download/v7.3.0/PowerShell-7.3.0-win-x64.msi)代理

	
	```powershell
	
	echo $profile	#查看配置文件路径
	Test-Path $profile	#测试文件路径,看配置文件是否存在
	New-Item -Path $profile -Type File –Force	#新项 配置文件路径 配置文件类型 文件强制
	notepad $profile
	function openproxy() {
	  $Env:https_proxy="http://localhost:7890"
	  $Env:http_proxy="http://localhost:7890"
	}
	function closeproxy() {
	  $Env:https_proxy=""
	  $Env:http_proxy=""
	}
	
	```

4. 开启代理
	```
	openproxy
	```

4. 下载仓库到本地

	```bash
	git clone https://github.com/hcjohn463/JableTVDownload
	```
5. 更改requirements.txt中的模块版本，避免出现可能出现的问题

	```
	pycryptodome==3.4.3 --> pycryptodome==3.15
	```
6. 安装必要的依赖
	```
	pip install -r requirements.txt
	```
7.下载视频
	```
	python main.py

	輸入jable網址:https://jable.tv/videos/ssis-560

	```

