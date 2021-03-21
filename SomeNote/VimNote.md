# Vim 学习笔记

## 常用键位及操作

### 移动

| w   | 移动到下一个单词词首       |
| --- | -------------------------- |
| b   | 移动到上一个单词词首       |
| e   | 移动到下一个单词词尾       |
| ^   | 移动到行首第一个非空字符   |
| 0   | 移动到行首（包含非空字符） |
| $   | 移动到行尾                 |
| 3$  | 可添加数字                 |

### 查找

| f   | 查找     |
| --- | -------- |
| F   | 反向查找 |

| 3f
| t | 到达（目标字符之前） |
| T | 反向到达 |
| ; | , 可以重复以上四个命令 |
| % | 括号匹配 |

### 总体移动

| 快捷键 | 操作       |
| ------ | ---------- |
| 移动   | 到指定位置 |
| gg     | 文首       |
| G      | 文末       |
| 10 gg  |
| 10 G   |

屏幕视野内移动
| 快捷键 | 操作 |
|--------|------|
| H |
| M |
| L |

### 滚屏

| 快捷键 | 操作       |
| ------ | ---------- |
| C-f    | 向下滚整屏 |
| C-b    | 向上整屏   |
| C-u    | 向上滚半屏 |
| C-d    | 向下滚半屏 |
| C-e    | 上滚一行   |
| C-y    | 下滚一行   |
| zz     | 屏幕居中   |

### 简单查找

> 备注 : 字符 .\*[]^%/\?~$ 有特殊含义。如果你要查找它们,需要在前面加上一个"\"。

| 快捷键  | 操作                  |
| ------- | --------------------- |
| /string | 正向查找              |
| %string | 反向查找              |
| n/N     | 切换上/下一个搜索结果 |

> 自定义

| \<leader\>nh | 取消搜索高亮 |
| ------------ | ------------ |

查找时可以使用方向键遍历之前的记录

#### 使用标记（跳转）

| ''     | 位置跳转                |
| ------ | ----------------------- |
| C-o    | 跳转到较老的位置        |
| C-i    | 跳转到较新的位置        |
| ma     | 设置书签 a(并不会显示） |
| 'a     | 跳转到书签 a            |
| :marks | 查看书签列表            |

## 宏的使用

1. qa 将宏录制到寄存器 a 后开始操作
2. 操作
3. 再次按 q 退出录制
4. 到需要执行的地方 @a
5. 多选：

> 使用 V 模式多选后进入命令模式
>
> :normal @a

## 插件快捷键

### Bracey.vim

> live edit html, css, and javascript in vim

| \<leader\>hp | 打开 html, css, javascript 预览 |
| ------------ | ------------------------------- |

### vim-table-mode

> VIM Table Mode for instant table creation.

| \<leader\>tm | 启动 table-mode |
| ------------ | --------------- |
| \<leader>tdd | delete row      |
| \<leader>tdc | delete column   |
| \<leader>tic | insert column   |

> 使用
>
> 1. 启动模式
> 2. 输入表头 | header | header |
> 3. 第二行输入**两次 ||**自动生成表格

### nvim.coc

\<L-h> 查看函数定义帮助
\<L-rn> 重命名变量
:help coc-nvim 打开 coc 帮助

### switch

\<L-swb> 切换 bool 值

### coc.translator

\<leader>ts 翻译单词

### NERDTree

| 命令                                    | 操作                                                 |
| --------------------------------------- | ---------------------------------------------------- |
| \<L-mb> :Bookmark [name]                | 添加书签                                             |
| \<L-bb> :OpenBookmark [name]            | 进入书签                                             |
| I                                       | 打开/关闭 隐藏文件                                   |
| \<L-cb> :ClearBookmarks \[\<bookmarks>] | 清除书签                                             |
| \<L-db> :EditBookmarks                  | 打开书签配置文件                                     |
| o                                       | open file                                            |
| go                                      | open selected file, but leave cursor in the NERDTree |
| t                                       | open selected node/bookmark in a new tab             |
| T                                       | same as 't' but leave the cursor on the current tab  |
| i                                       | open selected file in a split window                 |
| s                                       | open selected file in a vsplit window                |
| D                                       | delete the current bookmark                          |

### commentary.vim

| 快捷键 | 操作                  |
| ------ | --------------------- |
| gcc    | 注释/取消注释单行代码 |
| gc     | 注释/取消注释多行     |

### vCoolor.vim

| hotkey  | operating           |
| ------- | ------------------- |
| \<Alt>c | insert a color      |
| \<Alt>r | insert a rgb color  |
| \<Alt>v | insert a hsl color  |
| \<Alt>w | insert a agba color |
