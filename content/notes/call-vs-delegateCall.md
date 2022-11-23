---
title: "call vs delegateCall"
date: '2022-11-20'
---
- https://eun97.tistory.com/entry/Solidity-call-delegateCall
- 둘 다 contract A가 contract B의 function을 호출 할 때 사용
- `call()`
	- 가장 기본적인 호출
	- B의 function안에서 보면 `msg.sender`는 Contract A
	- contract B의 state가 변경됨
- `delegateCall()`
	- Contract B의 함수에게 내(Contract A) state를 변경시킬 권한을 넘겨주면서 호출
	- `msg.sender`는 A(`call()`과 동일)
	- 즉, Contract A의 state가 변경됨 (Contract A state의 field들이 Contract B와 같아야 함)
	- <https://ethereum.stackexchange.com/a/3672/54687>
---
[[tags/Solidity]]