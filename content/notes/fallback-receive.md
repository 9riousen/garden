---
title: fallback() & receive()
---

- ERC-20 contract에서 다음 두가지 callback을 구현할 수 있다
- `fallback()`: 없는 함수를 호출하는데 `msg.data`에 내용이 있는 경우
- `receive()`: ERC 토큰이 아닌 ETH(Coin)을 전송받은 경우
- [[tags/TODO]] 실험필요

---
[[tags/Solidity]]