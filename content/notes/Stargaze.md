---
title: "Stargaze"
date: '2022-11-24'
---
- <https://www.stargaze.zone/>
- Keplr 연동됨
- CosmWasmJS
- IPFS
	- NFT.storage
	- Pinata
- Discord
	- faucet도 discord bot으로 구현해 community 참여 유도
# [Launching an NFT project](https://docs.stargaze.zone/guides/readme/1.-setup-a-basic-project)
- [stargaze-tools](https://github.com/public-awesome/stargaze-tools)를 clone하고 `config.js` 수정
- repo안에 image upload등 필요한 script모두 제공됨
- [Stargaze's sg721 contract allows for off-chain metadata storage. We recommend using a decentralized storage solution such as IPFS](https://docs.stargaze.zone/guides/readme/3.-add-assets-and-metadata)
- Stargaze NFT metadata follows the [OpenSea metadata standards](https://docs.opensea.io/docs/metadata-standards).
- NFT.storage
	- image도 올리고 (CID - Content ID)받는다
	- metadata도 올리고 CID받는다
- BaseURL 예제 (`baseTokenUri`로 사용)
	- ipfs://bafybeigemuqa4ddnexclmc633qghcrbd34ne2jq6aym6udubldxzmss6ma/metadata
- Minter Contract
	- Minter contract는 이미 chain에 있다. instantiate만 시키면 된다(Ethereum과 차이)
	- script 제공
		- `minter` : minting, 가격, whitelist 관리 contract를 instantiate
		- `sg721`: collection contract를 instantiate
	- collection launching에 1000 STARS를 gas fee로 소모
		- 50%: burn
		- 50%: communit pool (추후 staker에게 분배될 것)
# Clips
- [How to deploy an NFT collection on Stargaze in 9 minutes](https://youtu.be/1gvDlBWKEUc)
---
[[tags/Cosmos SDK]] [[tags/NFT]]