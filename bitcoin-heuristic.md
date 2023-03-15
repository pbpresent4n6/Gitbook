---
cover: .gitbook/assets/Bitcoin_Trading_Network_4K_HD_1366x768 (1).jpg
coverY: 59
---

# 비트코인 주소 클러스터링과 휴리스틱

## 1. 주소 식별과 클러스터링



암호화폐 트랜잭션 추적이 가능하기 위해서 먼저 수행되어야 하는 것은 암호화폐 주소에 대한 그룹 식별과 클러스터링이다.

블록체인 네트워크 상의 데이터인 on-chain 데이터와 소셜 네트워크나 웹 등에 공개되어 있는 데이터인 OSINT, HUMINT를 통해 얻을 수 있는 데이터가 적절하게 조화될 수록 암호화폐 추적이 용이해진다.

OSINT, HUMINT 정보를 통해 특정 그룹에 속한 주소를 식별하는 경우는 다음의 예시로 들 수 있다.

* 랜섬웨어 공격 과정 분석을 통해 특정 그룹으로 식별했을 경우, 몸값 주소
* SNS, 웹 등에 특정 집단이 소유한 것으로 공개된 주소
* VASP의 협조를 통해 획득한 주소
* ...

위와 같은 정보를 통해 동일한 그룹에 포함되는 주소들끼리 클러스터링 할 수 있을 것이다.



<figure><img src=".gitbook/assets/image.png" alt=""><figcaption><p>[그림 1] 클러스터링이 적용되지 않은 그래프</p></figcaption></figure>

<figure><img src=".gitbook/assets/image (2).png" alt=""><figcaption><p>[그림 2] 클러스터링이 적용된 그래프</p></figcaption></figure>



\[그림 1], \[그림 2]와 같이 클러스터링이 적용된 것과 되지 않은 것의 차이는 분석 시 유의미한 차이를 만든다. 클러스터링에 따라 홉 수의 차이가 발생하기 때문에 자금 출처를 분석할 때, 특정 주소와 이전 트랜잭션에서 확인할 수 있는 주소가 강한 연관성을 가지고 있는지 판단하는데 영향을 미치기 때문이다.

\[그림 1]에서는 Victim으로부터 Exchange까지의 홉 수가 4이기 때문에 Exchange에 전송된 자금이 범죄에 사용된 주소의 사용자가 속한 조직으로부터 받은 금액인지, 중간 트랜잭션에서 희석되어 정당한 사용자로부터 받은 금액인지 판단하기 어려울 수 있다.

하지만, \[그림 2]와 같이 클러스터링이 적용되었을 때는 홉 수가 2로 줄어들기 때문에 같은 조직으로부터 전송된 자금으로 쉽게 판단할 수 있다.

불법 조직으로 널리 알려진 클러스터에 포함된 주소로부터 자금이 전송되었을 경우, 거래소는 해당 자금을 동결시킬 수도 있을 것이다.



비교적 정확한 정보를 얻을 수 있는 OSINT, HUMINT를 통한 방법과 달리, on-chain 상에서의 클러스터링은 그 사실이 100% 보장되지 않는 휴리스틱에 의존한다.

UTXO 모델을 기반으로 하는 비트코인은 트랜잭션을 수행했을 때, 지불 금액과 전송할 UTXO의 크기가 일치하지 않을 때, 차액에 해당하는 UTXO를 돌려받는다.

현재 비트코인 생태계에서는 차액으로 인한 UTXO를 돌려받을 때, 주소 하나를 새로 생성해서 해당 주소로 돌려받는 것을 권장하고 있으며, 대부분의 시스템이 이를 지원하고 있다. (HD Wallet의 특징 중 하나)

이 때 생성되는 주소를 잔금(change) 주소라고 한다.

그리고 사용자의 의도로 인해 비트코인을 전송받는 주소를 지불(payment) 주소라고 한다.

본 글에서는 change 주소와 payment 주소를 합쳐서 출력(output) 주소라고 하겠다.

비트코인을 전송하는 주소는 input, source, send 등 다양한 방법으로 표현할 수 있는데, 입력(input) 주소라고 하겠다.



<figure><img src=".gitbook/assets/image (3) (2).png" alt=""><figcaption><p>[그림 3] 가장 일반적인 비트코인 트랜잭션 형태</p></figcaption></figure>



가장 일반적인 비트코인 트랜잭션의 형태 중 하나는 입력 주소 1개, 지불 주소 1개, 잔금 주소 1개를 가지는 형태이며, 위와 같은 그래프로 표현될 수 있다.

이와 같은 트랜잭션 형태는 최근 블록에 포함된 트랜잭션들 중에서 50%에 가까운 비중을 차지하고 있다.([transactionfee.info](https://transactionfee.info/charts/transactions-1in-2out/))

위 그래프는 다음과 같이 2가지 방법으로 해석할 수 있을 것이다.

* <mark style="background-color:blue;">bc1qvjg4ctfsvqgjr4e3rkstz7ve52g98ame3azxm8</mark> 주소로부터 0.00490078 BTC가 <mark style="background-color:purple;">1FVtPvTnUuiDr6ZZubj9yZgkV3YRBkMB4o</mark> 주소로 전송되고, 수수료를 제외한 차액인 0.00007654 BTC가 <mark style="background-color:orange;">bc1qel2agpm8cxktt86mqzr599ejg5yqpfkxp8v9w4</mark> 주소로 전송되었다.
* <mark style="background-color:blue;">bc1qvjg4ctfsvqgjr4e3rkstz7ve52g98ame3azxm8</mark> 주소로부터 0.00007654 BTC가 <mark style="background-color:orange;">bc1qel2agpm8cxktt86mqzr599ejg5yqpfkxp8v9w4</mark> 주소로 전송되고, 수수료를 제외한 차액인 0.00490078 BTC가 <mark style="background-color:purple;">1FVtPvTnUuiDr6ZZubj9yZgkV3YRBkMB4o</mark> 주소로 전송되었다.



첫 단추를 잘 끼워야 한다는 말이 있듯이, 잔금 주소를 어떤 주소로 식별하는지에 따라 이후 트랜잭션 분석에서 올바른 결과가 도출될지, 완전히 잘못된 결과가 도출될지 결정된다.

위와 같은 이유로 비트코인의 익명성을 강화하기 위해서 주소 재사용(잔금 주소로 입력 주소를 사용하는  것;address reuse)을 방지하고, 새 주소를 생성하거나 기존에 생성된 다른 주소를 이용해서 잔금 주소로 활용하는 것이다.

따라서, on-chain 데이터를 통한 비트코인 트랜잭션 분석의 첫 걸음은 잔금 주소를 식별하는 것으로부터 시작된다.



## 2. 비트코인 휴리스틱



본 글에서는 비트코인 on-chain 데이터를 가지고 적용할 수 있는 잔금 주소 식별을 포함한 몇 가지 휴리스틱을 소개하고자 한다.



### 2-1) 주소 재사용

<figure><img src=".gitbook/assets/image (2) (1).png" alt=""><figcaption><p>[그림 4] 비트코인 휴리스틱 1 - 주소 재사용</p></figcaption></figure>



잔금 주소를 새로 생성하는 것을 권장하고 있지만, 일부 지갑 프로그램에서는 입력 주소를 재사용하고 있다.

\[그림 4]를 보면 입력 주소와 2번째 출력 주소가 같은 것을 알 수 있다. 이 때, 첫 번째 출력 주소를 지불 주소로 판단할 수 있다.

* [\[그림 4\] 트랜잭션](https://www.blockchain.com/explorer/transactions/btc/167db4b77c1a5ed21d78c73d94275b61d061ac9e626109aac7df856b22b67821)



### 2-2) 동일한 주소 포맷

<figure><img src=".gitbook/assets/image (14).png" alt=""><figcaption><p>[그림 5] 비트코인 휴리스틱 2 - 동일한 주소 포맷</p></figcaption></figure>



대부분의 시스템에서 입력 주소와 잔금 주소는 동일한 포맷을 사용하는 경향이 있는 점에서 비롯된 휴리스틱으로, 강한 휴리스틱 중 하나이다.

\[그림 5]에서 입력 주소는 1로 시작하는 P2PKH 타입이며, 출력 주소는 bc1q로 시작하는 P2WPKH와 1로 시작하는 P2PKH 타입이다. 이 때, 2번째 출력주소가 입력 주소와 동일한 포맷을 사용하기 때문에 잔금 주소로 볼 수 있다.

* [\[그림 5\] 트랜잭션](https://www.blockchain.com/explorer/transactions/btc/d50db1c12fbdad40a9c97619c6ed3cb4fa7077de1b3014bd3521ab1f5c8b3e07)

비트코인은 크게 4가지 주소 형식을 사용하는 것으로 널리 알려져 있으며, 다음과 같다.

* 1 로 시작하는 P2PKH Format
* 3 으로 시작하는 P2SH Format
* bc1q 로 시작하는 P2WPKH Format
* bc1p 로 시작하는 P2TR Format



### 2-3) 트랜잭션 이전 기록이 없는 주소

<figure><img src=".gitbook/assets/image (7).png" alt=""><figcaption><p>[그림 6] 비트코인 휴리스틱 3 - 트랜잭션 이전 기록이 없는 주소</p></figcaption></figure>



A 트랜잭션이 발생했을 때, 출력 주소 중 하나는 A 트랜잭션 발생 이전 트랜잭션 내역이 존재하지만 다른 출력 주소는 A 트랜잭션이 첫 번째 트랜잭션일 경우 잔금 주소로 판단하는 방법이다.

\[그림 6] 트랜잭션의 경우, 첫 번째 출력 주소에서 \[그림 6] 트랜잭션 보다 먼저 발생한 트랜잭션이 있는 것을 확인할 수 있지만, 두 번째 출력 주소는 \[그림 6] 트랜잭션이 첫 번째 트랜잭션이기 때문에 잔금 주소로 볼 수 있다.

* [\[그림 6\] 트랜잭션](https://www.blockchain.com/explorer/transactions/btc/f122ced0a8400d97b5c67fe609d86b181c6b8ea49e65cb2e867ddd96c57b0f95)
* [첫 번째 출력 주소](https://www.blockchain.com/explorer/addresses/btc/1CYkZ5aNdMbRtzpExTpqw99pdMg2nkeXmU)
* [두 번째 출력 주소](https://www.blockchain.com/explorer/addresses/btc/1FgJMt7MhYorHnd6gtHTpNwzeKosucjPrZ)



### 2-4) 어림수 (Round Number)

<figure><img src=".gitbook/assets/image (8).png" alt=""><figcaption><p>[그림 7] 비트코인 휴리스틱 4 - 어림수 (Round Number)</p></figcaption></figure>



어림수는 버림, 올림, 반올림 등을 통해 얻은 딱 떨어지는 수를 의미한다.

사람의 특성 상 깔끔하게 떨어지는 액수를 보낼 확률이 높은 것에 기반한 휴리스틱으로, 출력 주소 중 어림수가 전송된 주소를 지불 주소로 판단하는 방법이다.

\[그림 7] 트랜잭션에서는 0.00349588 BTC보다는 깔끔하게 떨어지는 0.0005 BTC를 보낸 첫 번째 출력 주소를 지불 주소로 판단할 수 있다.

* [\[그림 7\] 트랜잭션](https://www.blockchain.com/explorer/transactions/btc/7f57b612e30c77ba76de09ef6654456746c36abf696ff9d6d5baf97d06dbb842)



### 2-5) 다중 서명 주소

<figure><img src=".gitbook/assets/image (5) (2).png" alt=""><figcaption><p>[그림 8] 비트코인 휴리스틱 5 - 다중 서명 주소</p></figcaption></figure>



입력 주소가 다중 서명 주소이고, 출력 주소 중 하나가 다중 서명 주소이고 입력 주소와 같은 속성을 가질 때(2/3, 3/5 등), 해당 출력 주소를 잔금 주소로 판단하는 방법이다.

\[그림 8]은 입력 주소와 첫 번째 출력 주소 모두 다중 서명 지갑 주소이지만, 두 번째 출력 주소는 Legacy 주소이기 때문에 지불 주소로 볼 수 있다.

* [\[그림 8\] 트랜잭션](https://www.blockchain.com/explorer/transactions/btc/8d0d9e682bbb98af4231389a232fdf331e8f47ab60f0416f5b8853a84af6791f)

다중 서명 지갑 주소 판단은 다음과 같은 방법으로 할 수 있다.

* [https://bitcointalk.org/index.php?topic=5279353.0](https://bitcointalk.org/index.php?topic=5279353.0)

<figure><img src=".gitbook/assets/image (15).png" alt=""><figcaption><p>[그림 9] oxt.me 사이트에서 트랜잭션 조회</p></figcaption></figure>



또는 [oxt.me](https://oxt.me)와 같은 사이트에서 트랜잭션을 조회했을 때 태깅되는 정보로 확인할 수 있다.



### 2-6) 공동 입력 소유권 (Common Input Ownership)

<figure><img src=".gitbook/assets/image (1) (3).png" alt=""><figcaption><p>[그림 10] 비트코인 휴리스틱 6 - 공동 입력 소유권 (Common Input Ownership)</p></figcaption></figure>



최근 대부분의 비트코인 지갑은 계층적 결정론적(Hierarchical Deterministic) 지갑 구조를 가지고 있다.

HD Wallet은 단일 마스터 시드키를 통해 하위 개인/공용 키 및 관련 주소를 생성한다.

계층적 구조에 의해 하나의 지갑에는 다수의 주소가 포함될 수 있다는 의미이다.

이와 같은 사실을 근거로 공동 입력 소유권 휴리스틱이 등장하게 되었다. 공동 입력 소유권 휴리스틱은 각 주소가 동일한 개인키 또는 지갑 소프트웨어에 의해 제어된다고 가정하는 것이다.

한 마디로 하나의 트랜잭션에서 모든 입력 주소의 소유자를 같다고 판단하는 것으로, 비교적 강력한 휴리스틱으로 평가받고 있다.

주의할 점으로 다수의 입력 주소가 존재할 수 있는 트랜잭션 형태인 coinjoin, payjoin과 구분해야 한다.

* [\[그림 10\] 트랜잭션](https://www.blockchain.com/explorer/transactions/btc/8b4b8757b2f09d8f15ab1eb9cbcca2e3faaf9a45a34490a255efa19aeb2911db)



### 2-7) 가장 큰 입력 금액

<figure><img src=".gitbook/assets/image (37).png" alt=""><figcaption><p>[그림 11] 비트코인 휴리스틱 7 - 가장 큰 입력 금액</p></figcaption></figure>



입력 주소의 금액들 중 최댓값이 출력 주소의 금액들 중 최댓값보다 작으면, 해당 값을 받은 주소를 지불 주소로 판단하는 방법이다.

UTXO 모델을 사용하는 비트코인의 특성 상 전송 금액을 감당할 수 있을 만한 크기의 UTXO가 없을 경우, 적은 금액을 가지는 다수의 UTXO들을 모아서 지불하는 것을 근거로 한 휴리스틱이다.

\[그림 11] 트랜잭션에서 입력 금액의 최댓값은 0.02184592인데, 지불 금액의 최댓값은 0.10104000 BTC이기 때문에 0.10104000 BTC를 받는 주소를 지불 주소로 볼 수 있다.

* [\[그림 11\] 트랜잭션](https://www.blockchain.com/explorer/transactions/btc/e019c56f3e39d2baf8849d435b99e6940155a0ba23c92f3a241605a23164686a)



### 2-8) 가장 큰 출력 금액

<figure><img src=".gitbook/assets/image (6).png" alt=""><figcaption><p>[그림 12] 비트코인 휴리스틱 8 - 가장 큰 출력 금액</p></figcaption></figure>



출력 금액 중 가장 큰 금액을 받은 주소를 잔금 주소로 판단하는 방법으로, 가장 약한 휴리스틱 중 하나이다.

적은 금액을 받은 출력 주소가 다수 있고, 큰 금액을 받은 출력 주소가 하나 있는 상황에서 고려해볼 수 있다.

\[그림 12] 트랜잭션에서는 더 큰 금액을 받은 두 번째 출력 주소를 잔금 주소로 볼 수 있다.

* [\[그림 12\] 트랜잭션](https://www.blockchain.com/explorer/transactions/btc/d2622c734f7507d484cb4888df76d6ad2cdf0e0480f57b4684a99037a8f0009f)



### 2-9) 다른 클러스터에 속한 주소

<figure><img src=".gitbook/assets/image (3) (3).png" alt=""><figcaption><p>[그림 13] 비트코인 휴리스틱 9 - 다른 클러스터에 속한 주소</p></figcaption></figure>



출력 주소 중 하나가 이미 다른 클러스터에 속해있는 주소일 때, 해당 주소를 지불 주소로 판단하는 휴리스틱이다.

OSINT, HUMINT 등의 정보를 통해 이미 클러스터에 속해있는지 확인할 수 있다.

\[그림 13] 트랜잭션은 첫 번째 출력 주소가 랜섬웨어에 사용된 주소로 기존에 알려져 있기 때문에 지불 주소로 볼 수 있다.

* [\[그림 13\] 트랜잭션](https://www.blockchain.com/explorer/transactions/btc/9975160cda28797ca6a6c55bc4f0a4f4a69e25b035c420cd9a687f8b548b7ae0)



### 2-10) 트랜잭션 속성 분석

<figure><img src=".gitbook/assets/image (2) (3).png" alt=""><figcaption><p>[그림 14] 비트코인 휴리스틱 10 - 트랜잭션 속성 분석</p></figcaption></figure>



동일한 지갑 서비스일 경우 동일한 트랜잭션 속성을 가질 것이라는 가정에 기반한 휴리스틱이다.

\[그림 14]와 같이 입력 주소와 출력 주소의 포맷이 모두 같고, 어림수 휴리스틱도 적용하기 어려운 경우에 고려할 수 있다.



<figure><img src=".gitbook/assets/image (4) (2).png" alt=""><figcaption><p>[그림 15] QLUE로 확인한 [그림 14] 트랜잭션</p></figcaption></figure>



A 트랜잭션이 발생했을 때, A 트랜잭션의 출력 주소가 입력 주소가 되는 트랜잭션 B, C의 속성과 A 트랜잭션의 속성이 같은지 비교하는 방법이다.



<figure><img src=".gitbook/assets/image (3) (4).png" alt=""><figcaption><p>[그림 16] [그림 14] 트랜잭션 정보</p></figcaption></figure>

<figure><img src=".gitbook/assets/image (4).png" alt=""><figcaption><p>[그림 17] 2f3c8f0838a3ee190d1c4f043dbe541952df15b5437a96449b74e1d657a60cae 트랜잭션 정보</p></figcaption></figure>

<figure><img src=".gitbook/assets/image (1).png" alt=""><figcaption><p>[그림 18] e08bca06cab177bf66cb3f533506814f26d005a7fa59592476c7d4d157ed0309 트랜잭션 정보</p></figcaption></figure>



다양한 트랜잭션 속성 중 주목할 부분은 RBF(Replace By Fee), Locktime, Version, Witness 값이다.

연속된 트랜잭션 중에 네 항목의 값이 동일한 트랜잭션이 있다면 같은 지갑 서비스를 사용하고 있을 확률이 높을 것이다.

\[그림 16], \[그림 17], \[그림18]에서 확인할 수 있듯이 RBF, Locktime, Witness 값은 동일한 것을 알 수 있다.

하지만 \[그림 16] 트랜잭션과 e08b-0309 트랜잭션의 Version 값은 1인데, 2f3c-0cae 트랜잭션의 Version 값은 2이기 때문에 지불 주소로 볼 수 있다.

* [\[그림 14, 16\] 트랜잭션](https://www.blockchain.com/explorer/transactions/btc/d01de62cf5794cd8e93a86e3f01dcaa30b3c82540152fc4958e41af3a2c0c2ba)
* [\[그림 17\] 트랜잭션](https://www.blockchain.com/explorer/transactions/btc/2f3c8f0838a3ee190d1c4f043dbe541952df15b5437a96449b74e1d657a60cae)
* [\[그림 18\] 트랜잭션](https://www.blockchain.com/explorer/transactions/btc/e08bca06cab177bf66cb3f533506814f26d005a7fa59592476c7d4d157ed0309)



### 2-11) 그 외

* 믹싱 서비스의 특징을 기반으로 판단할 수 있다. (Wasabi Coinjoin은 bc1q 주소를 가진다 등)
* 일반적으로 수수료는 잔금 주소에서 빠져나간다. mempool을 관찰할 수 있는 경우 수수료가 감소되는 주소를 확인한다.
* 특정 지갑 서비스의 경우 지불 주소를 트랜잭션 vout의 첫 번째 인덱스에 고정하는 경우가 있다. (이러한 점을 개선하기 위해  BIP-0069가 제안되었지만 많은 서비스에서 적용하고 있지 않음)
* Dust Attack을 수행하고, Dust를 받은 주소에서 발생하는 트랜잭션을 통해 클러스터링을 할 수 있다.



## 3. 결론

* 위에서 언급한 휴리스틱들을 바탕으로 일부 트랜잭션 조회 사이트나 암호화폐 추적 솔루션에서는 트랜잭션에 잔금 주소를 식별해주기도 한다.
* 잔금 주소 식별은 어디까지나 휴리스틱에 의존하는 것이기 때문에 100% 신뢰해선 안된다는 것을 명심할 필요가 있다.
* 여러 휴리스틱을 동시에 적용 가능할 수 있다면 더 신뢰할 수 있을 것이다.
* 휴리스틱만으로는 암호화폐 추적이 어려우며, OSINT 및 HUMINT를 통해 얻은 정보와 결합해서 분석한다면 강력하게 작용할 수 있을 것이다.

