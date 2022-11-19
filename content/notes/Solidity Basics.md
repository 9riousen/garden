---
title: Solidity Basics
date: '2022-11-19'
---
# Data type
- `bool` 에는 `true` or `false`만 가능
- 숫자
	- `int8` (8bit), `int16`... ~ `int256` (256bit) 까지의 타입이 존재한다
		- byte가 최소 할당 단위이기 때문에 8의 배수로만 존재한다. 즉, `int7`이나 `int15`는 존재하지 않는다
		- `int` 는 `int256`이다. gas를 아끼려면 최소한의 메모를 할당해야 한다
	- unsigned형도 존재한다. `uint8` ~ `uint256`
		- `uint`는 `uint256`이다.
	- 고정소수점
		- [부동소수점(floating point) 수는 지원되지 않는다. 고정소수점은 지원된다](https://solidity-kr.readthedocs.io/ko/latest/)
		- `fixedMxN` 형식의 타입 제공
			- `M`: 8의 배수 (`8` ~ `256`), 수의 배열
			- `N`: 소수점 자리수
			- [[tags/TODO]]: 예제 추가
		- `fixed`는 `fixed128x19`
		- `ufixed`는 `ufixed128x19`
- [`bytes1`(1byte)~`bytes32`(32byte) 타입이 지원된다](notes/bytes type) 

# Read only 동작
- state를 변경하지 않는 함수는 호출하여도
	- blockchain transaction이 생성되지도 않고 block에 기록되지도 않는다
	- [[tags/TODO]] 그럼 어떻게 호출하는가? smart contract의 메소드 호출은 tx를 만들어야 하는거 아닌가?

# `view` function
- <https://www.tutorialspoint.com/solidity/solidity_view_functions.htm>
```solidity
pragma solidity ^0.5.0;

contract Test {
   function getResult() public view returns(uint product, uint sum){
      uint a = 1; // local variable
      uint b = 2;
      product = a * b;
      sum = a + b; 
   }
}
```
- `returns` 앞에 `view` 가 붙은 함수는
	- contract의 state를 변경시키지 않는다
	- state변수를 읽기는 한다 (`pure` function과의 차이점)
# `pure` function
- <https://www.tutorialspoint.com/solidity/solidity_pure_functions.htm>
- state를 읽지도 않고 오로지 함수의 인자만 참고하여 return한다

# Data location
- `storage`
	- contract의 field는 `storage`에 저장된다
- `memory`
	- 함수 body에서 allocate
- `calldata`
	- function arguments가 저장되는 곳
	- `memory`와 거의 동일하게 동작한다

# [Remix IDE](https://remix.ethereum.org/)
- [[notes/Code completion in Remix]]

# [Special Variables and Functions](https://docs.soliditylang.org/en/v0.8.17/units-and-global-variables.html#special-variables-and-functions "Permalink to this heading")
- `blockhash(uint blockNumber) returns (bytes32)`: hash of the given block when `blocknumber` is one of the 256 most recent blocks; otherwise returns zero
- `block.basefee` (`uint`): current block’s base fee ([EIP-3198](https://eips.ethereum.org/EIPS/eip-3198) and [EIP-1559](https://eips.ethereum.org/EIPS/eip-1559))
- `block.chainid` (`uint`): current chain id 
- `block.coinbase` (`address payable`): current block miner’s address 
- `block.difficulty` (`uint`): current block difficulty
- `block.gaslimit` (`uint`): current block gaslimit 
- `block.number` (`uint`): current block number
- `block.timestamp` (`uint`): current block timestamp as seconds since unix epoch
- `gasleft() returns (uint256)`: remaining gas
- `msg.data` (`bytes calldata`): complete calldata
- `msg.sender` (`address`): sender of the message (current call)
- `msg.sig` (`bytes4`): first four bytes of the calldata (i.e. function identifier)
- `msg.value` (`uint`): number of wei sent with the message
- `tx.gasprice` (`uint`): gas price of the transaction
- `tx.origin` (`address`): sender of the transaction (full call chain)

# `payable` keyword
- ether를 보내는 함수는 `payable`이 붙어야 함
- 종류
	- address payable
		- 이 타입의 변수는 `send()`와 `transfer()`를 가진다
	- function payable
		- 이 함수를 호출 할 때 `msg.value`를 지정하여 contract 주소에 입금 가능
- `msg.value`는 payable 함수를 호출하면 contract에 쌓인다. function body에서 무엇을 하던 상관 없다.
- payable이 아니면서 주소로 자신(contract)의 돈을 보내느 함수도 작성 가능
- 함수가 payable이건 아니건 contract 주소만 알면 ETH는 보낼 수 있는거 맞지?
	- Metamask에 local ganache 추가 성공
	- ganache의 private key를 import하니 잘 나오네
	- 엇? contract로 0.01eth 했더니 실패. 다시 해봐야지. 에러는 out of gas 라고 나오긴 하는데
	- 옷! 역시나 `receive()`를 구현하니 잘 된다. out of gas나는 건 사람 헷깔리게 한다
## `receive()` and `fallback()`
- 눈치 챘을지 모르지만 이 함수들은 `function` keyword를 사용하지 않는다
- `external` 이어야 한다. 아니면 Remix에서 에러 발생
	- 참고 : [`external`이 `public`보다 gas fee 저렴](https://ethereum.stackexchange.com/a/19391/54687)

# [Sending Ether](https://solidity-by-example.org/sending-ether/)
- Contract에 ETH를 보내는 방법은 3가지
	- `address.transfer(amount)`: 실패시 error
	- `address.send(amount)`: 성공여부 반환(false면 `revert()`를 call하자)
	- `address.call{value:msg.value}("")`:  (result, data)를 반환

# 참고자료
- <https://solidity-kr.readthedocs.io/> (한글)
- <https://remix.ethereum.org/>
- [solidity - payable (1) 개념](https://caileb.tistory.com/147)
- [Units and global variables](https://docs.soliditylang.org/en/v0.8.13/units-and-global-variables.html): API Reference
---
[[tags/Solidity]]