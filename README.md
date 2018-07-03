### 马甲壳打包
        所谓马甲壳打包实则为多渠道打包，主要体现是同一套代码打包成多个app，各个app拥有自己的应用名、应用包名、应用启动图标等

### 多渠道打包
        主要通过gradle子节点productFlavors来配置渠道版本，关于多渠道打包详细介绍请自行了解，本例只做为一个基本介绍。
        ![](https://github.com/Wzhixiang/MaJiaKe/blob/master/device-2018-07-03-153156.png)
        添加渠道版本后同步项目（sync project），这个时候在Build Variant中就生成多渠道对应的版本
        ![](https://github.com/Wzhixiang/MaJiaKe/blob/master/device-2018-07-03-153156.png)

### 渠道版本信息
        applicationId 设置包名
        manifestPlaceholders 设置AndroidManiest.xml变量
        

### 效果
![](https://github.com/Wzhixiang/MaJiaKe/blob/master/device-2018-07-03-153156.png)