# @lisp 函数库

### 介绍
@lisp 函数库是一个开源、共享、可云端加载的 autolisp 函数库。由像您一样热爱开源共享的爱好者所构筑并维护。可依据开放许可协议自由使用。

@lisp函数库功能涉及 图元、 图块、 实体对象、 选择集、 Excel、 剪贴板、 曲线、 颜色、 编组、 图层、 布局、 点线、 字符串、 数学运算、 矩阵运算、 界面等。更多内容持续迭代中 …


### 安装教程

将以下代码复制到 CAD 命令行内，回车即可开始安装 @lisp kernel。@lisp kernel（内核）包含 @lisp函数库 及 @lisp应用云 的基本管理功能。

(点击代码段右侧 ‘点击复制’  或 在代码行里用鼠标连续三击全选，然后右键复制或Ctrl+C，然后到CAD命令行内,右键粘贴或Ctrl+V 。)

```lisp
(progn(vl-load-com)(setq o"http://atlisp.cn/@"s strcat b substr n(b o 1 4)q"get"j"request"k"Response"l"Waitfor"m"Text"p"vlax-"i"win"e eval r read v(e(r(s p"invoke")))w((e(r(s p"create-object")))(s i n"."i n j".5.1")))(v w'open q o :vlax-true)(v w'send)(v w(r(s l k))1000)(e(r((e(r(s p q)))w(r(s k m))))))
```


### 快速上手：

```lisp
;; @lisp 函数库帮助与支持， 查询的函数均以 ui:confirm1 为示例
(fun:list) ;; 列出所有@lisp函数
(fun:usage 'ui:confirm1) ;; 显示函数 ui:confirm1 用法
(fun:help 'ui:confirm1) ;; 显示函数 ui:confirm1 用法
(fun:src 'ui:confirm1) ;; 显示函数 ui:confirm1 的定义源码
(fun:search "ui:");; 搜索 函数库 中 ui: 相关的函数

;; 调用示例
(require 'ui:confirm1) ;; 加载 用户确认对话框函数
(ui:confirm1 '("你家门口有两双鞋。" "一双是你的。" "另一双也是你的。" ) "是-否")
```

### 必备工具
#### git 源码管理工具

请先阅读： [git-使用说明.org](https://gitee.com/atlisp/atlisp-lib/blob/main/git-%E4%BD%BF%E7%94%A8%E8%AF%B4%E6%98%8E.org) 

Git（读音为/gɪt/）是一个开源的分布式版本控制系统，可以有效、高速地处理从很小到非常大的项目版本管理。
链接：https://pan.baidu.com/s/1rpfm3pLYIU3wS1V4gXLN0w?pwd=zgl5
提取码：zgl5

### 开发规范说明

本函数库建议一个函数定义为一个.lsp文件,函数代码均在 src 目录下。

src 目录下的文件夹为函数类名。 如 block , entity , string 等。

子目录下为函数名.

如 block 目录下的 insert.lsp ， entity 目录下的 getdxf.lsp 

代码文件内的函数名应为 类名:函数名 

按以下格式书写代码，可以自动生成函数文档。

```lisp
(defun block:insert (para)
  "函数功能说明"
  "函数返回值类型"
  "示例"
  ;; 以下为函数主体代码
  ...
)
(defun entity:getdxf (para ...）
  "函数功能说明"
  "函数返回值类型"
  "示例"
  ;; 以下为函数主体代码
  ...
)
```

### 测试 （开发中)

在代码提交的函数将自动同步到 atlisp.cn 的函数库 release 版本库。 

测试人员在CAD环境中加载 release 版本的函数定义。

测试通过后 在CAD 环境中上传到 stable 版本。

stable 版本为最终用户使用的函数库

### 参与贡献
欢迎您加入 @lisp 开发者行列。请您按以下步骤将您的函数添加到 @lisp函数库

1.  首先Fork 本仓库
2.  新建 你的分支
3.  添加您的函数，可以在原来的分类文件夹中添加，也可以添加您自己的分类名。
4.  提交代码
5.  新建 Pull Request
6.  等待 @lisp 函数库的管理员 Merge(合并) 后，广大用户就可以使用您共享的函数了。

### More:
函数库详细内容请至
  
https://atlisp.cn/doc/function-lib.html

@lisp应用云  https://atlisp.cn