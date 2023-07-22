---
title: "CosmWasm"
date: '2023-07-22'
images: ['https://avatars.githubusercontent.com/u/52079682?s=280&v=4']
---
![CosmWasm](https://avatars.githubusercontent.com/u/52079682?s=280&v=4)

# 개요
- [[tags/Cosmos SDK|Cosmos SDK]] 기반의 Blockchain에 WebAssembly 기반의 Smart contract runtime을 제공하는 module
# 도입 동기
- 원래 Cosmos SDK 진영은 Smart contract 보다는 여러개의 고성능 [App chain (aka. Application-specific Blockchain)](https://docs.cosmos.network/main/intro/why-app-specific)을 만들고 이들을 [IBC(Inter-Blockchain Communication)](https://tutorials.cosmos.network/academy/3-ibc/1-what-is-ibc.html)로 연결하는 개념을 지향. 즉, dApp마다 Blockchain을 따로 운영하는 개념을 추구
- 하지만 현실적인 문제들 발생
	- dApp 로직 수정시 chain upgrade필요. 이 과정이 큰 작업이고 breaking change면 더욱 번거롭다
	- app chain 별로 validator를 구해야 한다. 소형 dApp사가 진행하기엔 무리
# 왜 CosmWasm 인가?
- WebAssembly는 언어에 종속적이지 않다
	- 현실은 Rust말고는 어렵긴 하지만 LLVM 상의 언어를 모두 포함할 예정
- [Actor model을 도입](https://book.cosmwasm.com/actor-model.html)하여 [EVM의 Reentrancy 공격](https://matt-rickard.com/reentrancy-attacks)을 원천차단한다. 즉, 더 안전한 runtime이다
- 실행속도가 빠르다
- Code와 instance의 분리

# CosmWasm 101: Counter 컨트랙트 by DSRV

<iframe width="560" height="315" src="https://www.youtube.com/embed/9a08CacSjRQ?si=k6shob10ojoa6GDC" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

# 추천자료
- [CosmWasm 101: Counter 컨트랙트 by DSRV](<https://www.youtube.com/playlist?list=PLpDsd5-6efUbb_0V0vg5R54GSRxtK0-vX>)
- [CosmWasm 101 와씀 1편: Counter 컨트랙트 톺아보기 - DSRV Medium](https://medium.com/dsrv/cosmwasm-101-%EC%99%80%EC%94%80-1%ED%8E%B8-counter-%EC%BB%A8%ED%8A%B8%EB%9E%99%ED%8A%B8-%ED%86%BA%EC%95%84%EB%B3%B4%EA%B8%B0-e82ac42569ba)

# 관심 있는 CosmWasm 지원 체인
- [Junø](https://junonetwork.io/)
	- Interchain과 smart contract 지원 blockchain
- [Terra](https://academy.terra.money/courses/cosmwasm-smart-contracts-i)
	- 썩어도 준치
- [Osmosis](https://osmosis.zone/)
	- [Upload 단계가 permissioned](https://osmosis.zone/blog/permissioning-cw-contracts)
---
- [[tags/Cosmos SDK|Cosmos SDK]]
- <https://cosmwasm.com>
- [Application-Specific Blockchain](https://docs.cosmos.network/main/intro/why-app-specific)
- [What is IBC?](https://tutorials.cosmos.network/academy/3-ibc/1-what-is-ibc.html)