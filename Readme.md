### npm install appcenter appcenter-analytics appcenter-crashes
### ios folder폴더에서
 pod install --repo-update
### ios 폴더의 .xcworkspace열기
### Project Name 마우스오른쪽클릭 Newfile
### AppCenter-Config라는 plist 파일 만들기
### Key String 입력
### AppDelegate.m파일에 
```
#import <AppCenterReactNative.h>
#import <AppCenterReactNativeAnalytics.h>
#import <AppCenterReactNativeCrashes.h>
```
### AppDelegate.m파일 =>didFinishLaunchingWithOptions method return Yes 위에 3줄 추가
```
  [AppCenterReactnative register];
  [AppCenterReactNativeCrashes registerWithAutomaticProcessing]
  [AppCenterReactNativeAnalytics registerWithInitiallyEnabled:true]
```


### android=>app=>src=>main=>assets=>appcenter-config.json 파일설정

### android=>app=>src=>main=>res=>values=>strings.xml 파일에 다으코드추가
```
    <string name="appCenterCrashes_whenToSendCrashes" moduleConfig="true" translatable="false">DO_NOT_ASK_JAVASCRIPT</string>
    <string name="appCenterAnalytics_whenToEnableAnalytics" moduleConfig="true" translatable="false">ALWAYS_SEND</string>

```
