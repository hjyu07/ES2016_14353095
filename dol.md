#example1
## .dot截图
![img1](http://oficjb2g0.bkt.clouddn.com/ex1_dot.png)
## 实验过程
1. 删除已经运行过的example1文件
1. 进入dol/examples/example1
1. 修改square.c文件，如下，读square的端口“PORT_IN"，将值读到i，i=i*i*i, 输出其三次方数       
     ![img2](http://oficjb2g0.bkt.clouddn.com/ex1_square.png)
1. 运行结果：输出三次方数![img3](http://oficjb2g0.bkt.clouddn.com/ex1.png)

#example2
## .dot截图
![img4](http://oficjb2g0.bkt.clouddn.com/ex2_dot.png)
## 实验过程
1. 进入dol/examples/example2
1. 修改xml文件的iterator，使其只迭代两次，如下图所示 
![img5](http://oficjb2g0.bkt.clouddn.com/ex2_generate.png)
1. 运行结果：使square模块变为两个![img6](http://oficjb2g0.bkt.clouddn.com/ex2.png)

# 实验感想
本次实验的基础知识在课堂上讲解得非常详细，理解起来比较简单，实验过程中的主要问题是删不了已经运行过的example文件，后来翻看群记录，加上了
`sudo chown -R (username) dol/build/bin/main/exampex1`
就可以去掉文件夹上的锁了。
