### 源码：
docs文件夹里是源码，就一个 index.html 文件

### 演示地址：

https://liu-shichao.github.io/musical-alphabet/

### 使用说明：

1. 目前只试过在 win11 谷歌浏览器 下运行。

2. 使用方法：随便选一个按键，回忆是什么音名，然后单击那个按键，显示音名进行对照。

3. 快捷键 d 可以 （显示 / 隐藏） 全部音名。

### 代码解释：

1. 使用 html 中的 ``<div>`` 元素作为钢琴块；
2. 白键使用 css 中的 float 样式，从左向右依次排列，这里指定父元素的高度，来清除后续元素的浮动，同时父元素设置为相对定位，配合黑键的绝对定位（子绝父相）；
3. 黑键采用绝对定位，计算每个黑键的偏移量，覆盖在白键上方，需要注意绝对定位需要自己指定宽度，不然默认会为0；
4. 每个键的内部又嵌套了两个``<div>``元素，用来显示建上的音名；
5. 使用``css:active``选择器控制音名的透明度，实现显示隐藏的控制
6. 绑定电脑键盘 d 键的按下事件，当按下时使用``toggleClass``为音名添加或去除``showName``类名，匹配样式，通过样式设置透明度为不透明进行显示；
7. 音名中降号符号输入法一直没能打出来，是从网上找了一个直接复制粘贴过去的。

### 参考：
1. https://gitcode.com/mirrors/inanyworld/javascript-piano/tree/main
2. 【零基础学音乐·自学乐理】5-音名、钢琴键盘: https://www.bilibili.com/video/BV1Ay4y1r7JF/?spm_id_from=333.788&vd_source=55a350b8650fa259fcd33c6529c36cf5