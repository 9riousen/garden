---
title: "(Deep|Universal|App|Dynamic) link"
date: '2023-02-19'
images: ['https://s34035.pcdn.co/wp-content/uploads/2021/07/Apple-UniversalLink-BlogIMG@3x-1536x767.png']
---
![Universal link](https://s34035.pcdn.co/wp-content/uploads/2021/07/Apple-UniversalLink-BlogIMG@3x-1536x767.png)
## ChatGPT가 한글로 알려주더라

### Deep link, Universal link, Dynamic link 차이점을 설명해줘
Deep link, Universal link, Dynamic link는 모두 모바일 애플리케이션에서 링크를 다루는 방법 중 일부입니다. 각각의 차이점은 다음과 같습니다:

1.  Deep link: Deep link는 특정 애플리케이션의 내부 콘텐츠로 바로 이동할 수 있는 하이퍼링크입니다. 예를 들어, 페이스북 앱에서 특정 게시물로 바로 이동하거나, 인스타그램 앱에서 특정 게시물 댓글을 바로 볼 수 있도록 하는 등의 기능을 제공합니다. 이 링크는 앱 개발자가 직접 구현할 수 있습니다.
2.  Universal link: Universal link는 특정 URL을 통해 모바일 앱으로 연결하는 링크입니다. Universal link를 사용하면, 모바일 웹 페이지에서 링크를 클릭하면 해당 앱이 바로 열리는 것이 아니라, 해당 링크와 연결된 앱이 설치되어 있을 경우, 앱으로 연결됩니다. 만약 해당 앱이 설치되어 있지 않으면, 모바일 웹 페이지로 연결됩니다. 이 링크는 앱 개발자가 iOS에서는 애플 개발자 포털, 안드로이드에서는 앱 링크를 통해 설정할 수 있습니다.
3.  Dynamic link: Dynamic link는 Universal link와 비슷한 개념이지만, 추가적인 기능을 제공합니다. Dynamic link를 사용하면, 사용자가 특정 링크를 클릭하여 앱으로 연결된 후, 앱에서 원하는 콘텐츠로 이동할 수 있도록 도와줄 수 있습니다. 예를 들어, 쇼핑 앱에서 특정 상품 페이지로 바로 이동할 수 있도록 하는 등의 기능을 제공합니다. 또한, Dynamic link는 모바일 웹 페이지로도 연결될 수 있으며, 이를 이용하여 iOS와 안드로이드 간의 링크 호환성 문제를 해결할 수 있습니다. 이 링크는 Firebase Dynamic Links를 사용하여 설정할 수 있습니다.

### 각 URL 예제를 보여줘

각각의 링크를 보여드리도록 하겠습니다.

1.  Deep link 예제:
    `myapp://products/123`
    이 링크는 'myapp'이라는 이름의 앱에서, 'products'라는 화면으로 이동하고, 상품 ID가 123인 상품을 보여줍니다.
2.  Universal link 예제:
    `https://www.myapp.com/products/123`
    이 링크는 'myapp'이라는 이름의 앱과 연결되어 있으며, 사용자가 이 링크를 클릭하면 해당 앱의 'products' 화면으로 이동하고, 상품 ID가 123인 상품을 보여줍니다. 사용자가 해당 앱을 설치하지 않았다면, 모바일 웹 페이지에서 해당 콘텐츠를 보여줍니다.
3.  Dynamic link 예제:
    `https://myapp.page.link/products/123`
    이 링크는 Firebase Dynamic Links를 사용하여 생성된 링크로, 사용자가 이 링크를 클릭하면 'myapp'이라는 이름의 앱과 연결되어, 해당 앱의 'products' 화면으로 이동하고, 상품 ID가 123인 상품을 보여줍니다. 사용자가 해당 앱을 설치하지 않았다면, 사용자의 디바이스에 맞는 모바일 웹 페이지에서 해당 콘텐츠를 보여줍니다.

### App Link도 같이 비교해줘
App Link는 안드로이드 플랫폼에서 Universal Link와 비슷한 기능을 제공하는 개념입니다. 앱 링크는 안드로이드 운영체제에서 URL을 사용하여 앱과 웹 사이트 간의 연결을 지원합니다. Universal Link와 마찬가지로 사용자가 링크를 클릭하면 연결된 앱을 열 수 있고, 앱이 설치되어 있지 않은 경우 Google Play Store에서 해당 앱을 다운로드하도록 안내할 수 있습니다.

앱 링크를 사용하려면, 해당 링크를 앱의 `AndroidManifest.xml` 파일에 등록하고, 웹 사이트에서 해당 링크와 연결된 디지털 에셋을 등록해야 합니다. 이를 통해 안드로이드 플랫폼에서 앱 링크를 인식하고 사용자가 링크를 클릭할 때마다 해당 앱으로 연결할 수 있습니다.

App Link 예제:

`https://www.example.com/product/123`

이 링크는 'example.com' 웹 사이트와 연결되어 있으며, 사용자가 이 링크를 클릭하면 해당 앱의 'product' 화면으로 이동하고, 상품 ID가 123인 상품을 보여줍니다. 사용자가 해당 앱을 설치하지 않았다면, Google Play Store에서 해당 앱을 다운로드하도록 안내할 수 있습니다.

---
- 설명이 너무 깔끔하구나
- Deep link
	- mobile app에서 custom protocol handler를 정의하여 브라우져가 아닌 전용앱으로 여는 링크임
	- `http://` 나 `https://` 로 시작하지 않고 `gongshim://` 처럼 custom scheme을 가진다
	- iOS에도 있고 Android에도 있다
- Universal Link(iOS), App Link(Android)
	- 이 둘은 거의 같은 개념인데 Platform만 다르다고 보면 됨
	- `https://gongshim.net/teams/12` 처럼 `https://`로 시작함. 외형적으론 일반 web page주소와 구분이 안됨
	- 하지만 `.well-known`에 해당 사이트를 볼 수 있는 native app의 정보를 기재해 두어 disambiguation(browser로 열것인가? 공식 app으로 열 것인가?) dialog 단계없이 바로 Native App으로 해당 정보를 볼 수 있게한다
	- app이 설치 안된 경우 설치를 유도할 수 있다
- Firebase Dynamic Links
	- Universal Link와 App Link를 둘 다 지원하는게 번거로우니 한꺼번에 지원해주는 서비스가 몇 개 있다. 그 중 하나임
	- Firebase는 원래 Google이 만든 회사가 아니고 인수한 회사임
	- Google Dynamic Links라고 안하고 `Firebase` 라는 이름을 유지하는 이유는 iOS도 지원하는 중립적인 느낌을 주려는게 아닐까?
---
- [[tags/Technology]]
- [Google Acquires Firebase To Help Developers Build Better Real-Time Apps - TechCrunch (2014)](https://techcrunch.com/2014/10/21/google-acquires-firebase-to-help-developers-build-better-realtime-apps/)
- [Avoid Android disambiguation dialog Using App Link Digital Assets Link](https://medium.com/android-news/avoid-android-disambiguation-dialog-using-app-link-digital-assets-link-434395e1ed30)
- [For what is the ".well-known" folder? - serverfault](https://serverfault.com/a/795474)
- [Android App Links 추가](https://developer.android.com/studio/write/app-link-indexing?hl=ko)