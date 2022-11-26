---
title: "Electrum"
date: '2022-11-27'
---
# Overview
- Python으로 만든 Bitcoin용 Wallet application ([Github repo](https://github.com/spesmilo/electrum))
	- 이름과 달리 [Electron](https://www.electronjs.org/)하고 아무 관련이 없다
	- 이게 Bitcoin용 desktop wallet중엔 가장 유명한가 본데 꽤 별로임
- Upbit도 안전한지 모르겠으니 옮겨야겠다

# 송금받을 주소 만들기
![[notes/images/Electrum-receive.png]]
- `{ from: 'upbitAddr', to: ??` } 전송을 하기 위해 나의 `to` address를 만드는 법
- `Receive` tab에서 `Create Request`버튼을 누를 때 마다 address가 새로 생성됨
- `Expires after`에 `Never`, `Requested amount`에 blank상태로 `Create Request` 하면 주소 생성
# Upbit는 Bitcoin 개인지갑을 지원하지 않는가?

공지사항 [개인지갑 주소관리](https://upbit.com/mypage/customer_info/personal_wallet) 를 보면 Bitcoin은 지원이 안되네. 킹받네
![[notes/images/selfhosted-wallets-upbit.png]]
- Metamask: Ethereum
- Kaikas: Klaytn
- Phantom: Solana
- Keplr: Cosmos
- Polkadot: Polkadot

---
[[tags/Bitcoin]]