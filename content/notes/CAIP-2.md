---
title: "CAIP-2: 여러 블록체인을 지원하는 Chain ID"
date: '2023-02-26'
images: ['https://opengraph.githubassets.com/1d1c8207a84664bd0595de367fe9b1f5389102001fb49a2823f8d83e6febef42/ChainAgnostic/CAIPs/issues/5']
---
![CAIP-2](https://opengraph.githubassets.com/1d1c8207a84664bd0595de367fe9b1f5389102001fb49a2823f8d83e6febef42/ChainAgnostic/CAIPs/issues/5)

- 특정 체인에 종속적이진 않은 스펙을 정의하는 [Chain Agnostic](https://chainagnostic.org/)
- 각 Blockchain 마다 chind id의 스펙 정의가 있다. 예를들어 Ethereum의 chain id는 정수형이다
- namespace를 포함한 문자열 형태로 chain id를 정의하는 표준이다

## Examples

```
# Ethereum mainnet
eip155:1

# Bitcoin mainnet (see https://github.com/bitcoin/bips/blob/master/bip-0122.mediawiki#definition-of-chain-id)
bip122:000000000019d6689c085ae165831e93

# Litecoin
bip122:12a765e31ffd4059bada1e25190f6e98

# Feathercoin (Litecoin fork)
bip122:fdbe99b90c90bae7505796461471d89a

# Cosmos Hub (Tendermint + Cosmos SDK)
cosmos:cosmoshub-2
cosmos:cosmoshub-3

# Binance chain (Tendermint + Cosmos SDK; see https://dataseed5.defibit.io/genesis)
cosmos:Binance-Chain-Tigris

# IOV Mainnet (Tendermint + weave)
cosmos:iov-mainnet

# StarkNet Testnet
starknet:SN_GOERLI

# Lisk Mainnet (LIP-0009; see https://github.com/LiskHQ/lips/blob/master/proposals/lip-0009.md)
lip9:9ee11e9df416b18b

# Dummy max length (8+1+32 = 41 chars/bytes)
chainstd:8c3444cf8970a9e41a706fab93e7a6c4
```

---
- [[tags/Blockchain]]
- https://github.com/ChainAgnostic/CAIPs/blob/master/CAIPs/caip-2.md
