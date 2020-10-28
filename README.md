# JCSDK-iOS
## Introduction to JCSDK

JCSDK is a set of advertising SDK provided by MS Company, which integrates the advertising SDKs of major advertisers and related statistical SDKs to facilitate the joint operation and data analysis of in-app advertising between platforms.

Ad types supported:

splash Ads、banner Ads、rewardVideo Ads、intersitial Ads、native Ads
 
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
、、、
-(void)initJCSDKWithLog:(BOOL)isOpenLog isFirstShowSplash:(BOOL)isShow splashClose:(unityBlock)block;
、、、
>4.Change the log log interface, increase the log level.  see: JCAdCallBackHeader.h  
>5.Change JCiOSConfig.plist, add: "KochavaAppID", "TenJinAppID", "ShowSplashFirst", "LogLevel"  

**Project configuration：**  
* add Support Library and file:  
   > AppTrackingTransparency.framework  
   > KochavaCore.framework               (Embed & Sign)  
   > KochavaTracker.framework            (Embed & Sign)  
   > KochavaAdNetwork.framework          (Embed & Sign)  
   > libTenjinSDK.a  
   > TenjinSDK.h 
</details>
 



