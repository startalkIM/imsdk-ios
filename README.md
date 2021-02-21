Startalk, The Best open sourced instant messenger software in the world!

* [Chinese Version(中文版)](https://github.com/startalkIM/imsdk-ios/blob/master/README_zh_CN.md)

Public Service(Startalk App)
=====
Based on Startalk public service and Startalk client apps, users can build their own IM service using their own domain,
Sign up an account in our web site, create new domains, add users, download client app, and configure navigation for that domain,
After the 5 steps above, you own your own IM now.

Download client app [Download](https://i.startalk.im/home/#/download)
Register new domain in our web site: [Register[(https://i.startalk.im/home/#/register)

- Android

[![Startalk on Android](https://s.qunarzz.com/qtalk_official_web/pages/download/android.png)](https://qt.qunar.com/downloads/qtalk_android.apk)

- iOS

*temporary unavailable due to App Store certificate problem.

Configure navigation for client app [Configure navigation](https://i.startalk.im/home/#/platform/access_guide/config_navs?id=config_navs)

Private Service(Startalk SDK)
=====
Private Service is a way for decentralized deployment. Customers or enterprises would deploy the back end code on their own servers, embedding SDK into their own apps. Every enterprise is an independent node; every node works independently, and the data would only be saved in the node.  

Please see the guide of embedding Android SDK and the configuration below.

## Requirements

- iOS 9.0 or later
- Xcode 10.0 or later

## Getting Started

- Read this Readme doc

## Communication
- If you'd like to **ask a general question**, use [Stack Overflow](http://stackoverflow.com/questions/tagged/startalk).
- If you **found a bug**, open an issue.
- If you **have a feature request**, open an issue.


## Example Run
```
1. pod install
2. open IMSDK-iOS.xcworkspace use Xcode10+
```
## How To Use

* Objective-C

```objective-c
#import "QIMSDK.h"
...
[QIMSDKUIHelper sharedInstanceWithRootNav:rootNav rootVc:rootVc];
...
BOOL success = [[QIMKit sharedInstance] qimNav_updateNavigationConfigWithDomain:@"qim.com" WithUserName:@"san.zhang"];
if (success = YES) {
  [[QIMKit sharedInstance] loginWithUserName:userName WithPassWord:userPwd];
} else {
  
}
...
UIView *sessionView = [[QIMSDKUIHelper sharedInstance] getQIMSessionListViewWithBaseFrame:self.view.bounds];
[self.view addSubview:sessionView];
```

- For details about how to use the library and clear examples, see [The detailed How to use](https://github.com/startalkIM/imsdk-ios/wiki/QIMSDK-iOS%E6%8E%A5%E5%8F%A3%E6%96%87%E6%A1%A3%E8%AF%B4%E6%98%8E)

## Installation

There are four ways to use QIMSDK in your project:
- using CocoaPods
- manual install (build frameworks or embed Xcode Project)

### Installation with CocoaPods

[CocoaPods](http://cocoapods.org/) is a dependency manager for Objective-C, which automates and simplifies the process of using 3rd-party libraries in your projects. See the [Get Started](http://cocoapods.org/#get_started) section for more details.

#### Podfile
```
source 'https://github.com/qunarcorp/libqimkit-ios-cook.git'
source 'git@github.com:CocoaPods/Specs.git'
platform :ios, '9.0'
pod 'QIMUIKit', '~> 4.0'
```

### Manual Installation Guide

See more on [Manual install Guide](https://github.com/startalkIM/imsdk-ios/wiki/Customized-building-manually)

### Import headers in your source files

In the source files where you need to use the library, import the umbrella header file:

```objective-c
#import "QIMSDK.h"
```

### Build Project

At this point your workspace should build without error. If you are having problem, post to the Issue and the
community can help you solve it.

Feedback
=====
-   app(AT)startalk.im（Email）
