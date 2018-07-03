### 马甲壳打包
<br>所谓马甲壳打包实则为多渠道打包，主要体现是同一套代码打包成多个app，各个app拥有自己的应用名、应用包名、应用启动图标等</br>

### 如何实现
<br>1.在gradle子节点productFlavors中配置渠道版本（关于多渠道打包详细介绍请自行了解，本例只做为一个基本介绍）

![](https://github.com/Wzhixiang/MaJiaKe/blob/master/screenshot/TIM图片20180703155527.png)

applicationId 设置包名

manifestPlaceholders 设置AndroidManiest.xml中变量

移除defaultConfig中的applicationId，同步项目（sync project），这个时候在Build Variant中就生成多渠道对应的版本
        
![](https://github.com/Wzhixiang/MaJiaKe/blob/master/screenshot/TIM图片20180703155400.png)

2.在src目录下新建一个以渠道版本名文件夹，并添加资源文件（因为Android编译时会以渠道版本引用资源文件，和res引用资源文件类似），从而达到控制渠道版本特有样式
![](https://github.com/Wzhixiang/MaJiaKe/blob/master/screenshot/TIM图片20180703161922.png)
        
（ps：渠道版本特征有多种实现方式，这里只介绍本人觉得比较便捷、浅显易懂方式）</br>
        
### 效果
![](https://github.com/Wzhixiang/MaJiaKe/blob/master/screenshot/device-2018-07-03-153156.png)