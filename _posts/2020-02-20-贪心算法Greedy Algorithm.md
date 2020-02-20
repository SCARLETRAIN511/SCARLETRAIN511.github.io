---
layout:     post
title:      贪心算法笔记
subtitle:   coursera课程 第二周笔记
date:       2020-02-20
author:     JiaxuanTang
header-img: img/post-bg1.jpg
catalog: true
tags:
    - Python
    - 算法
    - 学习笔记
---

# This post is talking about greedy algorithms

#### Notes from course Data Structure and algorithms from coursera
----------
**Typical Example**

Use python do make the script
```python
def solution(NumberList):
    NumberList.sort(reverse = True)
    MaxNum = ""
    for i in NumberList:
        MaxNum += str(i)
    MaxNum = int(MaxNum)
    return MaxNum

#递归解法

def efficient(NumberList):
    MaxNum = ""
    if len(NumberList) == 0:
        return ""
    else:
        maxNow = max(NumberList)
        MaxNum += str(maxNow)
        pos = NumberList.index(maxNow)
        NumberList.pop(pos)
        return MaxNum + efficient(NumberList)


if __name__ == "__main__":
    #use this list as an example

    print(solution([1,2,3,5,1,3,8]))
    print(efficient([1,2,3,4,5,5,5]))

```