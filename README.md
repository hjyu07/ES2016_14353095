# ES2016_14353095
# Lab1 README
## Description
分布式操作层（DOL）是一个用来运行并行应用的软件开发框架。DOL允许指定基于应用Kahn进程网络模型的计算，它的特点是基于SystemC仿真引擎。此外，DOL提供了基于XML规范的格式来描述一个多处理器系统上的并行应用程序的实现，包括结合和映射。 
## Install DOL
1. 配置ubuntu环境
2. 下载systemc-2.3.1.tgz和dol.ethz.zip
3. 解压文件  
    新建dol的文件夹  
    ` mkdir dol`  
    将dolethz.zip解压到dol文件夹中  
    `unzip dol_ethz.zip -d dol`
    解压systemc
    `tar -zxvf systemc-2.3.1.tgz`  
4. 编译systemc  
   解压后进去systemc-2.3.1的目录  
   `cd systemc-2.3.1`  
   新建一个临时文件夹objdir  
   `mkdir objdir`  
   进入该文件夹  
   `cd objdir`  
   运行configure  
   `../configure CXX=g++ --disable-async-updates`  
   运行后的截图为：  
   ![img1](https://cl.ly/2c461p062a2Q/img1.png)  
  编译  
  `sudo make install`  
  编译完后的文件目录为：  
  ![img2](https://cl.ly/1b2b043t1R0j/img2.png)  
  记录当前的工作路径：  
  ![img3](https://cl.ly/3r3Q3V0m403K/img3.png)  
5. 编译dol  
    进入dol的文件夹，修改build_zip.xml文件为：  
    ![img4](https://cl.ly/1W2o1v3l3Q1t/img4.png)  
    编译  
    `ant -f build_zip.xml all`  
    ![img5](https://cl.ly/0P3r2F1u3V3e/img5.png)  
    运行第一个例子  
    `cd build/bin/main`  
    `ant -f runexample.xml -Dnumber=1`  
    运行结果为：  
    ![img6](https://cl.ly/1p3Q1m2g000N/img6.png)  
    
## Experimental experience
第一次配置的时候忘记安装java环境，导致最后出了一点问题，安装之后就好了。写这份文档的时候为了截图又重新配置一次环境，发现在最后一步的时候build fail， 出现Unable to find a javac complier。试了网上很多方法都不成功，可能是在云计算实验课上配置环境的时候更改到了什么地方，又重新安装一遍系统。
