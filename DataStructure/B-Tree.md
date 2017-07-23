# B树
## 什么是B树？
B树是一种树形的数据结构，经常被写为B- Tree，当然有B- Tree就有B+ Tree。树形的数据结构是一种非常适合与搜索相关的算法实现的数据结构，最典型的应用场景就是数据库的索引。

## 数据库的索引为什么要使用B- Tree?
当了解到数据库的索引是用B- Tree的数据结构时，很多人可能会有疑问，为什么要用B- Tree，为什么不直接用数组，为什么不用二叉树，甚至为什么不直接用链表？其实从算法的时间复杂度来说二叉树已经非常好了（O（logN）），但是对于数据库的索引来说，它是需要存储到硬盘上，一旦存储到了硬盘上，IO问题就是一个大问题，并且影响效率的就不再是算法的效率而是IO所消耗的时间。每次IO的时间只能通过硬件来解决，软件控制不了，所以，只能从IO的查找次数下手了，二叉树找到目标需要10此IO，而B- Tree需要<10次IO，这就有足够的理由选择B- Tree。

## B-Tree的原理
对于搜索树这种数据类型来说，影响其比较次数的就是树的高度，所以如果想减少IO的次数，可以通过降低树的高度来实现，B-树的基本原理就是这样。

一个m阶的B树具有如下几个特征：
1. 根节点至少有两个子女
2. 每个中间节点都包含k-1个元素和k个孩子，其中m/2<=k<=m
3. 每一个叶子节点都包含k-1个元素，其中m/2<=k<=m
4. 所有的叶子节点都位于同一层
5. 每个节点的元素从小到大排序，节点当中k-1个元素正好是k个孩子包含的元素的值域的划分

## B-的查找
第1次磁盘IO：

![](http://upload-images.jianshu.io/upload_images/1975419-d3041b0215c42148?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

在内存中定位（和9比较）：

![](http://upload-images.jianshu.io/upload_images/1975419-a3953a5f3a618078?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

第2次磁盘IO：

![](http://upload-images.jianshu.io/upload_images/1975419-02072bdd25eed2b5?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

在内存中定位（和2，6比较）：

![](http://upload-images.jianshu.io/upload_images/1975419-530b47ac087b1e81?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

第3次磁盘IO：

![](http://upload-images.jianshu.io/upload_images/1975419-7beb51451f650442?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

在内存中定位（和3，5比较）：

![](http://upload-images.jianshu.io/upload_images/1975419-c6567e2f52bd7359?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

## B-插入节点
插入4
自顶向下查找4的节点位置，发现4应当插入到节点元素3，5之间。

![](http://upload-images.jianshu.io/upload_images/1975419-735fd0910ba71ed5?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

节点3，5已经是两元素节点，无法再增加。父亲节点 2， 6 也是两元素节点，也无法再增加。根节点9是单元素节点，可以升级为两元素节点。于是**拆分**节点3，5与节点2，6，让根节点9升级为两元素节点4，9。节点6独立为根节点的第二个孩子。

![](http://upload-images.jianshu.io/upload_images/1975419-aa87aa954404f186?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

## B-删除节点
自顶向下查找元素11的节点位置。

![](http://upload-images.jianshu.io/upload_images/1975419-9c8fb0c0981905a9?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

删除11后，节点12只有一个孩子，不符合B树规范。因此找出12,13,15三个节点的中位数13，取代节点12，而节点12自身下移成为第一个孩子。（这个过程称为**左旋**）

![](http://upload-images.jianshu.io/upload_images/1975419-6b8481b474d4c420?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

![](http://upload-images.jianshu.io/upload_images/1975419-084b797a85fe44f3?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

该数据结构广泛的应用于文件系统的索引和数据库的索引，如MongoDb,其实从本质上来说，该数据结构就是针对于和IO操作比较频繁的应用场景做出的优化，通过增加内存中的数据量，来提高效率。