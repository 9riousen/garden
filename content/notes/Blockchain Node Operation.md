---
title: "Blockchain Node Operation"
date: '2023-01-14'
images: ["https://101blockchains.com/wp-content/uploads/2021/04/types-of-nodes-in-blockchain.png"]
---
![Blockchain Node](https://101blockchains.com/wp-content/uploads/2021/04/types-of-nodes-in-blockchain.png)
- Blockchain node를 운영하는 업체들이 지원하는 API가 조금씩 다르네. 이런건 의무사항은 아닌건가? 초심자는 혼란스럽다
- 아래의 노드는 모두 같은 network(`cosmoshub-4`)의 node임

## api.cosmos.network
- REST API에 대한 정보는 https://v1.cosmos.network/rpc/v0.44.5 에서 확보함
- 여기 swagger에서 가장 간단한 `GET /node_info` 만 해봐도 `503 - Service Unavailable` 이다. `api.cosmos.network` 면 공식 서버일텐데 이래도 되나? (gRPC endpoint만 신경쓰나보다)

## lcd-cosmoshub.keplr.app
- 여기가 차라리 낫다. keplr를 제공하다 보니 책임감 있게 운영하나 보다.
- https://lcd-cosmoshub.keplr.app/blocks/latest 는 잘 동작한다.
- 그런데 https://lcd-cosmoshub.keplr.app/blocks/latest 이건 404다. 스펙 문서는 https://v1.cosmos.network/rpc/v0.44.5 이걸 보고 테스트 중이다.
- https://lcd-cosmoshub.keplr.app/cosmos/auth/v1beta1/accounts 이것도 404이다. cosmoshub와 같은 node binary(gaiad)를 사용하는데 load balancer에서 경로를 차단하는것일까? 전체 address를 iterate하면 node에 부하를 줄테니 이해는 된다.
- https://lcd-cosmoshub.keplr.app/cosmos/auth/v1beta1/accounts/cosmos1kw88mhxtm2w8emvvr6gv5u0wmgx9p9kktgavxx 이렇게 특정 주소를 지정하면 잘 된다
## cosmos-mainnet-rpc.allthatnode.com
- 역시 전문업체라 그런지 잘 된다
- https://cosmos-mainnet-rpc.allthatnode.com:1317/node_info - 👍
- https://cosmos-mainnet-rpc.allthatnode.com:1317/cosmos/auth/v1beta1/accounts/cosmos1kw88mhxtm2w8emvvr6gv5u0wmgx9p9kktgavxx - 👍
- https://cosmos-mainnet-rpc.allthatnode.com:1317/cosmos/auth/v1beta1/accounts - ❌
	- 여기서도 account 목록은 의도적으로 차단하는 듯 보임
	- Status code는 `200` 이긴 함
---
- [[tags/Blockchain]]
- [[tags/TODO]]