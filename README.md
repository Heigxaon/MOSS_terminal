### 安装

文件管理器使用：[MT管理器](https://mt2.cn/download/)  
- QQ群：768464439  
安卓QQ群下载的文件路径：`/storage/emulated/0/Android/data/com.tencent.mobileqq/Tencent/QQfile_recv/`  

- [蓝奏云下载](https://ycww.lanzn.com/b00wmittna) 密码:`550W`  

- [Gitee下载](https://gitee.com/heigxaon/moss-android-terminal/archive/refs/tags/MOSS.zip)  

- [GitHub下载](https://github.com/Heigxaon/MOSS_terminal/archive/refs/tags/MOSS.zip)  

> 如果有4个`MOSS.tar.gz`包，需要合并  
在MT管理器 **批量选中** 这4个文件， **长按 - 工具 - 文件合并** ，将合并后的文件改名为`MOSS.tar.gz`
1. 将`MOSS.tar.gz`文件移动到`/storage/emulated/0/Documents/`里， **无需解压**  
(如果`/storage/emulated/0/`里没有`Documents`文件夹，需要手动创建)  

2. 所需软件  
 **[Termux](https://github.com/termux/termux-app/releases)** （必需）  
 **[Termux:API](https://github.com/termux/termux-api/releases)** （必需）  
[Termux:Widget](https://github.com/termux/termux-widget/releases) （可选，用于创建桌面小部件）  
[Autox.js](https://github.com/aiselp/AutoX/releases) （可选，用于消息自动回复）  

3. 开启Termux的所有权限，电池策略设为 **无限制**  
开启Termux:API的 **自启动** 权限  
创建Termux:Widget的桌面小部件（若需要）  

4. 用Termux执行：  
`yes | termux-setup-storage && ln -sfn /sdcard/Documents ~/storage/documents && echo -n "▷ 回车继续" && read -n 1 && cd ~/storage/documents && tar -zxvf MOSS.tar.gz -C . && bash MOSS/setup.sh || exit`  
若出现弹窗，请同意 **授予管理所有文件的权限** 

### 接入QQ机器人
1. 下载 [Autox.js](https://github.com/aiselp/AutoX/releases)  
2. 打开Autox.js应用，左上角，开启权限：**无障碍服务** 、**通知读取权限**、**前台服务**、**悬浮窗**、**后台弹出界面**、**允许通知**  
3. 开启你要接入的应用的消息 **通知权限** （比如QQ，一定确保它的后台消息内容能在通知栏显示）  
4. 使用指令`!pre`修改AI回复的前缀内容，默认是 **@MOSS** ，只有以 **@MOSS** 开头的消息才会被回复，你可以改成自己的，比如使用`!pre /`，就会回复以`/`开头的消息  
5. 使用`!name auto`即可切换为自动回复模式，然后用Autox.js运行`消息自动化`脚本  

`[音量减]键`只是 **暂停/恢复** ，并不是关闭/重启  
`[音量加]键`是 **显示/隐藏** 日志，默认关闭  
⚠️如果要重新启动"消息自动化"， **先点击悬浮按钮里的 **╳** 来结束上一个** ，否则会导致两个 **叠加运行**  
⚠️ **_重新启动脚本之前先手动关掉之前的（清理后台没用）_**  

 **手机息屏状态下也可以自动亮屏回复**  
> 前提：  
取消手机锁，亮屏上滑能够直接进入  
关闭省电模式(否则消息接收可能延迟)  
打开QQ的锁屏通知、电池策略设为后台无限制  
在Autox.js打开'前台服务'开关  
关闭防误触(可选，否则手机在口袋的情况无法操作)  
(关于后台、锁屏通知的都打开，包括Autox.js、QQ、Termux，不被电池优化)  

 **隐藏用法**  
> 使用`!app`可切换其它应用，如果是QQ则不限前台和后台消息  
QQ获取前台消息原理是：捕获当前界面的最后一条消息，所以滚动屏幕会让"最后一条"发生变化  
会忽略屏幕右侧自己的消息，除非以`$`开头（自己的消息以`$`开头仍然可以被处理）  
其它应用仅限后台消息，所以不要让聊天应用显示在前台（因为会导致消息不进通知栏从而无法接收）  
`!speech`的原始功能是语音开关，`!stream`的原始功能是流式输出开关，它们在自动回复模式下还有其他功能：  
`!speech`设为关闭可以让回复不@对方，否则AI回复会@对方  
当`!pre`前缀为空的时候会回复所有消息，此时把`!stream`设为关闭就只回复`固定回复.json`里的规则  
