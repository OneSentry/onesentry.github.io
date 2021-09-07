---
title: "GitHub + Jekyll创建自己的博客"
date: 2021-09-06  17:15:05 +0800
category: Markdown
tags: [Markdown, Minimalism]
excerpt: 本文主要从无到有小白式通过GitHub创建博客。
---

## 说明

GitHub可以创建搭建静态页面，搭配Jekyll主题，文件也是 默认使用 [kramdown] 来渲染 markdown 类型文件。

### GitHub创建仓库

* 在GitHub页面上创建一个新仓库

![](https://cdn.jsdelivr.net/gh/OneSentry/ImgHosting/blogImg/blog1.png)

###  创建博客的地址

* 格式：xxx.github.io  **必须是这个格式**   (“xxx”为自己博客取得名称，随便取)

* 下一行是博客说明，随意写

![](https://cdn.jsdelivr.net/gh/OneSentry/ImgHosting/blogImg/blog2.png)

![](https://cdn.jsdelivr.net/gh/OneSentry/ImgHosting/blogImg/blog3.png)


### clone喜欢的主题

* 点击:point_right:[主题 minimalism](https://github.com/showzeng/minimalism):octocat: 去这个主题链接进行下载

![](https://cdn.jsdelivr.net/gh/OneSentry/ImgHosting/blogImg/blog4.png)

* 替换成个人所需要的信息
* “-posts” 如果没有这个文件夹，自己创建一个，这个是存放编写的博文

![](https://cdn.jsdelivr.net/gh/OneSentry/ImgHosting/blogImg/blog5.png)

* 博文的格式必须是2021-9-1-xxx-xxx-xxx.md ("xxx"最好是英文，自己取)，如下图：

![](https://cdn.jsdelivr.net/gh/OneSentry/ImgHosting/blogImg/blog6.png)


效果：

* 无序列表项 一
* 无序列表项 二
* 无序列表项 三

### 5. 有序列表

使用数字和点表示有序列表。

示例：

```
1. 有序列表项 一
2. 有序列表项 二
3. 有序列表项 三
```

效果：

1. 有序列表项 一
2. 有序列表项 二
3. 有序列表项 三

### 6. 引用

使用 `>` 表示引用。

示例：

```
> Less is more. —— 「Andrea del Sarto」
```

效果：

> Less is more. —— 「Andrea del Sarto」

当然，引用也可以嵌套使用。

示例：

```
> Less is more. —— 「Andrea del Sarto」
>> 万物之始，大道至简，衍化至繁。 —— 『道德经』
```

效果：

> Less is more. —— 「Andrea del Sarto」
>
> > 万物之始，大道至简，衍化至繁。 —— 『道德经』

### 7. 行内代码块

使用 \`代码\` 表示行内代码块。

示例：

```
让主题 `Minimalism` 成为行内代码块。
```

效果：

让主题 `Minimalism` 成为行内代码块。

### 8. 代码块

使用四个缩进空格表示代码块。

示例：

```
    这是一个代码块，此行左侧有四个不可见的空格。
```

效果：

    这是一个代码块，此行左侧有四个不可见的空格。

需要指出的是，我并不喜欢和推荐用这种格式来书写，其实这个代码块在主题中就是没有指定代码类型默认的代码块样式 (而指定代码类型使用的是 [Prism] 官网定制的代码渲染主题，你也可以制作你自己的代码渲染主题并替换博客主题的代码渲染主题，具体请参考博客主题定制文章。)，所以，当你想实现一个代码块效果时，推荐如下用法。

示例：

<pre class="highlight">
  <code>
  ```
  这是一个代码块。
  ```

  ```text
  指定代码类型的代码块。
  ```

  ```java
  public class HelloWorld {

      public static void main(String[] args) {
          // Prints "Hello, World" to the terminal window.
          System.out.println("Hello, World");
      }

  }
  ```
  </code>
</pre>

效果：

```
这是一个代码块。
```

``` text
指定代码类型的代码块。
```

```java
public class HelloWorld {

    public static void main(String[] args) {
        // Prints "Hello, World" to the terminal window.
        System.out.println("Hello, World");
    }

}
```

### 9. 插入图像

使用 \!\[描述](图片链接地址) 插入图像。

示例：

```
![头像](https://www.z4a.net/images/2017/08/31/shortcut_icon.png)
```

效果：

![头像](https://www.z4a.net/images/2017/08/31/shortcut_icon.png)

同外链接，图片也可在链接地址后加一个标题，直观效果时鼠标悬停时的文本提示，其语法是链接后加空格和标题文本。

示例：

```
![头像](https://www.z4a.net/images/2017/08/31/shortcut_icon.png "头像")
```

效果 (鼠标悬停在头像上时触发)：

![头像](https://www.z4a.net/images/2017/08/31/shortcut_icon.png "头像")

### 10. 分隔符

使用 `---` 可显示分隔符。

示例：

```
---
```

效果：

---

### 11. 反转义

使用 `\` 可使 Markdown 解析时不会去解析本该属于语法部分的一些符号。

示例：

```
\`代码块\`
```

效果：

\`代码块\`

### 12. Emoji

主题同样也支持 Emoji 表情，使用方法很简单。

示例：

```
(Smile) :smile: (Sob) :sob:
```

效果：

(Smile) :smile: (Sob) :sob:

Emoji 的代码参考 [Emoji sheet]。

### 13. 段内换行

在同一段落里让文本换行，只需在上一行末尾加 2 个空格即可。

示例：

```
这是这个段落的第一行。  
这是同一个段落的第二行。
```

效果：

这是这个段落的第一行。  
这是同一个段落的第二行。

## Markdown 高阶语法

### 1. 删除线

使用 `~~` 表示删除线。

示例：

```
~~这是一段错误的文本。~~
```

效果：

~~这是一段错误的文本。~~

### 2. 注脚

使用 [^keyword] 表示注脚。

示例：

```
这是第一个注脚 [^footnote1] 的样例。

这是第二个注脚 [^footnote2] 的样例。

对应在文章末尾放置如下，点击效果中的注脚即可跳转至文章末尾的注脚注解。

[^footnote1]: 这是第一个注脚的注解。
[^footnote2]: 这是第二个注脚的注解。
```

效果：

这是第一个注脚 [^footnote1] 的样例。

这是第二个注脚 [^footnote2] 的样例。

### 3. 加强的代码块

使用 [Prism] 官网定制的代码高亮主题，选择了所有支持的编程语言，你可以定制你自己的语法主题。

非代码示例：

<pre class="highlight">
<code>
```
$ sudo pacman -S oh-my-zsh-git
```
</code>
</pre>

效果：

```
$ sudo pacman -S oh-my-zsh-git
```

Python 示例：

<pre class="highlight">
<code>
```python
@requires_authorization
def somefunc(param1='', param2=0):
    '''A docstring'''
    if param1 > param2: # interesting
        print 'Greater'
    return (param2 - param1 + 1) or None

class SomeClass:
    pass

>>> message = '''interpreter
... prompt'''
```
</code>
</pre>

效果：

```python
@requires_authorization
def somefunc(param1='', param2=0):
    '''A docstring'''
    if param1 > param2: # interesting
        print 'Greater'
    return (param2 - param1 + 1) or None

class SomeClass:
    pass

>>> message = '''interpreter
... prompt'''
```

JavaScript 示例：

<pre class="highlight">
<code>
``` javascript
/**
* nth element in the fibonacci series.
* @param n >= 0
* @return the nth element, >= 0.
*/
function fib(n) {
  var a = 1, b = 1;
  var tmp;
  while (--n >= 0) {
    tmp = a;
    a += b;
    b = tmp;
  }
  return a;
}

document.write(fib(10));
```
</code>
</pre>

效果：

```javascript
/**
* nth element in the fibonacci series.
* @param n >= 0
* @return the nth element, >= 0.
*/
function fib(n) {
  var a = 1, b = 1;
  var tmp;
  while (--n >= 0) {
    tmp = a;
    a += b;
    b = tmp;
  }
  return a;
}

document.write(fib(10));
```

### 4. 表格支持

示例：

```
| 项目 | 价格 | 数量 |
| -- | -- | -- |
| 计算机 | \$1600 | 5 |
| 手机 | \$12 | 12 |
| 管线 | \$1 | 234 |
```

效果：

| 项目 | 价格 | 数量 |
| -- | -- | -- |
| 计算机 | \$1600 | 5 |
| 手机 | \$12 | 12 |
| 管线 | \$1 | 234 |

表格中的项默认都是左对齐，使用 `:--:` 和 `--:` 可设置居中和右对齐。

示例：

```
| 项目 | 价格 | 数量 |
| -- | :--: | --: |
| 计算机 | \$1600 | 5 |
| 手机 | \$12 | 12 |
| 管线 | \$1 | 234 |
```

效果：

| 项目 | 价格 | 数量 |
| -- | :--: | --: |
| 计算机 | \$1600 | 5 |
| 手机 | \$12 | 12 |
| 管线 | \$1 | 234 |

### 5. 定义型列表

示例：

```
名词 1
: 定义 1（左侧有一个可见的冒号和空格）

名词 2
: 定义 2（左侧有一个可见的冒号和空格）
```

效果：

名词 1
: 定义 1（左侧有一个可见的冒号和空格）

名词 2
: 定义 2（左侧有一个可见的冒号和空格）

### 6. Html 标签

可在 Markdown 语法中直接嵌套 Html 标签，譬如，你可以用 Html 写一个纵跨两行的表格：

示例：

```
<table>
    <tr>
        <th rowspan="2">值班人员</th>
        <th>星期一</th>
        <th>星期二</th>
        <th>星期三</th>
    </tr>
    <tr>
        <td>李强</td>
        <td>张明</td>
        <td>王平</td>
    </tr>
</table>
```

效果：

<table>
    <tr>
        <th rowspan="2">值班人员</th>
        <th>星期一</th>
        <th>星期二</th>
        <th>星期三</th>
    </tr>
    <tr>
        <td>李强</td>
        <td>张明</td>
        <td>王平</td>
    </tr>
</table>

### 7. 待办事项 Todo 列表

使用带有 `[ ]` 或 `[x]` (未完成或已完成) 项的列表语法撰写一个待办事项列表，并且支持子列表嵌套以及混用Markdown语法。

示例：

```
- [x] **博客改版**
    - [x] 响应式布局，移动端适配
    - [ ] 多语言支持
    - [x] 主页
    - [x] 文章列表页
    - [x] 归档页
    - [x] 关于页
    - [x] 文章详情页
        - [x] 排版
        - [x] Markdown 渲染
        - [x] 代码高亮，使用 [Prism](https://prismjs.com/)
        - [ ] Toc 功能
        - [x] 评论功能
        - [x] 打赏功能

- [x] **Minimalism 主题发布**
    - [x] 主题编写
    - [x] 打包发布
```

效果：

- [x] **博客改版**
    - [x] 响应式布局，移动端适配
    - [ ] 多语言支持
    - [x] 主页
    - [x] 文章列表页
    - [x] 归档页
    - [x] 关于页
    - [x] 文章详情页
        - [x] 排版
        - [x] Markdown 渲染
        - [x] 代码高亮，使用 [Prism](https://prismjs.com/)
        - [ ] Toc 功能
        - [x] 评论功能
        - [x] 打赏功能

- [x] **Minimalism 主题发布**
    - [x] 主题编写
    - [x] 打包发布

## 写在最后

本篇博客列举的语法模板部分参考了 [Cmd Markdown 编辑阅读器的语法说明] :+1:，感谢。

---

[^footnote1]: 这是第一个注脚的注解。
[^footnote2]: 这是第二个注脚的注解。

[Minimalism]: https://github.com/showzeng/minimalism
[kramdown]: https://github.com/gettalong/kramdown
[Prism]: https://prismjs.com/
[Emoji sheet]: https://www.webfx.com/tools/emoji-cheat-sheet/
[Cmd Markdown 编辑阅读器的语法说明]: https://www.zybuluo.com/mdeditor?url=https%3A%2F%2Fwww.zybuluo.com%2Fstatic%2Feditor%2Fmd-help.markdown
