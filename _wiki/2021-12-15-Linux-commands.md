---
layout: wiki
title: "Linux 命令"
categories: Linux
description: 本人的命令积累笔记
keywords: Linux,command,命令,不完整
---

| 命令                        | 作用                                                         |
| --------------------------- | ------------------------------------------------------------ |
| --save-temps                | gcc保存编译过程中的中间文件                                  |
| mv test.txt wbk.txt         | 将test.txt重命名为wbk.txt                                    |
| mv /usr/udt/* .             | 将/usr/udt中的所有文件移动到当前目录                         |
| mv * ../                    | 将当前文件夹下的所有文件移动到上一级目录                     |
| mmv (-n) f\\* F\\#1         | 将所有以f开头的文件改成以F开头,中间的-n表示打印输出而不是重命名文件,用于重命名前检验一下。 |
| mmv (-n) \\*.c \\#1.txt     | 将后缀名为.c的后缀名全部修改为.txt                           |
| mmv (-n) '*abc\*' '#1xyz#2' | 将文件名中带有abc的文件的abc全部改为xyz,前后的字符数可以不相等 |
| mmv f\\* ..                 | 将所有以f开头的文件移动到上一级目录                          |
| man mmv                     | mmv的详细使用说明                                            |
| mv 文件名/* 另一个目录      | 把当前目录的一个子目录里的文件移动到另一个子目录里           |
| sudo su                     | 进入root                                                     |
| sudo passwd root            | root模式下修改root密码                                       |
| poweroff                    | 关机                                                         |

