**结合“Hugo + Github + Markdown”搭建一个以“hugo-theme-techdoc”为主题的文档网站**

**前提条件：**


- 已安装 Homebrew。
- 已注册Github账号。
- 已创建新的Github repository。

**操作步骤：**

1.	打开一个终端，执行以下命令，安装Hugo。

	brew install hugo
	

2.	执行以下命令，查看Hugo是否安装成功，检查Hugo版本号。

	hugo version

	回显信息如下，说明安装成功。

	hugo *v0.81.0+extended darwin/amd64 BuildDate=unknown*

3.	执行以下命令，创建一个新的网站。


	hugo new site *techdoc*

4.	执行以下命令，添加一个主题。


	cd */Users/wuguangmin/techdoc*


	git init

	git submodule add *git submodule add https://github.com/thingsym/hugo-theme-techdoc.git themes/hugo-theme-techdoc*


5.	执行以下命令，在根目录下的“config.toml ”文件中添加新数据。


	echo 'theme = " *hugo-theme-techdoc*"' >> config.toml


	说明：
	
* 	Theme配置项指的是所选主题的名称，必须与步骤3中添加的主题相同。在本例中，即theme = " hugo-theme-techdoc"。
*  在“访达”中运用组合键“Command+Shift+G”，在弹出页面的输入框中输入：“/Users/wuguangmin/techdoc”，找到config.toml文件，鼠标右键选择“打开方式 > 文本编辑“。将baseURL 的值"http://example.org/"改为“https://github.com/wuguangmin01/wuguangmin01.github.io.git/”，title 的值"My New Hugo Site”改为  "Hailey's Techdoc Website”,按住“Command+S”保存。
	
6.	在“访达”中运用组合键“Command+Shift+G”，在弹出页面的输入框中输入：“*/Users/wuguangmin/techdoc/content/”，放入已编写完成的_index.md文件，按住“Command+S”保存。
7.	执行以下命令，启动Hugo server。

	hugo server
	
	回显信息如下，说明Server启动成功。

8.	使用浏览器打开"http://localhost:1313/wuguangmin01/wuguangmin01.github.io.git/"预览。
9. 根据网站页面提示，在/user/wuguangmin/techdoc/content,在此目录下放入已编写完成的_index.md文件。

10.	执行以下命令在sunshine/public目录下，为Git本地库添加远程连接。
 
	 git remote add origin git@github.com: git@github.com:*wuguangmin01/wuguangmin01.github.io.git*
 
11. 执行以下命令，查看Git 本地库与远程库的关联情况。
	
	cat.git/config
	
	回显信息如下,说明Git 本地库与远程库关联成功。


12. 执行以下命令，通过commit提交修改到本地库，并写一个commit message 来简洁描述修改内容。

	git status 
      
      git add .
     
     git commit -m “Add a new post”

13. 执行以下命令，将修改推至远程库。

	git push -u origin master

	git status 





