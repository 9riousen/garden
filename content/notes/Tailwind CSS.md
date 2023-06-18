---
title: "Tailwind CSS"
date: '2023-05-14'
images: ['https://sjmitchblog.gatsbyjs.io/static/b010f9233278411413e88e0ac9a9c96f/d8623/image.jpg']
---
![TailwindCSS](https://sjmitchblog.gatsbyjs.io/static/b010f9233278411413e88e0ac9a9c96f/d8623/image.jpg)
- tailwind는 순풍(역풍의 반대)을 의미한다. "순풍CSS"
- Prototyping을 하거나 간단히 개인프로젝트를 할 때 CSS 공부하기는 부담스럽다면 그나마 Tailwind CSS를 사용하는게 좋다
- 제대로 만들어야 하는 서비스라면 유지관리성에서 떨어진다고 생각함
- css 파일을 서비스 개발자가 작성하지 않고 Tailwind CSS가 제공하는 CSS class들만 취사 선택하여 적용한다. 즉, HTML 파일 밖을 벗어나지 않아도 된다

# [Responsive Design](https://tailwindcss.com/docs/responsive-design)
## width의 5가지 breakpoint prefix
- media query의 `min-width`로 동작한다
- https://tailwind-css-responsive-1.rious9.repl.co/

|Breakpoint prefix|Minimum width|CSS|
|---|---|---|
|`sm`|640px|`@media (min-width: 640px) { ... }`|
|`md`|768px|`@media (min-width: 768px) { ... }`|
|`lg`|1024px|`@media (min-width: 1024px) { ... }`|
|`xl`|1280px|`@media (min-width: 1280px) { ... }`|
|`2xl`|1536px|`@media (min-width: 1536px) { ... }`|

---
- [[tags/Web Frontend|Web Frontend]]
- [Tailwind CSS](https://tailwindcss.com/)
- [Tailwind CSS Cheat Sheet](https://tailwindcomponents.com/cheatsheet/)
