---
title: "SVM (Solana Virtual Machine)"
date: '2023-08-14'
images: ['https://framerusercontent.com/images/vM5AODwlWSCoi0g1PXYWEizO6CQ.png']
---
![SVM](https://framerusercontent.com/images/vM5AODwlWSCoi0g1PXYWEizO6CQ.png)

- Ethereum : EVM = Solana : SVM
- 수천 TPS의 성능을 보인다 주장
## Sealevel
![Sealevel](https://framerusercontent.com/images/WQ3GqQbX2oKdsU3k8wXyeojmR0.png)

![EVM](https://framerusercontent.com/images/wM6JMqpBEKltqoNXFc54UHdLnwY.png)

- Sealevel(해수면?) 이라는 병렬화 엔진 탑재
- 여러 contract를 병렬로 실행시킨다. (EVM은 하나씩 실행한다)
	- EVM은 single threded라서 multi-core CPU를 활용 못함
- Solana의 contract는 실행되는 동안 어떤 데이터(state)를 읽고 쓰는지 기재(describe)하기 때문에 가능
---
- [[tags/Blockchain|Blockchain]]
- [What is SVM - The Solana Virtual Machine - squards.so](https://squads.so/blog/solana-svm-sealevel-virtual-machine)
