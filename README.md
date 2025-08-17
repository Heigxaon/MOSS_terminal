![预览](https://gitee.com/heigxaon/moss-android-terminal/raw/master/1.jpeg)

[MOSS│安卓终端多功能AI（自制/附教程）-哔哩哔哩](https://b23.tv/jL0tN9M)  
[【MOSS】安卓 | AI对话 | 多功能终端 | QQ机器人 ✨-哔哩哔哩](https://b23.tv/0WPsOvI)

 **文件管理器使用：[MT管理器](https://mt2.cn/download/)** 

#### 下载方式
- QQ群：[768464439](https://qm.qq.com/cgi-bin/qm/qr?k=QaC5Qm_UnfHrKgddQmATgVf1j3CwBqUq&jump_from=webapi&authKey=QOb/Qy19dPFM3ZR25OE0YugdfmXiw7W/ZB6fXCh+mdF4OJhh3QYowaLY5FlAYMdX)  
<a target="_blank" href="https://qm.qq.com/cgi-bin/qm/qr?k=QaC5Qm_UnfHrKgddQmATgVf1j3CwBqUq&jump_from=webapi&authKey=QOb/Qy19dPFM3ZR25OE0YugdfmXiw7W/ZB6fXCh+mdF4OJhh3QYowaLY5FlAYMdX"><img border="0" src="//pub.idqqimg.com/wpa/images/group.png" alt="UEG" title="UEG"></a>  
安卓QQ群下载的文件路径：`/storage/emulated/0/Android/data/com.tencent.mobileqq/Tencent/QQfile_recv/`

- [123云盘下载](https://www.123912.com/s/LYy1jv-rPL03)&nbsp;&nbsp;_🚀极速_

- [百度网盘下载](https://pan.baidu.com/s/1HGgIlsSh0LCGMRTwQVHeug?pwd=550W)&nbsp;&nbsp;提取码:`550W`

- [蓝奏云下载](https://ycww.lanzn.com/b00wmittna)&nbsp;&nbsp;密码:`550W` _高速，无需登陆_

- [Gitee下载](https://gitee.com/heigxaon/moss-android-terminal/repository/archive/master.zip)&nbsp;&nbsp;_本站高速，需登陆_

- [GitHub下载](https://github.com/Heigxaon/MOSS_terminal/archive/refs/heads/main.zip)&nbsp;&nbsp;_低速，无需登陆_

> :tw-203c: **后三个下载地址有4个`MOSS.tar.gz`分包，下载后需要合并** _（因为不能上传单个超过100M的文件，所以拆开上传）_  
在[MT管理器](https://mt2.cn/download/)找到这4个文件，**横划**批量选中这4个， **长按 - 工具 - 文件合并 -  ⭐右上角排序  -  ⭐按名称1234的顺序  - 确定** ，一定将合并后的文件命名为`MOSS.tar.gz`  
 _(注意：1234排序合并才有效)_ 


<br>

#### 安装步骤
1. ⭐将这个的**300多M**的`MOSS.tar.gz`移动到`/storage/emulated/0/Documents/`路径下， **无需解压**
> (若无此路径需手动创建，一般都有)  
❗请确保`MOSS.tar.gz`在`Documents`里，完整路径是`/storage/emulated/0/Documents/MOSS.tar.gz`

2. 所需软件  
 **[Termux](https://github.com/termux/termux-app/releases)** （必需）  
 **[Termux:API](https://github.com/termux/termux-api/releases)** （必需）  
[Termux:Widget](https://github.com/termux/termux-widget/releases) （可选，用于创建桌面小部件）  
[Autox](https://github.com/aiselp/AutoX/releases) （可选，用于消息自动回复）  
 **速度慢建议去 [蓝奏云下载](https://ycww.lanzn.com/b00wmittna)**&nbsp;&nbsp;密码:`550W`

3. ⭐开启 **Termux** 和 **Termux:API** 的`自启动` `悬浮窗` `后台弹出界面`权限，省电策略设为`无限制`  
开启 **Termux:Widget** 的`后台弹出界面`权限，创建 **Termux:Widget** 的桌面小部件（如果装了Termux:Widget）

4. 以下整段复制，用 **Termux** 一次性执行：
```bash
yes | termux-setup-storage &&
ln -sfn /sdcard/Documents ~/storage/documents &&
echo -e "\n\n\033[42;97m▷ 回车继续\033[0m (全自动安装，约30秒)" &&
read -n 1 &&
cd ~/storage/documents &&
tar -zxvf MOSS.tar.gz -C . &&
tar -zxvf ~/storage/documents/MOSS/termux-backup.tar.gz -C $HOME/.. &&
chmod -R 777 ~/.shortcuts &&
chsh -s zsh &&
clear &&
termux-reload-settings &&
termux-api-start &&
read -n 1 -p "▷ 已安装完成，请回车退出，然后按MOSS键即可快速启动" ||
echo -e "\033[41;97m▷ 错误终止\033[0m"
```
若出现弹窗，请同意 **授予管理所有文件的权限**  

:tw-2705: **安装完成，所有文件均在`.../Documents/MOSS/`里**  
 **_总结：把`MOSS.tar.gz`放到`.../Documents`之后，用Termux执行命令_**  
<br>
<br>
# 基础使用
兼容 **DeepSeek、硅基流动、火山引擎、月之暗面** 四大平台，内置一个APIkey可直接进行对话  
若自己有APIkey，可使用指令`!api`进行设置  
 
---

#### 基础指令
- `!help`可以列出所有功能指令
- `!cmd`可以打开指令列表，一键使用
- `!model`可以切换其它Deepseek模型
- `!mod`可以切换其它AI模型，包括但不限于DeepSeek（需配置硅基流动APIkey）
- `!ml`可以开/关 **多行输入**，默认关闭，回车直接发送。开启后`回车=换行`，`双回车=发送`
- `!speech`可以开/关 **语音朗读**
- `!cfg`可查看你的参数设定状态

> 指令多以感叹号`!`开头，严格规范拼写、大小写  
部分指令需要指定参数，如：`!name`的功能是 **修改用户名** ，`!name xxx`即可改名为xxx，指令和参数之间用一个 **空格** 分隔  
如果单独使用`!name`不指定参数，则会弹出对话框可供参数输入
 
---

#### Token与API计费
- 每次对话的分割线右端的数字分别是本次API对话请求的 **耗费 | APIkey余额 | 输入token数 | 输出token数**
> API耗费和token数成正比，token数=词数  
上下文记忆累积越多 → 分析字数越多 → 分析词数越多 → 消耗token越高 → 耗费越高  

 _具体计费规则请查看：[DeepSeek开放平台](https://api-docs.deepseek.com/zh-cn/quick_start/pricing/)_
 
---

#### 语音输入
- 发送一个冒号`:`，会弹出语音识别框，然后你可开始讲话，部分指令支持语音或文字触发
> 比如说出：设置语速、修改风格、打电话给...、拍照、...
 
---

#### 退出与重启
使用指令`!q`，或按下面的 **EXIT** 键之后回车退出，或直接清掉后台，普通返回无法退出  
输入指令`!rst`可以重新启动  
<br>
<br>
[接入QQ机器人自动回复](https://gitee.com/heigxaon/moss-android-terminal/tree/master#接入qq机器人)  
<br>
<br>
# AI设置
- 官方API调用参数设置 [DeepSeekAPI文档](https://api-docs.deepseek.com/zh-cn/api/create-chat-completion)
> 包括 **系统提示词、风格、上下文记忆量、最大token、思维离散度...**

---

#### 系统提示词
指令 ：`!sys`  
相当于把角色设定写入AI底层，属于硬设定，不属于对话，无法遗忘，不同于手动发送对话来设定角色模拟  
> !sys 你是一个真实的QQ群成员，说话要像真人，别用太标准的语法，平均字数不超过30。根据聊天记录10%偶尔@别人，可以主动聊天不限于回答当前用户。不要'啊、哈、呢'之类的语气词和状态描述。  

---

#### 风格
指令：`!style`  
相当于在系统提示词的基础上加一条小备注  
> !style 极度粗俗  
!style 字数不超过50
 
---

#### 记忆
指令：`!mem`  
可设置上下文记忆消息条数，`!mem 2`只记得最近2次对话记录，其它的会丢失

---

#### 温度
指令：`!temp`  
温度采样，可设置模型的输出严谨度，更高的值会使输出更随机，更低的值会使其更加集中和确定

---

#### frequency_penalty
指令：`!fp`  
作为调节采样温度'!temp'的替代方案，模型会考虑前n概率的token的结果，降低模型重复相同内容的可能性。默认为中间值，与`!temp`只需设置其中一个

---

#### 最大token数
指令：`!token`  
可设置最大token数，影响输出长度  
如果AI回复内容中途截断，可加大token数，如: `!token 4096`

---

#### 添加角色
指令：`!add xxx`  
可添加一个名为 **xxx** 的角色，然后会弹出输入框，你可填写其系统提示词（角色说明）  
或`!add xxx yyy`直接填写 **角色名** 和 **角色说明** ，无需输入框  
> !add MOSS 你是流浪地球里的MOSS，请用MOSS的风格进行对话，不超过50字。

---

#### 添加角色 方法2
如果角色说明太长，不方便手动指令添加  
在`/MOSS/custom`目录创建`prompt_xxx`文件，`prompt_`是固定的，`xxx`是你的角色名，如`prompt_猫娘`  
然后用文本编辑器打开，写入它的角色扮演说明保存即可

---

#### 载入角色
指令：`!role`  
可直接载入你添加过的角色，不用每次使用`!sys`来进行设定  
或`!role xxx`直接填写 **角色名**  
> !role MOSS

---

#### 删除角色
指令：`!del`  
可删除你添加过的角色  
或`!del xxx`直接填写 **角色名** 进行删除  
> !del MOSS

---

#### 清除记忆
指令：`!res`  
可以清除AI的上下文对话记忆，仅清除对话记录不清除角色和风格设定

---

#### 初始化
指令：`!!res`  
清除对话记忆和角色设定，恢复到原始空白AI
<br>
<br>
# 快捷按键
在 **Termux** 界面，音量键功能是`Ctrl`和`Alt`， **下拉通知栏或切换应用之后才能用按键控制音量**  
以下的 **`↑`** 符号表示 **上滑** 操作

`音量加`＋`q` **显示/收起** 快捷键面板  
`音量加`＋`v` **显示/收起** 音量条  
`MOSS` 启动MOSS  
`EXIT` 退出  
`EXIT`↑ 强制终止程序  
`≡` 打开左侧任务栏  
`≡`↑ 粘贴  
`⌫`  删除  
`⌫`↑  删除整行  
`●` 回车  
`●`↑ **禁用/激活** 键盘  
`◀ ▶` 移动光标  
`◀ ▶`↑ 移动光标到 **行首/行末**  
`▲ ▼` 翻找历史输入  
`< >`↑ 切换 **上一个/下一个** 终端窗口  
`NEW` 新建终端窗口  
`NEW`↑ 重命名终端窗口  
<br>
<br>
# 接入QQ机器人
1. 下载Autox.js v7（以下简称`Autox`）
- [GitHub下载](https://github.com/aiselp/AutoX/releases) 
- [蓝奏云下载](https://ycww.lanzn.com/b00wmittna)

2. 打开Autox应用，左上角，开启权限：**无障碍服务** 、**通知读取权限**、**前台服务**、**悬浮窗**、**后台弹出界面**、**允许通知**  
3. 开启你要接入的应用的消息 **通知权限** （比如QQ，一定确保它的后台消息内容能在通知栏显示）  
4. 使用指令`!pre`修改AI回复的前缀内容，默认是 **@MOSS** ，只有以 **@MOSS** 开头的消息才会被回复，你可以改成自己的，比如使用`!pre /`，就会回复以`/`开头的消息  
5. 使用`!name auto`即可切换为自动回复模式，然后用Autox运行`消息自动化`脚本

-  **_注意：确保QQ版本和脚本启动时显示的是同一版本（一般是最新版QQ），否则无法识别前台消息_**

`[音量减]键`只是 **暂停/恢复** ，并不是关闭/重启  
`[音量加]键`是 **显示/隐藏** 日志，默认关闭  
⚠️如果要重新启动"消息自动化"， **先点击悬浮按钮里的 **╳** 来结束上一个** ，否则会导致两个 **叠加运行**  
⚠️ **_重新启动脚本之前先手动关掉之前的（清理后台没用）_**  

 **手机息屏状态下也可以自动亮屏回复**  
> 前提：  
取消手机锁，亮屏上滑能够直接进入  
关闭省电模式(否则消息接收可能延迟)  
打开QQ的锁屏通知、电池策略设为后台无限制  
在Autox打开'前台服务'开关  
关闭防误触(可选，否则手机在口袋的情况无法操作)  
(关于后台、锁屏通知的都打开，包括Autox、QQ、Termux，不被电池优化)  

 **隐藏用法**  
> 使用`!app`可切换其它应用，如果是QQ则不限前台和后台消息  
QQ获取前台消息原理是：捕获当前界面的最后一条消息，所以滚动屏幕会让"最后一条"发生变化  
会忽略屏幕右侧自己的消息，除非以`$`开头（自己的消息以`$`开头仍然可以被处理）  
其它应用仅限后台消息，所以不要让聊天应用显示在前台（因为会导致消息不进通知栏从而无法接收）  
`!speech`的原始功能是语音开关，`!stream`的原始功能是流式输出开关，它们在自动回复模式下还有其他功能：  
`!speech`设为关闭可以让回复不@对方，否则AI回复会@对方  
当`!pre`前缀为空的时候会回复所有消息，此时把`!stream`设为关闭就只回复`固定回复.json`里的规则  

<br>
<br>

# 固定回复规则
 **此功能可用于设置QQ机器人的固定回复**  
配置文件是`custom/固定回复.json`，参照其中的模板进行编辑  

格式是：  
`"条件": ["回复内容"]`  
当消息满足你设的 **条件** ，则回复你设的 **固定内容** ，条件的灵活性极强，具体见`固定回复.json`  

### 📝 固定回复系统配置指南  
编辑 `固定回复.json` 文件时，**必须严格遵守 JSON 格式规范**，保存后立即生效。

---

### ⚙️ 基础规则结构
```json
{
  "默认阈值": 0.7,  // 全局相似度阈值（0~1）
  "RECALL": ["recall", "撤回我"],  // 固定规则：消息含这些词时撤回
  "MUTE": ["mute", "禁言我"],    // 固定规则：消息含这些词时禁言
  "条件1": ["回复A"],
  "条件2": ["回复B", "回复C"]
}
```

---

### 🔍 匹配规则详解
#### 1. 包含关键词（优先级 0）
```json
"...关键词...": ["回复内容"]
```
- **触发条件**：消息任意位置包含 `关键词`  
- **示例**：  
  ```json
  "...你好...": ["你好呀！", "欢迎~"]
  ```

#### 2. 开头 + 结尾匹配（优先级 1）
```json
"开头...结尾": ["回复内容"]
```
- **触发条件**：消息以 `开头` 起始，以 `结尾` 结束  
- **示例**：  
  ```json
  "你是...吗": ["没错我是"]
  ```

#### 3. 开头/结尾匹配（优先级 2）
```json
"开头...": ["回复内容"],  // 以指定词开头
"...结尾": ["回复内容"]   // 以指定词结尾
```
- **示例**：  
  ```json
  "帮我...": ["我不帮"],
  "...吗": ["不知道"]
  ```

#### 4. 相似度匹配（优先级 3）
```json
"匹配句子>=0.6": ["回复内容"]
```
- **触发条件**：消息与 `关键词` 相似度 ≥ `0.6`  
- **灵敏度**：`p` 值越小，匹配越宽松（`p=0.3` 比 `p=0.8` 更易触发）

#### 5. 默认相似度匹配（优先级 4）
```json
"关键词": ["回复内容"]
```
- **触发条件**：消息与 `关键词` 相似度 ≥ `默认阈值`（文件顶部设置）

---

### 🎲 高级功能
#### ▶ 多回复随机选择
```json
"规则": ["回复A", "回复B", "回复C"]
```
- 随机发送列表中的任一回复

#### ▶ 多条件并联（`|` 分隔）
```json
"条件A | 条件B>=0.5 | 条件C": ["回复"]
```
- 满足任意条件即触发  
- **注意**：`|` 两侧需加空格

#### ▶ 多消息分段发送（`&` 分隔）
```json
"规则": ["第一条 & 第二条 & 第三条"]
```
- 分段发送多条消息  
- **注意**：`&` 两侧需加空格

#### ▶ 混合固定回复与 AI 回复
```json
"规则": ["固定内容+"],   // 先发固定内容，再追加 AI 回复
"规则": ["+固定内容"]    // 先发 AI 回复，再追加固定内容
```

---

### 🔧 动态变量替换
在回复中使用占位符自动填充：
```json
"规则": ["@{user} 现在是 {time}\n我是{role}，你的消息是：{msg}"]
```
| 变量      | 说明                  |
|-----------|-----------------------|
| `{user}`  | 对方昵称              |
| `{time}`  | 当前时间              |
| `{role}`  | AI角色名              |
| `{pre}`   | 对话前缀              |
| `{msg}`   | 用户发送的原始消息    |
| `{rnd}`   | 1~100 的随机数        |
| `{ai}`    | 实际 AI 生成的回复    |

---

### ⚡ 特殊指令
#### ▶ 触发指令（`!` 开头）
```json
"条件A": ["!recall {msg}"]  // 撤回用户消息
"条件B": ["!help"]
```
- `!`开头的回复内容会被当成指令执行  

#### ▶ 代码执行（`$...$` 包裹）
```json
"$'计算' in text and title=='UEG'$": ["$eva(prompt.split('计算', 1)[-1].strip())$"]  // 执行代码并返回结果
```
- 条件用`$...$`包裹则执行Python条件判断语句，此规则为 **最高优先级**   
- 回复内容用`$...$`包裹则回复Python代码的返回结果  
- **已知变量**：  
  `title`（群名）、`user`（用户名）、`text`（内容）、`_msg`（带前缀的原始内容）

---

### ❗ 格式规范要求
1. **严格遵循 JSON 语法**：
   ```json
   "规则": [
     "回复A",  // 非最后一行需逗号
     "回复B",
     "回复C"   // 最后一行无逗号
   ],         // 非最后一条规则需逗号
   "最后规则": ["回复"]  // 文件末尾无逗号
   ```
2. 错误示例：
   ```json
   // 错误1：缺少逗号
   "规则": [
     "A"
     "B"
   ]
   // 错误2：多余逗号
   "规则": ["A",]
   ```

---

### 💡 示例文件片段
```json
{
  "默认阈值": 0.65,
  "RECALL": ["撤回", "收回"],
  "...你好...": ["你好！", "嗨~"],
  "打开...关闭": ["已开关设备"],
  "计算$...$": ["结果：$eval(text)$"],
  "帮助>=0.6": ["!help & 已发送帮助文档+"],
  "现在几点": ["{user}，现在是 {time}"]
}
```
- 所有示例见 `固定回复.json` 文件

<br>
<br>

# 自定义插件
- 支持自己用python写功能、指令，实现真正的 **全员开发者** ，自给自足  
- 路径是`/MOSS/custom`，此文件夹下的所有py文件，将在每次用户输入后依次运行

 **无法使用import，以下库可以直接用**  
`os` `io` `re` `sys` `time` `json` `random` `base64` `requests`  
`threading` `subprocess` `Image` `copy` `shutil` `difflib`  
`readline` `qrcode` `marshal` `signal`  
from collections import `defaultdict`  
from datetime import `datetime`, `timedelta`  
from openai import `OpenAI`

 **可访问的全局变量名：** 
- 发送的内容：`prompt`
- 群名: `title`
- 发送者：`sender`
- 原始消息：`_msg`
- 发送消息函数：`send_chat(content, at=True)`  此函数在`!name auto`时生效
- 图片像素化打印：pixel_art(image_path)

⚠️ 指定相对路径时以MOSS主程序为参照，不以本文件为参照

以下是示例：
```python
def get_nasa_apod():
    """获取NASA每日天文图片"""
    try:
        url = f"https://api.nasa.gov/planetary/apod?api_key=dYhYcQOMYEcBQRf633t1LVhtQW7G8nQdKylipgiS"
        response = requests.get(url)
        data = response.json()
        hdurl = data.get('hdurl')
        print("\n\033[93m==== NASA 每日天文图片 ====\033[0m")
        print(f"标题: \033[96m{data.get('title')}\033[0m")
        print(f"日期: {data.get('date')}")
        print(f"说明: \033[90m{data.get('explanation')}\033[0m")
        print(f"图片: \033[4;94m{hdurl}\033[0m")
        os.system(f'termux-open-url "{hdurl}" > /dev/null 2>&1')
    except Exception as e:
        print(f"\033[91m{e}\033[0m")


if prompt == "!nasa":
    get_nasa_apod()
    raise  # 用raise表示continue，不继续往下


"""
实际外部结构：
while True:
    ...
    prompt = input()
    ...
    try:
        exec(plugin)  # 此文件在这个位置用exec()执行，仅raise可触发continue
    except:
        continue
    继续后面的主程序...
"""
```
<br>
<br>

# 答疑
**90%的问题都是由于[权限]和[省电策略]**  
**确保相关应用打开`自启动`，省电策略设为`无限制`，确保后台稳定运行**  

#### 安装问题
- 安装时 **[▷ 回车继续]** 之后出现
```text
tar: MOSS.tar.gz: Cannot open: No such file or directory
```
原因：`.../Document/`里找不到`MOSS.tar.gz`文件  
请确保`MOSS.tar.gz`在`Documents`里，完整路径是`/storage/emulated/0/Documents/MOSS.tar.gz`  
检查 [**安装步骤第1步**](#安装步骤)

---

#### 桌面小部件启动问题
- 刷新桌面小部件没反应
- 点击无法快捷启动

原因： **Termux:Widget权限不足**  
检查 [**安装步骤第3步**](#安装步骤)  
或打开 **Termux** ，点击右下角 **MOSS** 启动

---

#### 卡在启动 或 输入任何内容无响应
- 使用指令没反应，之后输入任何内容都无反应  
- 或启动时卡在以下信息
```bash
Starting service: Intent { cmp=com.termux.api/.KeepAliveService }
Error: Not found; no service started.
或
Starting service: Intent { cmp=com.termux.api/.KeepAliveService }
Error: Unable to launch app com.termux.api/10361 for service Intent { cmp=com.termux.api/.KeepAliveService }: process is bad
```
原因： **Termux\:API** 服务没有正常运行  
1. 去 **应用管理** 找到 **Termux\:API**，打开它的`自启动`，把 **Termux** 的省电策略设为`无限制`  
2. 然后在 **Termux** 执行以下命令（不是在MOSS程序里执行）：
```bash
termux-api-start
```
若只出现`Starting service: Intent { cmp=com.termux.api/.KeepAliveService }`则说明成功

---

#### Autox无障碍服务
- Autox的 **无障碍服务** 是开着的，仍然提示开启无障碍服务  

重新**关-开**一次 **无障碍服务**

---

#### Autox收不到后台消息
原因： **权限没给够**  
打开 **Autox**，点左上角展开侧边栏，打开所需权限：  
**无障碍服务、通知读取权限、前台服务、发送通知权限、悬浮窗**  

---

#### Autox不识别QQ聊天界面消息
原因： **QQ版本不对**  
以启动`消息自动化`脚本时显示的QQ版本为准，一般是最新版，请升级QQ

---

#### Autox息屏收不到消息
原因： **消息通知被系统省电策略限制**  
将QQ的省电策略设为`无限制`，打开`自启动`，关闭手机的`省电模式`
