---
title: CometBFT
date: 2023-09-19
images:
  - https://avatars.githubusercontent.com/u/120695482?s=200&v=4
---
![CometBFT](https://avatars.githubusercontent.com/u/120695482?s=200&v=4)
- Tendermint의 fork (Cosmos-SDK 진영에서 Tendermint가 빠져나가고 이름을 못쓰게 해서로 알고 있다)
# docs.cometbft.com (v0.38)
## [Introduction](https://docs.cometbft.com/v0.38/)
- Blockchain application platform이다
	- web server : web application = CometBFT : Blockchain application
- 더 정확히 말하자면 Byzantine Fault Tolerant State Machine Replication (BFT SMR) for arbitrary deterministic, finite state machines
- 예제 앱으로 빠르게 시작하려면 [Quick start guide](https://docs.cometbft.com/v0.38/guides/quick-start)
- CometBFT에서의 앱개발에 대해 제대로 학습하려면 [ABCI++(Application-BlockChain Interface)](https://github.com/cometbft/cometbft/tree/v0.38.x/spec/abci)
- For more details on using CometBFT, see the respective documentation for [CometBFT internals](https://docs.cometbft.com/v0.38/core/), [benchmarking and monitoring](https://docs.cometbft.com/v0.38/tools/), and [network deployments](https://docs.cometbft.com/v0.38/networks/).
# 가이드
## [Go 언어로 built-in 앱을 생성하기](https://docs.cometbft.com/v0.38/guides/go-built-in)
### 가이드의 가정
- CometBFT 앱을 밑바닥부터 만들어 보려는 초보자 대상임
- CometBFT는 BFT SMR을 제공하는 서비스임
- "replicated state machine"이 "application"이다
- application은 ProtoBuf가 지원되는 모든 language로 작성 가능함
- Go로 만든 application인 경우 하나의 process로 실행 가능함(CometBFT를 library로 사용)
- 이 Tutorial에선 Go언어로 kvstore 라는 초간단 애플리케이션을 만들 것이다. key-value를 저장하는 서비스이다
- Go 언어에 일자무식이면 [Learn X in Y miutes where X=Go](https://learnxinyminutes.com/docs/go/) 추천
### Built-in app
- `built-in` 앱은 `external app`의 반대 의미로 사용하였다
- Go언어로 작성하여 CometBFT와 application이 하나의 process로 돌아가는 형태를 의미한다. 최고의 성능.
- Cosmos-SDK도 `built-in` 형태로 작성되었다.
- `external app` 형태는 더 강력한 보안모델을 적용할 수도 있을 것이다
- CometBFT는 애플리케이션의 state에는 접근하지 못한다.
### Go 언어 설치
```bash
$ go version
go version go1.20.7 darwin/arm64
```
- 설치되어 있지 않다면 <https://golang.org/doc/install>
### Project 생성
```bash
$ mkdir kvstore
$ cd kvstore
```
`main.go` 생성
```go
package main

import (
	"fmt"
)

func main() {
	fmt.Println("Hello, CometBFT")
}
```
실행
```bash
$ go run main.go
Hello, CometBFT
```
---
- [[tags/Cosmos SDK|Cosmos SDK]]
- [CometBFT Official Home](https://avatars.githubusercontent.com/u/120695482?s=200&v=4)
