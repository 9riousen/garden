---
title: "useEffect() 사용시 componentWillUnmount() 기능"
date: '2023-03-01'
images: ['https://daily-dev-tips.com/images/20-03-2022.jpg']
---

![useEffect cleanup](https://daily-dev-tips.com/images/20-03-2022.jpg)

- `useEffect()` 의 인자로 넘기는 함수를 정의할 때 clean up 함수를 정의하여 return하도록 설정 가능함
- 즉, `componentDidMount()`에서 정의하던 내용을 body에 넣고 `componentWillUnmount()`의 body부분을 실행하는 함수를 return하도록 작성 가능
```javascript
useEffect(() => {
  // Your effect

  return () => {
    // Cleanup
  };
}, []);
```

---
- [[tags/JavaScript]]
- [React - Effect Hook ( Clean-up ) - 흥(興)](https://velog.io/@enjoywater)
- [How to manage componentWillUnmount with useEffect - dev.to](https://dev.to/robmarshall/how-to-use-componentwillunmount-with-functional-components-in-react-2a5g)
- [React useEffect cleanup - daily dev tips](https://daily-dev-tips.com/posts/react-useeffect-cleanup/)
