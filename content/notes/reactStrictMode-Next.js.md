---
title: "useEffect(), React.StrictMode 그리고 Next.js"
date: '2022-12-25'
images: ['https://miro.medium.com/max/1400/1*Ndux6cTfsM3yOgOz5o33SA.png']
---

![React.StrictMode](https://miro.medium.com/max/1400/1*Ndux6cTfsM3yOgOz5o33SA.png)

- `useEffect` callback에서 log를 남겨보면 아무리 간단한 component를 만들어도 두 번 호출된다
- [React Hooks: useEffect() is called twice even if an empty array is used as an argument](https://stackoverflow.com/a/60619061/111890) 을 보니 [React.StrictMode](https://reactjs.org/docs/strict-mode.html) 를 사용하면 dev mode일 때만(production mode에선 아님) 오류 검증을 위해 두 번 호출된다고 함.
- 특별히 strict mode를 지정한 적이 없어서 확인해 보니 `next.config.js`에 `reactStrictMode: true`라고 되어있다. [Next.js를 사용하면 저절로 설정된다](https://nextjs.org/docs/api-reference/next.config.js/react-strict-mode)

---
- [[tags/JavaScript]]
- [짧막글 - react strict 모드란?? - yongseong.log](https://velog.io/@kysung95/%EC%A7%A4%EB%A7%89%EA%B8%80-react-strict-%EB%AA%A8%EB%93%9C%EB%9E%80)