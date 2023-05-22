---
title: "PostCSS with Autoprefixer"
date: '2023-05-14'
images: ['https://theprotoolbox.com/wp-content/uploads/2020/06/Autoprefixer-CSS-online-tool.png']
---
![PostCSS](https://theprotoolbox.com/wp-content/uploads/2020/06/Autoprefixer-CSS-online-tool.png)
- Autoprefixer는 [PostCSS](https://postcss.org/)용 plugin이다
- PostCSS는 CSS의 transform을 수행하는 tool이다. 즉 CSS 소스를 입력받아 변형된 CSS를 출력한다
- PostCSS는 plugin구조로 여러 용도로 사용되지만 [Autoprefixer](https://github.com/postcss/autoprefixer)가 실질적 주 목적임
- 여기서 "prefix"는 브라우저별 vendor prefix를 의미한다. 최근 몇개의 브라우져버전까지 지원할지를 설정해 두면 그에 맞춰 output을 생성한다. [Autoprefixer CSS online](https://autoprefixer.github.io/) 에서 설정을 변경해가며 결과를 확인해 볼 수 있다.
## 입력 예시
```css
:fullscreen {
}
```
## 출력 예시
```css
:-webkit-full-screen {
}
:-ms-fullscreen {
}
:fullscreen {
}
```

## 참고자료 (vendor prefix)
{{<youtube RUa1u2VsKDI>}}

---
- [[tags/Technology|Technology]]
- [PostCSS](https://postcss.org/)
- [Autoprefixer CSS online](https://autoprefixer.github.io/)
