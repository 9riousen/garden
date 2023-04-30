---
title: "eth_call"
date: '2023-04-30'
images: ['https://chainstack.com/wp-content/uploads/2022/12/Deep-dive-eth_call-2.png']
---
![eth_call](https://chainstack.com/wp-content/uploads/2022/12/Deep-dive-eth_call-2.png)
- `eth_call`은 Ethereum의 표준 JSON-RPC method중 하나
- on-chain transaction을 생성하지 않는 메세지를 수행한다

## Uniswap에서 사용하는 예제

엄밀히 말하면 uniswap과 별 상관 없는 동작이겠지만 Chrome DevTools에서 XHR을 보다가 나오는 request중 하나를 보면

- URL : https://mainnet.infura.io/v3/099fc58e0de9451d80b18d7c74caa7c1 (Uniswap이 사용하는 infura node)
- Method: POST
- Request Payload:

```json
{
	"method":"eth_call",
	"params":[
		{
			"to": "0x4976fb03c32e5b8cfe2b6ccb31c09ba78ebaba41",
			"data": "0xbc1c58d1aae707a405af4e19115d90a3be269b60383893f005e956d754877d56b002567b"
		},
		"latest"
	],
	"id":48,
	"jsonrpc":"2.0"
}
```
- Response:
```json
{
	"jsonrpc": "2.0",
	"id": 48,
	"result": "0x00000000000000000000000000000000000000000000000000000000000000200000000000000000000000000000000000000000000000000000000000000026e30101701220c24630c4bc3e0e5227956d059b6f57b2ba14afae5e42b1e8f2858fb257d114550000000000000000000000000000000000000000000000000000"
}
```

- Request의 `to`를 [Etherscan에서 보면](https://etherscan.io/address/0x4976fb03c32e5b8cfe2b6ccb31c09ba78ebaba41) ENS contract임을 알 수 있다.
- `latest`라고 되어있는 자리에는 block number를 hex로 기재하던지 기타 몇가지 tag를 지정할 수 있다
- Request의 `data`와 Response의 `result`를 ABI를 사용하면 decode할 수 있을텐데 어떻게 하는거지?

---
- [[tags/Ethereum]]
- [Deep dive Into eth_call - Chainstack](https://chainstack.com/deep-dive-into-eth_call/)
- [JSON-RPC API - ethereum.org](https://ethereum.org/en/developers/docs/apis/json-rpc/)
- [Ethereum input data decoder](https://lab.miguelmota.com/ethereum-input-data-decoder/example/)
