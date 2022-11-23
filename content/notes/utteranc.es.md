---
title: utteranc.es
date: '2022-11-23'
---
- https://en.dict.naver.com/#/entry/enko/099e7744e7444e0488d2cf86d724275b
	- 어터런시즈
	- 발언(들)
	- 동사형: utter
- <https://utteranc.es/>
- GitHub issue search API사용 (with url, pathname, title)
- 사용자가 GitHub OAuth로 authorize해야 post가능
## Configuration
- public repo여야 함
- repo에 [utterances app](https://github.com/apps/utterances)을 설치해야 함
- issue가 on되어있나 확인
```javascript
<script src="https://utteranc.es/client.js"
        repo="9riousen/garden"
        issue-term="pathname"
        theme="github-light"
        crossorigin="anonymous"
        async>
</script>
```
---
[[tags/TIL]] [[tags/English]]