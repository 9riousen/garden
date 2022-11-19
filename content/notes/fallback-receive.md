---
title: fallback() & receive()
date: '2022-11-19'
---

- 일반적인 경우 contract call에는 `msg.value`가 `0`이다.
- 하지만 `payable` 함수를 호출할 때는 contract balance에 추가도 되고 함수 body도 수행된다.
- Contract에서 다음 두가지 callback을 구현할 수 있다
	- `fallback() external payable`
		- 없는 함수를 호출하는 경우
	- `receive()` external payable
		- 이 contract주소로 ETH입금이 발생한 경우

---
[[tags/Solidity]]