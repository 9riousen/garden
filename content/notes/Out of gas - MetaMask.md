---
title: "Out of gas - MetaMask"
date: '2023-02-06'
images: ['https://metamask.zendesk.com/hc/article_attachments/360048240852/Why-did-my-transaction-fail-with-an-out-of-gas-error_image2.gif']
---
![out-of-gas](https://metamask.zendesk.com/hc/article_attachments/360048279551/Why-did-my-transaction-fail-with-an-out-of-gas-error_image1.png)
이건 당신이 지정한 gas limit 때문에 transaction이 끝까지 수행되지 못하였단 이야기다
gas limit을 높여서 재시도 해야한다

## MetaMask팀의 조언
대부분의 경우 MetaMask가 자동으로 gas limit을 설정하며 이는 충분하다
gas limit값의 지정은 개인 마음이지만 최근 성공적인 smart contract의 성공 사례를 참고하면 좋다
![out of gas - metamask](https://metamask.zendesk.com/hc/article_attachments/360048240852/Why-did-my-transaction-fail-with-an-out-of-gas-error_image2.gif)

추천 스텝:
1. Etherscan에서 당신의 'out of gas'를 찾아 contract address를 알아낸다(To address)
2. 해당 컨트랙트의 tx list를 보고 성공한 transaction의 Txn Hash를 찾는다
3. 'Click to see More'를 보고 Gas limit을 적어두고 따라서 재시도한다

---
- [[tags/Ethereum]]
- [Why did my transaction fil with an "Out of Gas" error? How can I fix it?](https://metamask.zendesk.com/hc/en-us/articles/360038849792-Why-did-my-transaction-fail-with-an-Out-of-Gas-error-How-can-I-fix-it-)