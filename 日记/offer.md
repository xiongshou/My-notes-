# 算法题

## 树的后继有左子树

![image-20210109153523602](https://tva1.sinaimg.cn/large/008eGmZEly1gmhhd7snogj30p606egm8.jpg)

## 找出数组中重复数字

​		依据i==nums【i】进行swap交换，先while交换，然后判断

## 旋转数组的最小值

![image-20210109163853743](https://tva1.sinaimg.cn/large/008eGmZEly1gmhj7auatwj30sm0dg753.jpg)

## dfs跑图

![image-20210109171002021](https://tva1.sinaimg.cn/large/008eGmZEly1gmhk3o2y62j30im08ymxo.jpg)

## 剪绳子

凑最多的3，剩下凑余数为1（凑数1+3=4），余数为2（2）

## 删除链表中重复节点

写一条新链，首部为-1。用p来维护链表

每次while（p->next)

找见p、q中间隔几个，隔一个的话，p顺位走一个

隔好多个，p跳过中间隔的p->next=q;

![image-20210109193330467](/Users/xiongshou/笔记/日记/image-20210109193330467.png)

## 合并链表

要注意最后p要next走

