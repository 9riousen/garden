---
title: "Remote Debugging WebViews"
date: '2023-01-05'
images: ['https://wd.imgix.net/image/admin/bI74HumV9kgCZc0l3OXl.png?auto=format&w=845']
---
![WebView for Android remote debugging](https://wd.imgix.net/image/admin/bI74HumV9kgCZc0l3OXl.png?auto=format&w=845)

- Desktop Chrome의 inspect window에서 Android(Emulator or USB connected device) WebView를 debug할 수 있다.
	- Desktop에서 <chrome://inspect/#devices> 에 접속
- Android app 코드에서 `WebView.setWebContentsDebuggingEnabled(true)`가 호출된 경우만 (static method라 application내 모든 WebView instance에 적용됨)
- WebView뿐 아니라 Android Chrome도 Wireless adb 연결되어 있으면 device 목록에 나타남

---
- [[tags/JavaScript]]
- [Remote debugging WebViews - Chrome Developers](https://developer.chrome.com/docs/devtools/remote-debugging/webviews/)
- [Remote debug Android devices - Chrome Developers](https://developer.chrome.com/docs/devtools/remote-debugging/)
