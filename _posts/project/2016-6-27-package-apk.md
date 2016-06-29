---
layout: post
title: 在Android整合百度地图应用  
category: project
description:HowToDo
---
### 在Android整合百度地图应用  
　　零、前言  
　　在我们Android项目中很多都用到了地图应用，和PC上的地图相比，移动端地图能够随时随地的查看，并且轻松构建出行路线，使用起来明显更加的方便。在手机地图领域做得最好的当数百度地图和谷歌地图了，并且这两种地图都提供了丰富的API,任何开发者都能够轻松地将地图功能引入到自己的应用程序中，由于墙的原因建议使用百度地图。您可以按照如下步骤在项目中使用百度地图。  
　　一、申请API key  
　　没有注册百度账号，具体的流程首先参照[百度地图官方API](http://lbsyun.baidu.com/index.php?title=android-locsdk/guide/key)。  
　　在申请API Key的时候注意事项：  
　　　1、需要你的应用的包名，以XXX项目为例在AndroidManifest.xml中的“package="com.test.demo"”。  
　　　2、SHA1获取（猜测为测试版本的key）:a、eclipse开发windows -> preferance -> android -> build,你就可以看到SHA1的值。b、Android studio 开发 **待完善**。  
　　　3、SHA2获取(猜测为正式版本的key):a、eclipse开发在打包的最后一步会生成一个SHA1。b、Android studio 开发 **待完善。**   

　　二、在完成输入后你会获取到一个Key值。这个key值就是你在Android项目中使用的在AndroidManifest.xml中添加如下代码:
```
<application
   <!--添加KEY-->
  <meta-data  
    android:name="com.baidu.lbsapi.API_KEY"   
    android:value="你生成的KEY值" />
   <!--注册百度地图服务-->
  <service  
    android:name="com.baidu.location.f"  
    android:enabled="true"  
    android:process=":remote"/>  
</application>
```
　　三、QAQ  
　　1、问题：在测试机器有地图打包之后地图不显示：SHA1和SHA2获取值不对。  
　　2、待补充。 
 
参考书籍《第一行代码》