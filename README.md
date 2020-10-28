# JCSDK-iOS
## Introduction to JCSDK

JCSDK is a set of advertising SDK provided by MS Company, which integrates the advertising SDKs of major advertisers and related statistical SDKs to facilitate the joint operation and data analysis of in-app advertising between platforms.

Ad types supported:

splash Ads、banner Ads、rewardVideo Ads、intersitial Ads、native Ads
 
 ## 资源文件
<details>
<summary>中文</summary>

### 请勿将iOS需要用到的SDK（包括.a、.framework及.embededframework格式的套件）下载或传送至Windows操作系统上，因为Windows文件系统会修改这些SDK，导致它们在Xcode中无法编译。

## 接入JCSDK所需的额外支持库 和 相关文件
[DataCollection_SDK](https://github.com/Romambo/DataCollection_SDK)数据统计相关库

[ADThirdParty_SDK](https://github.com/Romambo/ADThirdParty_SDK)第三方广告库

## 对接文档
[1.0.0](https://github.com/Romambo/JCSDK_DocumentFile)

## Unity桥接文件
[unityBridge](https://github.com/Romambo/JCSDK_DocumentFile/blob/main/IOS_UnityBridge.zip)

## 版本记录

<details>
<summary>1.0.0</summary>

支持开发者工具: Xcode 11
</details>
 
<details>
<summary>2.0.0</summary>

支持开发者工具: Xcode 12  
**更新内容**  
>1.新增了流量组和连续展示功能逻辑、升级内部广告接口 V4 -> V5  
>2.新增 "kochava" and "tenjin" 数据统计平台  
>3.修改了unity使用者需要接入的OC初始化接口. 详情见: JC_unityAdApi.h
```
旧代码
//-(void)initJCSDKWithLog:(BOOL)isOpenLog isFirstShowSplash:(BOOL)isShow splashClose:(unityBlock)block;
新代码
-(void)initJCSDKWithUnityShow:(unityBlock)block;
```

>4.修改了iOS日志打印接口。新增日志等级功能，详情见: JCAdCallBackHeader.h  
```
旧代码
//+(void)setOpenPlatformLog:(BOOL)openPlatformLog;
新代码
+(void)setTheLogLevel:(MSLogLevelStatus)logLevel;

```

>5.修改了JCiOSConfig.plist文件, 新增字段:   
   "KochavaAppID":    kochava 初始化参数   
   "TenJinAppID":     TenJin 初始化参数   
   "ShowSplashFirst": 应用首次打开是否展示开屏广告. 
   "LogLevel":日志等级 1、关闭. 2、打开JC日志. 3、打开JC+广告日志. 4、打开JC+广告+数据日志. 默认值:1  

**项目配置：**  
* 添加系统库:  
   > AppTrackingTransparency.framework  
* 添加第三方库和文件:
   > KochavaCore.framework               (Embed & Sign)  
   > KochavaTracker.framework            (Embed & Sign)  
   > KochavaAdNetwork.framework          (Embed & Sign)  
   > libTenjinSDK.a  
   > TenjinSDK.h 
</details>
</details>

## resource
<details>
<summary>English</summary>

### Do not download or transfer SDKs (including .a, .framework and .embededframework packages) required for iOS to Windows, as the Windows file system will modify these SDKs so that they will not compile in Xcode.

## Support library And File
[DataCollection_SDK](https://github.com/Romambo/DataCollection_SDK)

[ADThirdParty_SDK](https://github.com/Romambo/ADThirdParty_SDK)

## Document
[1.0.0](https://github.com/Romambo/JCSDK_DocumentFile)

## Unity_bridge
[unityBridge](https://github.com/Romambo/JCSDK_DocumentFile/blob/main/IOS_UnityBridge.zip)

## Version of the record

<details>
<summary>1.0.0</summary>

support development tools: Xcode 11
</details>
 
<details>
<summary>2.0.0</summary>

support development tools: Xcode 12  
**update content**  
>1.Added internal logic waterfall and continuous display  
>2.Added "kochava" and "tenjin" statistics  
>3.Change the SDK initialization interface used by Unity. see: JC_unityAdApi.h
```
old code
//-(void)initJCSDKWithLog:(BOOL)isOpenLog isFirstShowSplash:(BOOL)isShow splashClose:(unityBlock)block;
new code
-(void)initJCSDKWithUnityShow:(unityBlock)block;
```

>4.Change the log log interface, increase the log level.  see: JCAdCallBackHeader.h  
```
old code
//+(void)setOpenPlatformLog:(BOOL)openPlatformLog;
new code
+(void)setTheLogLevel:(MSLogLevelStatus)logLevel;
```

>5.Change JCiOSConfig.plist, add:   
   "KochavaAppID":    kochava initialization parameters   
   "TenJinAppID":     TenJin initialization parameters   
   "ShowSplashFirst": Whether to display splash when the app is first opened. 
   "LogLevel":loglevel 1、closeAll. 2、open JC_log. 3、open JC+AD log. 4、open JC+AD+Data log. Defaults:1  

**Project configuration：**  
* add System library:  
   > AppTrackingTransparency.framework  
* add Third party library and file:
   > KochavaCore.framework               (Embed & Sign)  
   > KochavaTracker.framework            (Embed & Sign)  
   > KochavaAdNetwork.framework          (Embed & Sign)  
   > libTenjinSDK.a  
   > TenjinSDK.h 
</details>
 

</details>



