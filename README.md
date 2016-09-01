# [jjdxm_alipay][project] #

## Introduction ##
社会化第三方登录、分享实现流程

## Screenshots ##

<img src="https://raw.githubusercontent.com/jjdxmashl/jjdxm_alipay/master/screenshots/icon01.png" width="300"> 
<img src="https://raw.githubusercontent.com/jjdxmashl/jjdxm_alipay/master/screenshots/icon02.png" width="300"> 

## Download ##

[demo apk下载][downapk]

[下载最新版本aar][lastaar]

Download or grab via Maven:

	<dependency>
	  <groupId>alipay</groupId>
	  <artifactId>jjdxm-alipay</artifactId>
	  <version>x.x.x</version>
	</dependency>

or Gradle:

	compile 'alipay:jjdxm-alipay:x.x.x'

历史版本

    compile 'alipay:jjdxm-alipay:1.0.1'   //alipaySdk-20160825.jar
    compile 'alipay:jjdxm-alipay:1.0.0'   //alipaySdk.jar、alipaysecsdk.jar、alipayutdid.jar


jjdxm-alipay requires at minimum Java 15 or Android 4.0.

## Get Started ##

支付宝2.0


混淆参考

    -dontshrink
    -dontpreverify
    -dontoptimize
    -dontusemixedcaseclassnames

    -flattenpackagehierarchy
    -allowaccessmodification
    -printmapping map.txt

    -optimizationpasses 7
    -verbose
    -keepattributes Exceptions,InnerClasses
    -dontskipnonpubliclibraryclasses
    -dontskipnonpubliclibraryclassmembers
    -ignorewarnings

    -keep public class * extends android.app.Activity
    -keep public class * extends android.app.Application
    -keep public class * extends android.app.Service
    -keep public class * extends android.content.BroadcastReceiver
    -keep public class * extends android.content.ContentProvider
    -keep public class * extends java.lang.Throwable {*;}
    -keep public class * extends java.lang.Exception {*;}

    -libraryjars libs/alipaySDK-20150610.jar

    -keep class com.alipay.android.app.IAlixPay{*;}
    -keep class com.alipay.android.app.IAlixPay$Stub{*;}
    -keep class com.alipay.android.app.IRemoteServiceCallback{*;}
    -keep class com.alipay.android.app.IRemoteServiceCallback$Stub{*;}
    -keep class com.alipay.sdk.app.PayTask{ public *;}
    -keep class com.alipay.sdk.app.AuthTask{ public *;}


    -keepclasseswithmembernames class * {
        native <methods>;
    }

    -keepclasseswithmembers class * {
        public <init>(android.content.Context, android.util.AttributeSet);
    }

    -keepclasseswithmembers class * {
        public <init>(android.content.Context, android.util.AttributeSet, int);
    }

    -keepclassmembers class * extends android.app.Activity {
       public void *(android.view.View);
    }

    -keepclassmembers enum * {
        public static **[] values();
        public static ** valueOf(java.lang.String);
    }

    -keep class * implements android.os.Parcelable {
      public static final android.os.Parcelable$Creator *;
    }

    # adding this in to preserve line numbers so that the stack traces
    # can be remapped
    -renamesourcefileattribute SourceFile
    -keepattributes SourceFile,LineNumberTable

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
