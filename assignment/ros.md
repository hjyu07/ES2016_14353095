#ROS配置
##配置过程
1. 配置Ubuntu软件仓库
1. 添加sources.list和keys
![img1](http://oficjb2g0.bkt.clouddn.com/1.png)
1. 安装桌面完整版 
   `sudo apt-get install ros-jade-desktop-full`
1. 初始化rosdep
    ![img2](http://oficjb2g0.bkt.clouddn.com/2.png)
1. 环境配置
    ![img3](http://oficjb2g0.bkt.clouddn.com/3.png)
1. 安装rosinstall
    `sudo apt-get install python-rosinstall`
##查看环境变量
   `export | grep ROS`
   
   ![img4](http://oficjb2g0.bkt.clouddn.com/4.png)
   
## 实验感想
ROS的配置比较顺利，但是配置cartographer的时候遇到了很多问题，先是尝试了google上的方法，配置到`catkin_make_isolated --install --use-ninja`这一步的时候就失败了。后来尝试中文博客上的做法，配置到`make –j3`这一步也一直不成功。