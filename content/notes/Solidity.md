---
title: Solidity
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

# 참고자료
- https://solidity-kr.readthedocs.io/ (한글)
- https://remix.ethereum.org/
---
[[tags/Solidity]]