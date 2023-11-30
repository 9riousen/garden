---
title: stETH vs wstETH
date: 2023-11-30
images:
  - https://s2.coinmarketcap.com/static/img/coins/200x200/8000.png
---
![LIDO](https://s2.coinmarketcap.com/static/img/coins/200x200/8000.png)

# stETH vs. wstETH
- 둘 다 Ethereum 2.0의 Liquid staking 서비스를 제공하는 Lido 에서 발행하는 ERC20토큰임. 언제든 <https://stake.lido.fi/wrap/> 에서 서로 wrap/unwrap이 가능하다(gas fee 발생)
	- stETH: ETH stake의 증표이면서 추가적인 보상
	- wstETH: Wrapped stETH - Defi 호환 토큰
- Lido에 100ETH를 스테이킹 하면 즉시 100stETH를 받고 reward로 예치량에 비례해 매일 소량의 stETH를 지급받는다.
- 그런데 매일 보상 받는다는것이 Lido에서 수많은 고객들에게 매일 트랜잭션을 발생시키는 것이 아니다(성능도 가스비도 문제일 것이다).
- rebasing token 이라고도 하는데 ERC20의 `balanceOf(addres)`를 단순 getter 형태로 구현하지 않고 **약간의 계산을 해서 돌려주는 방식**이다.
- `stETH`의 `balanceOf()`가 동적인 값을 주기 때문에 이를 기대하지 않은 기존 DEFI 서비스에 호환이 안되는 경우가 많다. 따라서 일반적인(시간이 지나도 `balanceOf()`값이 변하지 않는) ERC20 토큰이 wstETH이다. 물론 보상은 여전히 받아야 하기 때문에 wstETH의 잔액은 고정되지만 stETH와의 변환비가 지속적으로 상승한다.

## StETH.sol (lido-dao)
https://github.com/lidofinance/lido-dao/blob/master/contracts/0.4.24/StETH.sol
```solidity
/**
 * @return the amount of tokens owned by the `_account`.
 *
 * @dev Balances are dynamic and equal the `_account`'s share in the amount of the
 * total Ether controlled by the protocol. See `sharesOf`.
 */
function balanceOf(address _account) external view returns (uint256) {
	return getPooledEthByShares(_sharesOf(_account));
}
```

## wstETH / stETH
이 둘은 linear하게 증가한다. <https://data.chain.link/optimism/mainnet/crypto-eth/wsteth-steth%20exchangerate> 에서 확인 가능하다.
![[notes/images/wstETH2stETH.png]]

---
- [[tags/Ethereum|Ethereum]]
