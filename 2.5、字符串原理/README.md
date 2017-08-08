## 字符串原理


### 不顾一切找Frank

老式自动点歌机上的歌太多了，人们找不到他们要听的。为了帮助顾客，Head Fisrt酒吧的伙计希望你再写一个程序。
歌曲清单如下：

*新专辑《鲜为人知的Sinatra》中的歌曲*
```

I left my heart in harvard med school.
Newark Newark a wonderfull town
Dancing with a dork
From here to maternity
The girl from Iwo Jima
    ^-----------------------伙计说未来还有更多歌曲，但每首歌的标题不超过79个字符
```
这只是前面几首歌，这张歌单还有可能变长。你需要写一个C程序，要求用户输入想找的歌名，搜索所有的歌曲，显示匹配的曲目。
    

### 创建数组的数组

你需要记录几首歌的名字。可以一次用数组记录几件事。但别忘了，字符串本身就是一个数组，也就是说需要创建数组的数组。
```
char tracks[][80] = {
    "I left my heart in harvard med school",
    "Newark Newark a wonderfull town",
    "Dancing with a dork",
    "From here to maternity",
    "The girl from Iwo Jima"
}
```
也就是说，为了找到某一首歌的名字，可以这样写：
```
tracks[4]  ---> "The girl from Iwo Jima"
```
如果想读取字符串中的某个字符：
```
tracks[4][6]  ---> "r"
```
### 找到包含搜索文本的字符串

酒吧的那伙人给了你一个程序说明说：让用户输入要找的歌曲。循环遍历所有的歌名。如果歌名包含搜索文本，就显示出来。

+ 使用string.h

### 使用strstr()函数
