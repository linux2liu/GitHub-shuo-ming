`<kbd>`ctlr `</kbd><kbd>`+`</kbd><kbd>`k `</kbd>` 快捷添加地址

## 一、MarkDown语法

使用Ob写笔记的基本语法，和一些快捷键。有些是Ob的特定格式。
【说明】粗体显示文本表示Ob中的有效输入字符。

## any-rule 正则表达式  在编辑模式下按 F1 选择


### 1. 标题

共可分6级。

# 1级标题：**#**+**空格**+**标题**

## 2级标题：**##**+**空格**+**标题**

### 3级标题：**###**+**空格**+**标题**

#### 4级标题：**####**+**空格**+**标题**

##### 5级标题：**#####**+**空格**+**标题**

###### 6级标题：**######**+**空格**+**标题**

### 2. 分割线

连续输入≥3个的 **-** 或 *****

### 3. 列表

- 无序列表：文本开头使用 *****+**空格**，或者**-**+**空格**
- 有序列表：文本开头使用 **数字**+**.**+**空格**

### **4. 插入外部链接**

- 以地址方式显示：直接粘贴
- 以描述显示：**[描述](链接地址)** 快捷键 Ctrl+K

### **5. 块引用**

段落开头使用 **>**

### **6. 代码**

- 整段代码：段落开头输入一个**[制表符](https://www.zhihu.com/search?q=%E5%88%B6%E8%A1%A8%E7%AC%A6&search_source=Entity&hybrid_search_source=Entity&hybrid_search_extra=%7B%22sourceType%22%3A%22article%22%2C%22sourceId%22%3A336678751%7D)**(Tab)
- 段落文本中的代码：**·代码内容·** (单引号，键盘Esc键下面那个，这里显示的是一个点)
- 代码块：连用三个 **·** (代码块中会使用语法高亮显示)

【注】在使用代码块时，在三个单引号后面输入指定的语言，来选择语法高亮显示的方式。Ob支持的语言和相应代号可以在这里找到： [supported-languages](https://link.zhihu.com/?target=https%3A//prismjs.com/%23supported-languages) 。

### 7. 文字样式

斜体：***内容*** 快捷键 Ctrl+I
粗体：****内容**** 快捷键Ctrl+B
斜+粗：*****内容*****
删除线：**~~内容~~**
高亮文本：**==内容==**

**【注】**在这里 ***** 与 **_** 是通用的

### 8. 插入图片与音频

- 网络附件：
- 本地附件：**![带[后缀文件名](https://www.zhihu.com/search?q=%E5%90%8E%E7%BC%80%E6%96%87%E4%BB%B6%E5%90%8D&search_source=Entity&hybrid_search_source=Entity&hybrid_search_extra=%7B%22sourceType%22%3A%22article%22%2C%22sourceId%22%3A336678751%7D)]]** 或者直接从本地拖入

【注1】在Ob中拖入的本地图片与音频会以附件的重新复制到库中，建议先在库中新建一个文件夹，然后右键选择将其作为附件文件夹，这样所有新添加的附件就都会保存到该文件夹中，方便管理。

【注2】直接使用**![[带后缀文件名]]**语句时，附件需已存放在附件文件夹中。

### **9. 标签**

首先在插件中打开标签管理插件，
然后在笔记中使用 **#**+**[标签文本](https://www.zhihu.com/search?q=%E6%A0%87%E7%AD%BE%E6%96%87%E6%9C%AC&search_source=Entity&hybrid_search_source=Entity&hybrid_search_extra=%7B%22sourceType%22%3A%22article%22%2C%22sourceId%22%3A336678751%7D)** 添加标签。

### 10. [任务列表](https://www.zhihu.com/search?q=%E4%BB%BB%E5%8A%A1%E5%88%97%E8%A1%A8&search_source=Entity&hybrid_search_source=Entity&hybrid_search_extra=%7B%22sourceType%22%3A%22article%22%2C%22sourceId%22%3A336678751%7D) 复选框

- 已完成：**- [x]**+**空格**+**内容**
- 未完成：**- [ ]**+**空格**+**内容**

【注】在预览界面中可以直接单击复选框来改变其状态。

### 11. 绘制表格

![](https://pic4.zhimg.com/80/v2-ed3f84501832dc56d7d63180366c9d8f_720w.jpg)

（偷一张图）链接：https://zhuanlan.zhihu.com/p/24575242

- 用符号 | 作为列分割。
- 表头和表体使用 **----** 进行分割，其中 **-** 的数量应≥3。
- 在分割栏横线中使用 **:** 设置该列文本对齐方式，不加为居左，头尾加为居中，尾加为右。
- 单元格内换行可用**`<br/>`**。
- 每一行的[列数](https://www.zhihu.com/search?q=%E5%88%97%E6%95%B0&search_source=Entity&hybrid_search_source=Entity&hybrid_search_extra=%7B%22sourceType%22%3A%22article%22%2C%22sourceId%22%3A336678751%7D)允许少于总列数。

#### Case 1: 预留宽度，用于打印后填写

一个更加优雅的方法则是使用空的 `<img>` 标签。例如

| a | b  | c |
| - | -- | - |
| 1 | `` | 3 |

#### Case 2: 长文本需要指定列宽，控制换行

第一种方法可以使用

```
<div> style="width:[长度]">[单元格文本](https://www.zhihu.com/search?q=%E5%8D%95%E5%85%83%E6%A0%BC%E6%96%87%E6%9C%AC&search_source=Entity&hybrid_search_source=Entity&hybrid_search_extra=%7B%22sourceType%22%3A%22article%22%2C%22sourceId%22%3A93239297%7D)] </div>
```

的形式，长度单位可以是 `pt` , `px`, `cm`等。比如：

```
<style>
table th:first-of-type {
    width: 4cm;
}
table th:nth-of-type(2) {
    width: 150pt;
}
table th:nth-of-type(3) {
    width: 8em;
}
</style>
```

| a           | b           | c          |
| ----------- | ----------- | ---------- |
| 列宽 = 3 cm | 列宽 = 5 cm | 列宽 = 8em |

### 12. [脚注](https://www.zhihu.com/search?q=%E8%84%9A%E6%B3%A8&search_source=Entity&hybrid_search_source=Entity&hybrid_search_extra=%7B%22sourceType%22%3A%22article%22%2C%22sourceId%22%3A336678751%7D)

- 普通脚注：**[^脚注简介]** 然后另起一行输入 **[^脚注简介]: 脚注内容**
- [内部脚注](https://www.zhihu.com/search?q=%E5%86%85%E9%83%A8%E8%84%9A%E6%B3%A8&search_source=Entity&hybrid_search_source=Entity&hybrid_search_extra=%7B%22sourceType%22%3A%22article%22%2C%22sourceId%22%3A336678751%7D)：**^[脚注内容]**

![](https://pic3.zhimg.com/80/v2-a5523967dfbaddd56041f9d610dd05de_720w.jpg)

细节如图所示

### 13. [数学公式](https://www.zhihu.com/search?q=%E6%95%B0%E5%AD%A6%E5%85%AC%E5%BC%8F&search_source=Entity&hybrid_search_source=Entity&hybrid_search_extra=%7B%22sourceType%22%3A%22article%22%2C%22sourceId%22%3A336678751%7D)

（我暂时用不到。）

### **14. [内部链接](https://www.zhihu.com/search?q=%E5%86%85%E9%83%A8%E9%93%BE%E6%8E%A5&search_source=Entity&hybrid_search_source=Entity&hybrid_search_extra=%7B%22sourceType%22%3A%22article%22%2C%22sourceId%22%3A336678751%7D)**

链接到其它页面(笔记)： **[笔记名称](https://www.zhihu.com/search?q=%E7%AC%94%E8%AE%B0%E5%90%8D%E7%A7%B0&search_source=Entity&hybrid_search_source=Entity&hybrid_search_extra=%7B%22sourceType%22%3A%22article%22%2C%22sourceId%22%3A336678751%7D)]]**
直接在笔记中嵌入其它笔记内容：**! [[笔记名称]]**

【注】当在笔记中直接输入**[[名称]]**创建一个内部链接时，若该链接指定的页面不存在，则关系图中会使用一个灰色的节点来表示。单击该节点或者在预览中单击链接，将会直接创建一个新笔记。

