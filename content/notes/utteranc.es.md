---
title: utteranc.es
date: '2022-12-11'
images: ['https://www.discoverfrome.co.uk/wp-content/uploads/2022/03/Utterance-choir-poster-300x300.jpg']
---
![utterence](https://www.discoverfrome.co.uk/wp-content/uploads/2022/03/Utterance-choir-poster-300x300.jpg)

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
## SPA off
- SPA(Single Page Application)로 동작하면 내부 링크로 다른 post로 이동 했을때 utterenc.es 댓글이 업데이트 안됨
- `data/config.yml` 에서 `enableSPA: false` [추가](https://github.com/9riousen/garden/commit/b90e4bf44517579d68d2d8d8d7588aa9943266c2)로 해결

---
- [[tags/TIL]]
- [[tags/English]]