---
title: Git本地到远程
date: 2023-09-10 10:37:58
tags:
---



有关终端和命令的，Linux端，直接打开终端就行，Windows端，则需要在你想当Git仓库的文件夹中git bash here，然后在打开的终端中输命令



**步骤 1：在GitHub上创建一个新的仓库**

1. 登录到您的GitHub帐户。

2. 在GitHub页面右上角，点击加号（+），然后选择“New repository”（新仓库）。

3. 在“Repository name”（仓库名称）字段中输入您的仓库名称，选择其他选项，然后点击“Create repository”（创建仓库）。

**步骤 2：在本地创建一个新的Git仓库**

> linux

1. 打开终端或命令提示符。

2. 进入您要创建仓库的本地文件夹。可以使用`cd`命令来导航到文件夹，例如：
   ```
   cd /path/to/your/folder
   ```

3. 初始化一个新的Git仓库：
   ```
   git init
   ```

>Windows

直接自己新建一个文件夹，然后进入该文件夹，鼠标右键，git bash here，然后在打开的终端中执行

```
git init
```



**步骤 3：将文件添加到Git仓库**

1. 将您的项目文件复制到新创建的本地Git仓库文件夹中。

2. 使用以下命令将这些文件添加到Git仓库中：
   ```
   git add .
   ```

3. 使用以下命令提交文件到Git仓库，并添加一条提交消息：
   ```
   git commit -m "Initial commit"
   ```

**步骤 4：将本地Git仓库连接到GitHub仓库**

1. 回到GitHub页面，并在仓库设置中找到“Quick setup”（快速设置）部分。
2. 复制“…or push an existing repository from the command line”（或从命令行推送现有仓库）中的HTTPS或SSH URL。

如果找不到，直接在code的SSH复制链接

![image-20230928123316284](https://cdn.jsdelivr.net/gh/chengkhen/picture_via_picco/202309281233622.png)

**步骤 5：将本地Git仓库与GitHub仓库关联并推送**

1. 返回到终端或命令提示符，运行以下命令，将本地仓库与GitHub仓库关联（请将 `<GitHub Repo URL>` 替换为从GitHub复制的URL）：
   ```
   git remote add origin <GitHub Repo URL>
   ```

2. 使用以下命令将本地仓库的主分支推送到GitHub仓库（通常是master或main分支，取决于您的设置）：
   ```
   git push -u origin master  # 或者 git push -u origin main
   ```

3. 如果是第一次推送到GitHub，可能需要提供GitHub用户名和密码或令牌进行身份验证。

一旦完成上述步骤，本地Git仓库将被上传到GitHub，并与GitHub仓库同步。可以随时将更改推送到GitHub，使用`git add`和`git commit`添加和提交更改，然后使用`git push`命令将它们推送到GitHub仓库。
