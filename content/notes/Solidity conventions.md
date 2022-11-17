---
title: Solidity conventions
---
- [Style Guide](https://docs.soliditylang.org/en/v0.8.16/style-guide.html#style-guide "Permalink to this heading")

## Indent
- 4 spaces

## Blank lines
### Top level declaration에는 공백라인을 추가한다 (contract 사이)
```solidity
// SPDX-License-Identifier: GPL-3.0
pragma solidity >=0.4.0 <0.9.0;

contract A {
	// ...
}

contract B {
	// ...
}

contract C {
	// ...
}
```

### function group간에 공백라인
- one-liner의 경우 두지 않는다
- 아래의 예시에서 `spam`과 `ham`은 서로 반대 group이다
```solidity
// SPDX-License-Identifier: GPL-3.0
pragma solidity >=0.6.0 <0.9.0;

abstract contract A {
	function spam() public virtual pure;
	function ham() public virtual pure;
}

contrct B is A {
	function spam() public pure override {
		// ...
	}

	function ham() public pure override {
		// ...
	}
}
```

## Maximum Line Length
- 최대 120자 / line
- wrap될 때 indent는 한 번만
```solidity
thisFunctionIsReallyLong(
	longArgument1,
	longArgument2,
	longArgument3
);
```
- 나쁜 예#1
```solidity
thisFunctionIsReallyLong(longArgument1,
							longArgument2,
							longArgument3);
```
- 나쁜 예#2
```solidity
thisFunctionIsReallyLong(
longArgument1,
longArgument2,
longArgument3
);
```
## Source code
- UTF-8
- source file이름은 contract나 library이름에 맞춘다
	- source file 하나에 2개이상의 contract가 있으면 핵심 contract를 기준으로 한다
	- Contract이름은 `CapWord` 스타일을 따른다 (Pascal case)
---
[[tags/Solidity]]