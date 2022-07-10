# 基础工具



## 前述

1、本篇仅对文件管理中功能性、综合性、使用率更强更高的工具进行讲解。

2、本篇内容仅限于清晰明确理解格式及语法，命令选项满足于一般的工作需要。详情可阅读官方手册。

3、本文不对涉及到的正则表达式进行讲解，有时间单独开篇。



## 正篇

##### Grep

###### 概述

1、简述：prints lines that contain a match for one or more patterns.

2、官方地址：https://www.gnu.org/software/grep/manual/grep.html

3、基本格式：grep [option...] [patterns] [file...]

###### 选项

1、-i ：  Ignore case distinctions in both the PATTERN and the input files.（不区分大小写）

2、-v ：Invert the sense of matching, to select non-matching lines.（反选）

3、-A NUM ： Print NUM lines of trailing context after matching lines.（输出指定行及指定行之后的NUM行）

4、-B NUM ： Print NUM lines of leading context before matching lines. （输出指定行及指定行之前的NUM行）

5、-C NUM, -NUM ： Print  NUM  lines  of  output context. （输出指定行及指定行前后各NUM行）

6、-r ： Read all files under each directory, recursively, following symbolic links only if they are on the command line. （递归读取目录下每个文件） 

7、-R ：Read all files under each directory, recursively.  Follow all symbolic links, unlike -r.（递归读取目录下每个文件，-r于-R区别请读左侧）

8、-n ： Prefix each line of output with the 1-based line number within its input file. （显示行号）

9、-c ： Suppress normal output; instead print a count of matching lines for each input file.（输出匹配到的行数）

![grep选项](grep选项.png)

##### Sed

###### 概述

1、简述：Sed is a stream editor. 

2、官方手册：https://www.gnu.org/software/sed/manual/sed.html

3、基本格式：sed OPTIONS... [SCRIPT] [INPUTFILE...]

###### 选项

1、-f script-file ： Add the commands contained in the file script-file to the set of commands to be run while processing the input.

2、-i[SUFFIX] ： This option specifies that files are to be edited in-place. 

3、-n ： These options disable this automatic printing, and sed only produces output when explicitly told to via the p command.

###### script

1、Syntax ： [addr]X[options]

【1】X ： X is a single-letter sed command. 

【2】[addr] ：  [addr] is an optional line address.If [addr] is specified, the command X will be executed only on the matched lines. 

【3】[options] ： Additional [options] are used for some sed commands.

2、Address

【1】Numeric Addresses

- number ： Specifying a line number will match only that line in the input.
- $ ： This address matches the last line of the last file of input, or the last line of each file when the -i or -s options are specified.
- first~step ： This GNU extension matches every stepth line starting with line first.

【2】Regexp Addresses

- /regexp/
- \%regexp%
- /regexp/I
- \%regexp%I
- /regexp/M
- \%regexp%M

【3】Range Addresses ： An address range can be specified by specifying two addresses separated by a comma (,).

3、Commands

【1】=

【2】a text ： Append text after a line.(另有互相替代的语法参照手册)

【3】c text ： Replace (change) lines with text.

【4】i text ： insert text before a line

【5】d ： Delete the pattern space; immediately start next cycle.

【6】p ： Print the pattern space.

【7】l ： Print the pattern space in an unambiguous form.

【8】s/regexp/replacement/[flags]

- flags ： g

【9】{ cmd ; cmd ... } ： Group several commands together.

##### Gawk（awk）

###### 概述

2、官方手册：https://www.gnu.org/software/gawk/manual/html_node/index.html

3、基本格式

【1】 gawk [ POSIX or GNU style options ] -f program-file [ -- ] file ...

【2】pgawk [ POSIX or GNU style options ] -f program-file [ -- ] file ...

【3】gawk [ POSIX or GNU style options ] [ -- ] program-text file ...

【4】pgawk [ POSIX or GNU style options ] [ -- ] program-text file ...

###### options

###### program-text

1、Syntax

【1】[pattern]  { action }

【2】pattern  [{ action }]

【3】function name(args) { … }

2、Patterns

【1】Regexp Patterns

【2】Expression Patterns

【3】Ranges

【4】BEGIN/END

【5】BEGINFILE/ENDFILE

【6】Empty

3、Actions

【1】简述

- An action consists of one or more awk statements, enclosed in braces (‘{…}’). 
- Each statement specifies one thing to do. 
- The statements are separated by newlines or semicolons.

【2】statements

- Expressions
- Control Statements
- Compound statements
- Input statements
- Output statements
- Deletion statements

4、Expressions（这个部分与官方手册次序有所改动，详情请参照官方手册）

【1】Constant Expressions

【2】Regular Expression Constants

【3】Variables

【4】Operators

【5】Truth Values and Conditions

【6】Function Calls

5、Functions

【1】Numeric Functions

【2】String Functions

【3】Time Functions

【4】Type Function

【5】Bit Manipulations Functions

【6】Internationalization Functions

【7】USER-DEFINED FUNCTIONS

【8】YNAMICALLY LOADING NEW FUNCTIONS

6、Arrays





