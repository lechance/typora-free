# Typora 最后免费版本也不能用了？简单一招搞定

小牛呼噜噜

2022年8月2日

typora百宝箱

![img](http://image-upload-xiaoniuhululu.oss-cn-shanghai.aliyuncs.com/img/Snipaste_2022-08-01_20-29-21.png?x-oss-process=style/xiaoniuhululu)

> 作者：小牛呼噜噜

------

Typora是一款优秀的 Markdown 编辑器和阅读器

去年Typora还是免费的，今年的新版开始收费了，不过还是能理解的 当时摸了摸口袋

![img](http://image-upload-xiaoniuhululu.oss-cn-shanghai.aliyuncs.com/img/7a3eb89e-ae3c-49f4-b2ff-933ee4fde47b.png)

还是不选择升级了，就一直用的`Typora-0.11.18`版本，老就老一点吧，能用就行

> 公众号回复：**Typora-0.11.18**,即可获得最后免费版本Typora-0.11.18

但是最近发现最后的免费版本竟然也用不了，可能提前预知大家都不愿意升级 ，官方埋了个必须强制升级的雷，这个操作可太骚了！

![img](http://image-upload-xiaoniuhululu.oss-cn-shanghai.aliyuncs.com/img/image-20220729232614138.png?x-oss-process=style/xiaoniuhululu#crop=0&crop=0&crop=1&crop=1&id=niRjG&originHeight=177&originWidth=826&originalType=binary&ratio=1&rotation=0&showTitle=false&status=done&style=none&title=)

检索了下目前网上主要这几种方式：

1. 重新安装老版本，试了一下，还是这个强制升级的提示
2. 修改系统时间可以，但是系统时间很重要，恢复正常时间还是不行，鸡肋
3. 替换app.asar文件，搞了半天，也没效果，删了
4. 使用网友给的**winmm.dll，**来爆破收费版本，没成功，网上不明安装包，还有点危险

没办法，好好地研究一下typora的注册表，一般权限都和注册表有点关系。

> 注册表其实就是软件安装在win系统里面的配置文件,弄了个好听的名字

先打开typora的注册表看看，里面是什么情况

1. 打开注册表：按`Windows+R`打开运行窗口，输入` regedit`
2. 进入路径`计算机\HKEY_CURRENT_USER\SOFTWARE\Typora`

![img](http://image-upload-xiaoniuhululu.oss-cn-shanghai.aliyuncs.com/img/image-20220729233015019.png?x-oss-process=style/xiaoniuhululu#crop=0&crop=0&crop=1&crop=1&id=dkhFd&originHeight=906&originWidth=1620&originalType=binary&ratio=1&rotation=0&showTitle=false&status=done&style=none&title=)

我们可以发现，里面竟然有个时间`IDate`，那岂不是我们把时间给改了，那就不过期了？ 赶紧试试 果然修改后发现再次打开Typora, 还是不行，但时间竟然还是恢复`4/20/2022`。不信了，再多试几次 好吧，还是这个结果![img](http://image-upload-xiaoniuhululu.oss-cn-shanghai.aliyuncs.com/img/7cfa4369-c43a-43af-927d-7cec8fad7ff6.png#crop=0&crop=0&crop=1&crop=1&id=tBRLc&originHeight=240&originWidth=240&originalType=binary&ratio=1&rotation=0&showTitle=false&status=done&style=none&title=)

但也不是没有收获， 我们可以判断每次打开Typora，它会重置注册表中时间。那很有可能这个**注册表里的时间** 再加上**当前系统时间**来实现 `Typora Beta强制过期`的效果。不然Typora为什么会在启动时，一遍遍地**重置**这个**注册表里的时间** 呢？其中必有猫腻![img](http://image-upload-xiaoniuhululu.oss-cn-shanghai.aliyuncs.com/img/f5d472ba-a812-11ec-9007-0242ac110003.png#crop=0&crop=0&crop=1&crop=1&id=BFuef&originHeight=82&originWidth=81&originalType=binary&ratio=1&rotation=0&showTitle=false&status=done&style=none&title=)笔者立刻就试试看：Typora不是每次打开都**重置注册表里的时间，** 那我们就阻止这种行为？我们通过修改当前系统用户权限，让其无权限修改该注册表！![img](http://image-upload-xiaoniuhululu.oss-cn-shanghai.aliyuncs.com/img/image-20220729233305236.png?x-oss-process=style/xiaoniuhululu_black#crop=0&crop=0&crop=1&crop=1&id=YWwVm&originHeight=907&originWidth=1878&originalType=binary&ratio=1&rotation=0&showTitle=false&status=done&style=none&title=)

我们再打开一下，神奇的一幕：![img](http://image-upload-xiaoniuhululu.oss-cn-shanghai.aliyuncs.com/img/image-20220729233403718.png?x-oss-process=style/xiaoniuhululu#crop=0&crop=0&crop=1&crop=1&id=TYXh3&originHeight=870&originWidth=966&originalType=binary&ratio=1&rotation=0&showTitle=false&status=done&style=none&title=)

这样一下就解决问题了，还不需要下载额外的破解文件，分外优雅！![img](http://image-upload-xiaoniuhululu.oss-cn-shanghai.aliyuncs.com/img/8cafbabe0c6e61b476595fd31cd6b729a7bcd79e.png#crop=0&crop=0&crop=1&crop=1&id=LntCc&originHeight=384&originWidth=384&originalType=binary&ratio=1&rotation=0&showTitle=false&status=done&style=none&title=)

最后本文仅供学习参考之用，有条件的还是去支持一下正版
