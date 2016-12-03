# [jjdxm_alipay][project] #

## Introduction ##
针对支付宝提供移动支付SDK进行在线打包，上传到jcenter中心，方便在项目中快速接入，只需要使用compile命令就可以进行依赖

官方sdk下载地址：[https://doc.open.alipay.com/doc2/detail.htm?treeId=54&articleId=104509&docType=1](https://doc.open.alipay.com/doc2/detail.htm?treeId=54&articleId=104509&docType=1)

## Screenshots ##

<img src="https://raw.githubusercontent.com/jjdxmashl/jjdxm_alipay/master/screenshots/icon01.png" width="300"> 
<img src="https://raw.githubusercontent.com/jjdxmashl/jjdxm_alipay/master/screenshots/icon02.png" width="300"> 

## Download ##

[demo apk下载][downapk]

[下载最新版本aar][lastaar]

Download or grab via Maven:

	<dependency>
	  <groupId>com.dou361.alipay</groupId>
	  <artifactId>jjdxm-alipay</artifactId>
	  <version>x.x.x</version>
	</dependency>

or Gradle:

	compile 'com.dou361.alipay:jjdxm-alipay:x.x.x'

历史版本

    compile 'com.dou361.alipay:jjdxm-alipay:1.0.1'   //alipaySdk-20160825.jar 支付宝2.0
    compile 'com.dou361.alipay:jjdxm-alipay:1.0.0'   //alipaySdk.jar、alipaysecsdk.jar、alipayutdid.jar


jjdxm-alipay requires at minimum Java 9 or Android 2.3.


[架包的打包引用以及冲突解决][jaraar]

## Proguard ##

根据你的混淆器配置和使用，您可能需要在你的proguard文件内配置以下内容：

	-libraryjars libs/alipaySDK-20150602.jar
	
	-keep class com.alipay.android.app.IAlixPay{*;}
	-keep class com.alipay.android.app.IAlixPay$Stub{*;}
	-keep class com.alipay.android.app.IRemoteServiceCallback{*;}
	-keep class com.alipay.android.app.IRemoteServiceCallback$Stub{*;}
	-keep class com.alipay.sdk.app.PayTask{ public *;}
	-keep class com.alipay.sdk.app.AuthTask{ public *;}

## Get Started ##

注册权限

	<uses-permission android:name="android.permission.INTERNET"/>
    <uses-permission android:name="android.permission.ACCESS_NETWORK_STATE"/>
    <uses-permission android:name="android.permission.ACCESS_WIFI_STATE"/>
    <uses-permission android:name="android.permission.READ_PHONE_STATE"/>
    <uses-permission android:name="android.permission.WRITE_EXTERNAL_STORAGE"/>

在商户应用工程的AndroidManifest.xml文件里面添加声明：

	<activity
            android:name="com.alipay.sdk.app.H5PayActivity"
            android:configChanges="orientation|keyboardHidden|navigation|screenSize"
            android:exported="false"
            android:screenOrientation="behind"
            android:windowSoftInputMode="adjustResize|stateHidden">
        </activity>
        <activity
            android:name="com.alipay.sdk.app.H5AuthActivity"
            android:configChanges="orientation|keyboardHidden|navigation"
            android:exported="false"
            android:screenOrientation="behind"
            android:windowSoftInputMode="adjustResize|stateHidden">
        </activity>

开始使用
集成流程可以参考支付宝的官方文档

[https://doc.open.alipay.com/docs/doc.htm?spm=a219a.7629140.0.0.csxZPs&treeId=193&articleId=105296&docType=1](https://doc.open.alipay.com/docs/doc.htm?spm=a219a.7629140.0.0.csxZPs&treeId=193&articleId=105296&docType=1)

## More Actions ##

## ChangeLog ##

## About Author ##

#### 个人网站:[http://www.dou361.com][web] ####
#### GitHub:[jjdxmashl][github] ####
#### QQ:316988670 ####
#### 交流QQ群:548545202 ####


## License ##

    Copyright (C) dou361, The Framework Open Source Project
    
    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at
    
     	http://www.apache.org/licenses/LICENSE-2.0
    
    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.

## (Frequently Asked Questions)FAQ ##
## Bugs Report and Help ##

If you find any bug when using project, please report [here][issues]. Thanks for helping us building a better one.



[web]:http://www.dou361.com
[github]:https://github.com/jjdxmashl/
[project]:https://github.com/jjdxmashl/jjdxm_alipay/
[issues]:https://github.com/jjdxmashl/jjdxm_alipay/issues/new
[downapk]:https://raw.githubusercontent.com/jjdxmashl/jjdxm_alipay/master/apk/app-debug.apk
[lastaar]:https://raw.githubusercontent.com/jjdxmashl/jjdxm_alipay/master/release/jjdxm-alipay-1.0.0.aar
[lastjar]:https://raw.githubusercontent.com/jjdxmashl/jjdxm_alipay/master/release/jjdxm-alipay-1.0.0.jar
[icon01]:https://raw.githubusercontent.com/jjdxmashl/jjdxm_alipay/master/screenshots/icon01.png
[icon02]:https://raw.githubusercontent.com/jjdxmashl/jjdxm_alipay/master/screenshots/icon02.png
