---
layout: post
title: "第一周C语言力扣题"
categories: C
description: 游戏部布置的第一周的Leetcode题
keywords: leetcode,刷题
---

# 罗马数字转阿拉伯数字

  这是一道力扣的简单题，但以我数组和指针都没学过临时看了一下数组的水平，实际上是很有难度的。

  好在我室友有一个数组指针都学了的，所以在他的帮助下，我还是成功写出来了(计算阿拉伯数字是我自己设计的，他教了我怎么求数组的元素数目。)

  首先这一题先要求数组的元素个数，后面才好设计循环结构来将罗马数字变成阿拉伯数字  

`int romanToInt(char * s)
{
    int n=0, ret=1, i=0, number=0;
    while(ret==1)
    {
        n++;
        ret = scanf("%c",&s[n]);
    }
    while(i<=n)
    {
        if(s[i]== 'I'&&(s[i+1]=='V'||s[i+1]=='X'))
            number--;
        else if(s[i]== 'I')
             number++;
        if(s[i]== 'V')
                number += 5;
        if(s[i]== 'X'&&(s[i+1]== 'L'||s[i+1]== 'C'))
            number -= 10;
        else if(s[i]== 'X')
            number += 10;
        if(s[i]=='L')
            number += 50;
        if(s[i]=='C'&&(s[i+1]=='D'||s[i+1]=='M'))
            number -= 100;
        else if(s[i]='C')
            number += 100;
        if(s[i]== 'D')
            number += 500;
        if(s[i]== 'M')
            number += 1000;                             
            
        

    }
    return 0;

}`