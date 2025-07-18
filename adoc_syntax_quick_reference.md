# asciidoc语法快速参考 
IvorySQL文档是用“asciidoc”编写的。为确保格式的质量和一致性，在修改更新文档时应遵循某些 [asciidoc](https://docs.asciidoctor.org/asciidoc/latest/syntax-quick-reference/) 规则。


## 规范说明



​    **asciidoc规范**

​    1、标题从一级开始递增使用，禁止跳级使用。例如：一级标题下面不能直接使用三级标题；二级标题下面不能直接使用四级标题。

​    2、标题必须统一使用 ATX 风格，即在标题前加 = 号来表示标题级别。

​    3、标题的引导符号 = 后必须空一格再接标题内容。

​    4、标题的引导符号“=”后只能空一格后再接标题内容，不能有多个空格。

​    5、标题必须出现在一行行首，即标题的 = 号前不能有任何空格。

​    6、标题末尾仅能出现中英文问号、反引号、中英文单双引号等符号。其余如冒号、逗号、句号、感叹号等符号均不能在标题末尾使用。

​    7、标题上面须空一行。

​    8、文档中不能连续出现内容重复的标题，如一级标题为 = IvorySQL 架构，紧接着的二级标题就不能是 == IvorySQL 架构。如果不是连续的标题，则标题内容可重复。

​    9、文档中只能出现一个一级标题。

​    10、一般来说，除 TOC.adoc 文件可缩进 2 个空格外，其余所有 .adoc 文件每缩进一级，默认须缩进 4 个空格。

​    11、文档中（包括代码块内）禁止出现 Tab 制表符，如需缩进，必须统一用空格代替

​    12、禁止出现连续的空行。

​    13、块引用符号 > 后禁止出现多个空格，只能使用一个空格，后接引用内容。

​    14、使用有序列表时，必须从 1 开始，按顺序递增。

​    15、使用列表时，每一列表项的标识符（+、-、* 或数字）后只能空一格，后接列表内容。

​    16、列表（包括有序和无序列表）前后必须各空一行。

​    17、代码块前后必须各空一行。

​    18、文档中禁止出现裸露的 URL。如果希望用户能直接点击并打开该 URL，则使用一对尖括号 (<URL>) 包裹该 URL。如果由于特殊情况必须使用裸露的 URL，不需要用户通过点击打开，则使用一对反引号 (`URL`) 包裹该 URL。

​    19、使用加粗、斜体等强调效果时，在强调标识符内禁止出现多余的空格。如不能出现 `** 加粗文本 **`。

​    20、单个反引号包裹的代码块内禁止出现多余的空格。如不能出现 ` 示例文本 `。

​    21、链接文本两边禁止出现多余的空格。如不能出现 [某链接](https://www.example.com/)。

​    22、链接必须有链接路径。如不能出现[空链接]()或[空链接](#)等情况。

## 示例

1、标题从一级开始递增使用，禁止跳级使用。

```
= Heading 1
=== Heading 3

We skipped out a 2nd level heading in this document
```



2、标题必须统一使用 ATX 风格，即在标题前加 = 号来表示标题级别。

```
= Heading 1
== Heading 2
=== Heading 3
==== Heading 4
== Another Heading 2
=== Another Heading 3
```



3、标题的引导符号 = 后必须空一格再接标题内容。禁止=后多个空格，禁止=前出现空格

错误示范：

```
= Heading 1
== Heading 2
```

正确示范：

```
= Heading 1
== Heading 2
```



4、标题末尾仅能出现中英文问号、反引号、中英文单双引号等符号。 

错误示范

```
= This is a heading.
```

正确示范

```
= This is a heading
```



5、标题上面空一行

错误示范

```
= Heading 1
Some text
Some more text## Heading 2
```

正确示范

```
= Heading 1
Some text
Some more text

== Heading 2
```



6、文档中不能连续出现内容重复的标题，如一级标题为 = IvorySQL  描述，紧接着的二级标题就不能是 == IvorySQL 描述。如果不是连续的标题，则标题内容可重复。

错误示范

```
= Some text

== Some text
```

正确示范

```
= Some text

== Some more text
```



7、文档中只能出现一个一级标题。

错误示范

```
= Top level heading

= Another top-level heading
```

正确释放

```
= Title

== Heading

== Another heading
```



8、一般来说，除 TOC.adoc 文件可缩进 2 个空格外，其余所有 .adoc 文件每缩进一级，默认须缩进 4 个空格。

错误示范

```
* List item
  * Nested list item indented by 3 spaces
```

正确示范:

```
* List item
    * Nested list item indented by 4 spaces
```



9、文档中（包括代码块内）禁止出现 Tab 制表符，如需缩进，必须统一用空格代替

错误示范：

```
Some text
	* hard tab character used to indent the list item
```

正确示范:

```
Some text
  * Spaces used to indent the list item instead
```



10、禁止出现连续的空行

错误示范

```
Some text here


Some more text here
```

正确释放:

```
Some text here

Some more text here
```



11、块引用符号 > 后禁止出现多个空格，只能使用一个空格，后接引用内容。

错误示范

```
>  This is a blockquote with bad indentation>  there should only be one.
```

正确示范

```
> This is a blockquote with correct> indentation.
```



12、使用有序列表时，必须从 1 开始，按顺序递增。

错误示范:

```
1. Do this.
1. Do that.
1. Done.
```

```
0. Do this.
1. Do that.
2. Done.
```

 正确示范:

```
1. Do this.
2. Do that.
3. Done.
```



13、使用列表时，每一列表项的标识符（+、-、* 或数字）后只能空一格，后接列表内容。

正确示范

```
* Foo
* Bar
* Baz

1. Foo
  * Bar
1. Baz
```



14、列表（包括有序和无序列表）前后必须各空一行。

错误示范

```
Some text* Some* List

1. Some2. List

Some text
```

正确示范

```
Some text

* Some
* List

1. Some
2. List

Some text
```



15、代码块前后必须各空一行。

错误示范

```
Some text
​```
Code block
​```
​```
Another code block
​```
Some more text
```

正确示范

```
Some text

​```
Code block
​```

​```
Another code block
​```

Some more text
```



16、文档中禁止出现裸露的 URL。如果希望用户能直接点击并打开该 URL，则使用一对尖括号 (<URL>) 包裹该 URL。如果由于特殊情况必须使用裸露的 URL，不需要用户通过点击打开，则使用一对反引号 (`URL`) 包裹该 URL。

错误示范

```
For more information, see https://www.example.com/.
```

正确示范

```
For more information, see <https://www.example.com/>.
```



17、使用加粗、斜体等强调效果时，在强调标识符内禁止出现多余的空格。如不能出现 `** 加粗文本 **`。

错误示范

```
Here is some ** bold ** text.

Here is some * italic * text.

Here is some more __ bold __ text.

Here is some more _ italic _ text.
```

正确示范:

```
Here is some **bold** text.

Here is some *italic* text.

Here is some more __bold__ text.

Here is some more _italic_ text.
```



18、单个反引号包裹的代码块内禁止出现多余的空格。如不能出现 ` 示例文本 `。

错误示范：

```
some text 
 some text
```

正确示范:

```
some text
```



19、链接文本两边禁止出现多余的空格。如不能出现 [ 某链接 ](https://www.example.com/)。

错误示范

```
[ a link ](https://www.example.com/)
```

正确示范:

```
[a link](https://www.example.com/)
```



20、链接必须有链接路径。如不能出现[空链接]()或[空链接](#)等情况。

错误示范

```
[an empty link]()

[an empty fragment](#)
```

正确示范:

```
[a valid link](https://example.com/)

[a valid fragment](#fragment)
```



21、文档中的代码块统一使用三个反引号进行包裹，禁止使用缩进四格风格的代码块。

错误示范：

```
Some text.

  # Indented code

More text.
```

正确示范

```
```ruby
# Fenced code
​```
More text.
```
