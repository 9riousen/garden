---
title: "ESM (ECMA Script Module)"
date: '2023-02-04'
images: ["https://hacks.mozilla.org/files/2018/03/07_loader_vs_es.png"]
---
![ES Module](https://hacks.mozilla.org/files/2018/03/07_loader_vs_es.png)
- JavsScript의 양대 module system
	- CJS (CommonJS)
	- ESM (ECMA Module System)
- 이 둘을 동시에 지원하도록 library를 만들 수 있다
	- `package.json`의 `exports` 필드를 통해 지원

## CommonJS
- JavaScript 문법은 변경없이 API로 구현하는 느낌 (`module`은 변수, `require`는 함수)
- synchronous
- Tree shaking이 어렵다
- 명시적 file extension: `cjs`, `cts`
```javascript
// add.js
module.exports.add = (x,y) => x + y;

// main.js
const { add } = require('./add');
add(1,2);
```

## ECMAScript Modules
- 새 문법을 도입하여 module을 지원 (`import`, `export` 같은 언어수준 keyword 추가)
- asynchronous ([Top-level await 지원](https://nodejs.org/api/esm.html#top-level-await))
- Tree shaking이 쉽다
- 명시적 file extension: `.mjs`, `.mts`
```javascript
// add.js
export function add(x, y) {
	return x + y;
}
```

---
- [[tags/Glossary]]
- [[tags/JavaScript]]
- [CommonJS와 ESM에 모두 대응하는 라이브러리 개발하기: exports field | toss tech](https://toss.tech/article/commonjs-esm-exports-field)
- [ES modules: A cartoon deep-dive | Mozilla Hacks](https://hacks.mozilla.org/2018/03/es-modules-a-cartoon-deep-dive/)
- [ES6 in Depth: 모듈 | Mozilla 웹기술블로그](http://hacks.mozilla.or.kr/2016/05/es6-in-depth-modules/)
