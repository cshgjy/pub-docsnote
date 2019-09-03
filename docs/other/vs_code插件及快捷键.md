
# 软件的使用

## vs_code  

### 基本插件  

#### 中文汉化包  

```
对于一些英文不太好的小伙伴，上来第一件事肯定是要切换成中文语言环境，安装汉化包插件之后，按快捷键Ctrl+Shift+P调出命令面板，输入Configure Display Language，选择zh-ch，然后重启vs code即可。
```

#### `open-in-browser` 在浏览器中查看  

```
VS Code没有提供直接在浏览器中运行程序的内置功能，所以我们需要安装此插件，在浏览器中查看我们的程序运行效果。
```

#### `Live Server` 实时预览  

[演示](http://suo.im/4oXFUc)
```
安装这个插件之后，我们在编辑器中修改代码，按Ctrl+S保存，修改效果就会实时同步，显示在浏览器中，再不用手动刷新。
```

#### `Auto Close Tag` 自动闭合标签  

[演示](http://suo.im/4oXFOI)
```
输入标签名称的时候自动生成闭合标签，特别方便。
```

#### `Auto Rename Tag` 尾部闭合标签同步修改  

[`Auto Rename Tag` 尾部闭合标签同步修改](http://suo.im/584WeD)

```
自动检测配对标签，同步修改。
```

#### `Bracket Pair Colorizer` 同颜色括号匹配高亮  

[用不同颜色高亮显示匹配的括号](http://suo.im/5fB9AU)  

```
对配对的括号进行着色，方便区分，未安装该插件之前括号统一都是白色的。
```

#### `Highlight Matching Tag` 高亮显示匹配标签  

[演示](http://suo.im/4DZGhG)  

```
这个插件自动帮我们将选中的匹配标签高亮显示，再也不用费劲查找了。
```

#### `Vscode-icons VSCode` 文件图标  

```
此插件可以帮助我们根据不同的文件类型生成对应的图标，这样我们在侧边栏查看文件列表的时候直接通过图标就可以区分文件类型。
```

#### `TODO Highlight` 高亮  

[高亮](http://suo.im/584WNN)
```
如果我们在编写代码时想在某个地方做一个标记，后续再来完善或者修改里面的内容，可以利用此插件高亮显示，之后可以帮助我们快速定位到需要修改的代码行。
```

#### `Code Spell Checker` 单词拼写检查  

[单词拼写检查](http://suo.im/4oXGoG)  

```
我们在编写代码的时候经常会不小心拼写错误造成软件运行失败，安装这个插件后会自动帮我们识别单词拼写错误并且给出修改建议，大大帮我们减轻了排除bug的压力。
```
#### `Bookmarks` 书签  

[书签](http://suo.im/584um4)  
对代码进行书签标记，通过快捷键实现快速跳转到书签位置。

#### 快捷自定义设置  

[演示：](http://suo.im/4wtTJl)

## 常用快捷键  

### 编辑器与窗口管理    

Ctrl+Shift+P: 打开命令面板。
Ctrl+Shift+N: 新建窗口。
Ctrl+Shift+W: 关闭窗口。
切分窗口：Ctrl+1/Ctrl+3/Ctrl+3
Ctrl+H：最小化窗口
Ctrl+B：显示/隐藏侧边栏
Ctrl+"+/-"：放大/缩小界面
文件操作
Ctrl+N：新建文件
Ctrl+W：关闭文件
Ctrl+Tab：文件切换  

### 格式调整  

Ctrl+C/Ctrl+V：复制或剪切当前行/当前选中内容
Alt+Up/Down：向上/下移动一行
Shift+Alt+Up//Down：向上/下复制一行
Ctrl+Delete：删除当前行
Shift+Alt+Left/Right：从光标开始向左/右选择内容
### 代码编辑  

Ctrl+D：选中下一个相同内容
Ctrl+Shift+L：选中所有相同内容
Ctrl+F：查找内容
Ctrl+Shit+F：在整个文件夹中查找内容

## 常用设置  

我们可以在settings.json中手动进行一些设置，让我们的编辑器更好用。

### 关闭标签介绍信息  

我们在编写代码的时候鼠标移动到某个标签上，经常会自动弹出一些介绍信息，挡住部分代码，给我们的阅读带来了很大的困难，一直没有找到关闭它的方法，目前可以通过设置时间延迟暂时实现这个效果，我设置的5000毫秒，你可以设置的更大一些，基本上它就不会弹出来了。

```
"editor.hover.delay": 5000
```
![演示](http://suo.im/584uIu)


### 自动折行  

设置代码根据编辑器窗口大小自动折行
```
"editor.wordWrap": "on"
```

![](http://suo.im/5fBaCW)

### 字体设置
```js
// 一款适合代码显示的字体包（需要将字体包下载到本地）
  "editor.fontFamily": "Source Code Pro, 'Source Code Pro'",
// 设置代码字体大小
  "editor.fontSize": 15,
```

### 自动保存  

目前有四个选项：

* `off`：关闭自动保存。
* `afterDelay`：当文件修改后的时间超过"`Files：Auto Save Delay`"中配置的值时自动进行保存。
* `onFocusChange`：编辑器失去焦点时自动保存更新后的文件。
* `onWindowChange`：窗口失去焦点时自动保存更新后的文件。

```
"files.autoSave": "off"
```

### 关闭代码提示

```js
"editor.quickSuggestions": { "other": false, "comments": false, "strings": false }
```
