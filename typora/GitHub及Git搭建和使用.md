# GitHub及Git搭建和使用

[TOC]

作者：郭毅鑫

## 1.注册GitHub账户

地址：https://github.com/

## 2.下载Git

地址：https://git-scm.com/downloads

![image-20230612172319877](E:\笔记区\Typora_Date\图片\GitHub-Git下载.png)

![image-20230612172428787](E:\笔记区\Typora_Date\图片\GitHub-Git下载1.png)

## 3.安装Git

1. **基本上都是默认配置，以下是需要关注得地方**

2. 安装详细地址：[Git安装教程（windows） - 战争热诚 - 博客园 (cnblogs.com)](https://www.cnblogs.com/wj-1314/p/7993819.html)

3. 安装配置文件，自己需要的都选上![image-20230612172621644](E:\笔记区\Typora_Date\图片\GitHub-Git安装1.png)

4. ![image-20230612172651996](E:\笔记区\Typora_Date\图片\GitHub-Git安装2.png)

5. 不创建启动文件夹

   ![image-20230612173409319](E:\笔记区\Typora_Date\图片\GitHub-Git安装3.png)

## 4.创建GitHub仓库

1. 新建存储库![image-20230612175142741](E:\笔记区\Typora_Date\图片\GitHub-创建GitHub存储库.png)
2. 填写信息(需要部署简易网站时可以填写：用户名+.github.io;例如：Guo588.github.io；具体配置请看第6小节)，后点击提交创建![image-20230612175455296](E:\笔记区\Typora_Date\图片\GitHub-创建GitHub存储库1.png)   
3. 查看配置![image-20230612180327639](E:\笔记区\Typora_Date\图片\GitHub-创建GitHub存储库2.png)
4. 设置分支，然后点击save保存![image-20230612180538490](E:\笔记区\Typora_Date\图片\GitHub-创建GitHub存储库3.png)   ![image-20230612180633289](E:\笔记区\Typora_Date\图片\GitHub-创建GitHub存储库4.png)

## 5.使用Git，让本地上传到GitHub存储库

1. 打开此电脑，选择一个盘，比如 D 盘，右键空白处点击 git bash here（前提是git已经安装好）。![image-20230612181118217](E:\笔记区\Typora_Date\图片\GitHub-Git使用上传到存储库1.png)

2. 输入如下命令，用来在 D 盘创建 demo1 文件放你的github上的demo1 repository，克隆test repository到 demo1 文件中。![image-20230612181400474](E:\笔记区\Typora_Date\图片\GitHub-Git使用上传到存储库.png)

3. 生成文件夹![image-20230612181446219](E:\笔记区\Typora_Date\图片\GitHub-Git使用上传到存储库2.png)

4. 将自己的网页文件复制粘贴至 D 盘的 demo1- 文件中![image-20230612181515953](E:\笔记区\Typora_Date\图片\GitHub-Git使用上传到存储库3.png)

5. 执行如下命令![](E:\笔记区\Typora_Date\图片\GitHub-Git使用上传到存储库4.png)

6. 提交更改![image-20230612185210582](E:\笔记区\Typora_Date\图片\GitHub-Git使用上传到存储库5.png)

7. 输入git push来发布本地提交![image-20230612190236857](E:\笔记区\Typora_Date\图片\GitHub-Git使用上传到存储库6.png)

   会弹出确定框，确认就好

## 6.部署好后的使用流程

1. 将项目放进本地克隆仓库中，具体位置查看第5.4小节
2. 使用流程![image-20230612191214859](E:\笔记区\Typora_Date\图片\GitHub-使用流程.png)

上述最后一步是连接异常，多尝试几次提交就可以

## 7.网站部署理解

- 创建存储库（如果是以用户为名创建的库，是为默认网址；其创建方式查看第4.2小节）

- 非用户名创建的库，需要在访问路径上加库的名

- 示例：![image-20230612192533209](E:\笔记区\Typora_Date\图片\GitHub-网站部署理解.png)

- 以上为第二个为非用户名创建的库

- **默认访问地址为**

  ```http
  https://guo588.github.io
  ```

  另一个库则为

  ```http
  https://guo588.github.io/demo1
  ```

  当一个库内部有多个页面，而你也需要进入**不同页面时可以添加上指定路径**

  ```http
  https://guo588.github.io/index.html
  ```

  或**另一个页面**

  ```http
  https://guo588.github.io/index1.html
  ```

- **非用户的库则需要再加上库的名字**

  ```http
  https://guo588.github.io/demo1/index.html
  ```

  

## 8.Git中文件名乱码问题

1. 设置Git全局配置中的文件名编码

可以通过以下命令来设置Git全局配置中的文件名编码为UTF-8：

```
$ git config --global core.quotepath false
$ git config --global gui.encoding utf-8
$ git config --global i18n.commit.encoding utf-8
$ git config --global i18n.logoutputencoding utf-8
```