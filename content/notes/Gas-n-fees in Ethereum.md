---
title: "Gas-n-fees in Ethereum"
date: '2022-12-05'
images: ["https://ethereum.org/static/9628ab90bfd02f64cf873446cbdc6c70/302a4/gas.png"]
---
![gas](https://ethereum.org/static/9628ab90bfd02f64cf873446cbdc6c70/302a4/gas.png)
- Gas (unit)
	- 한국어로 '기름(휘발유)' 정도 된다. 단위는 `liter`가 아니고 `gas`자체이다.
	- "종로에서 일산가는데 휘발유 3L가 사용된다" 라는 느낌과 비슷하게
	- "ERC20 token을 transfer 하는데 65,000gas가 사용된다" 처럼 말 할 수 있다
	- 즉, 거리에 따라 liter수가 다르듯 실행하는 함수마다 소모되는 `gas`가 달라진다
- Gas Price
	- 휘발유도 liter당 가격이 유동적이듯 `gas`의 가격도 항상 변한다
		- 휘발유: 변경주기([[tags/TODO]] 하루?)마다 조정. 단위: **KRW/L**
		- Gas: 블럭마다 조정. 단위: **ETH/gas**
- Gas Fee (가스비)
	- 사용자가 함수호출에 사용할 비용은 결국 **3L X 1500원 = 4500원** 과 비슷하다
	- **Gas fee = gas X gasPrice**
	- 현재 [평균 Gas price는 14.84 Gwei](https://ycharts.com/indicators/ethereum_average_gas_price)
	- 즉, ERC20 transfer에 드는 gas fee는 대략 65,000gas X 14.84Gwei = 964600 Gwei
		- =0.0009646ETH ([Gwei calculator](https://www.alchemy.com/gwei-calculator))
	- Ether는 감이 없으니까 현재 가격(1ETH=1275.18USD)으로 대략 **1.23USD** = 1599KRW
---
- [[tags/Ethereum]]
- [Gas and fees - ethereum.org](https://ethereum.org/ko/developers/docs/gas/#top)