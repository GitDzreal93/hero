# 百万英雄答题助手
使用 `Python` 开发的答题助手，适配百万英雄、芝士超人、冲顶大会、头脑王者，自动显示答案，支持 Android 手机或电脑模拟器。

## 号外
* 电脑小白怎么办？邮件联系作者 `gito@foxmail.com`，免费索取打包好的程序，把右手食指放在鼠标左键上双击就可以运行:)
* 全自动版本的程序已完成，无需连接手机、无需额外安装任何依赖软件。该版本暂无开源计划，详情邮件询问。

## 运行效果截图
![](https://github.com/iflycn/hero/blob/master/cmd.png)

## 如何工作
1. 从手机屏幕获取截图并上传到电脑
2. 裁切出截图中的问题和答案部分，使用百度 ORC 识别文字
3. 抓取问答网站数据，统计每个答案在数据中出现的次数
4. 如果问答网站数据无法匹配，则使用问题+答案为关键字，抓取关键字在百度搜索中出现的次数
5. 根据统计出的数据计算权重并给出建议回答

## 如何使用（Windows 系统）
### 安装 ADB
1. 访问 [ADB Shell](http://adbshell.com/downloads) 下载 `ADB Kits`，解压到硬盘目录，例如 `D:\ADB`
2. 进入系统属性，点击环境变量，在弹出窗口的系统变量中找到 Path 并双击，在弹出窗口的变量值最后加上 `;D:\adb`
### 设置你的手机
3. 开启开发者选项，打开 USB 调试，小米手机一并打开 USB 调试（安全设置）
4. 使用数据线连接手机，等待系统自动安装驱动完成
### 下载程序
5. 下载[百万英雄答题助手压缩包](https://github.com/iflycn/hero/archive/master.zip)，解压到硬盘目录，例如 `D:\hero-master`
6. 修改文件 `config.py` 中的 `APP_ID`、`API_KEY`、`SECRET_KEY` 为你自己的，申请地址：[百度 AI 开放平台](http://ai.baidu.com/tech/ocr/general)
### 安装 Python
7. 从 [Python 官网](https://www.python.org/downloads)下载安装 `python3.6.4`
8. 电脑运行 `CMD`，输入命令 `pip3 install -r D:\hero-master\requirements.txt`，等待下载依赖包并安装完成
9. 如果下载依赖包过程中出错，重新输入命令 `pip3 install -r D:\hero-master\requirements.txt` 直到下载成功
### 开始使用
10. 手机进入百万英雄界面
11. 电脑运行 `CMD`，依次输入命令 `D:`、`cd hero-master`、`python main.py`，根据程序提示操作即可

## 参考项目
- [wuditken/MillionHeroes](https://github.com/wuditken/MillionHeroes)
- [smileboywtu/MillionHeroAssistant](https://github.com/smileboywtu/MillionHeroAssistant)