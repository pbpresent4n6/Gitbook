---
cover: .gitbook/assets/Bitcoin_Trading_Network_4K_HD_1366x768 (1).jpg
coverY: 59
---

# 비트코인 주소 클러스터링 휴리스틱

## 1. 주소 클러스터링이 중요한 이유



암호화폐 트랜잭션 추적이 가능하기 위해서 먼저 수행되어야 하는 것은 암호화폐 주소에 대한 그룹 식별과 클러스터링이다.

블록체인 네트워크 상의 데이터인 on-chain 데이터와 소셜 네트워크나 웹 등에 공개되어 있는 데이터인 OSINT, HUMINT를 통해 얻을 수 있는 데이터가 적절하게 조화될 수록 암호화폐 추적이 용이해진다.

OSINT, HUMINT 정보를 통해 특정 그룹에 속한 주소를 식별하는 경우는 다음의 예시로 들 수 있다.

* 랜섬웨어 공격 과정 분석을 통해 특정 그룹으로 식별했을 경우, 몸값 주소
* SNS, 웹 등에 공개된 거래소 소유의 주소
* VASP의 협조를 통해 획득한 주소
* ...

위와 같은 정보를 통해 동일한 그룹에 포함되는 주소들끼리 클러스터링 할 수 있을 것이다.

비교적 정확한 정보를 얻을 수 있는 OSINT, HUMINT를 통한 방법과 달리, on-chain 상에서의 클러스터링은 그 사실이 100% 보장되지 않는 휴리스틱에 의존한다.

UTXO 모델을 기반으로 하는 비트코인은 트랜잭션을 수행했을 때, 지불 금액과 전송할 UTXO의 크기가 일치하지 않을 때, 차액에 해당하는 UTXO를 돌려받는다.

현재 비트코인 생태계에서는 차액으로 인한 UTXO를 돌려받을 때, 특수한 경우를 제외하면 주소 하나를 새로 생성해서 해당 주소로 돌려받는 것을 권장하고 있으며, 대부분의 시스템이 이를 지원하고 있다.

이 때 생성되는 주소를 잔금(change) 주소라고 한다.

그리고 사용자의 의도로 인해 비트코인을 전송받는 주소를 지불(payment) 주소라고 한다.

change 주소와 payment 주소를 합쳐서 출력(output)주소라고 하겠다.

비트코인을 전송하는 주소는 input, source, send 등 다양한 방법으로 표현할 수 있는데, 본 글에서는 입력(input) 주소라고 하겠다.



<figure><img src=".gitbook/assets/image (3) (2).png" alt=""><figcaption><p>[그림 1] 가장 일반적인 비트코인 트랜잭션 형태</p></figcaption></figure>



가장 일반적인 비트코인 트랜잭션의 형태 중 하나는 입력 주소 1개, 지불 주소 1개, 잔금 주소 1개를 가지는 형태이며, 위와 같은 그래프로 표현될 수 있다.

이와 같은 트랜잭션 형태는 최근 블록에 포함된 트랜잭션들 중에서 50%에 가까운 비중을 차지하고 있다.([transactionfee.info](https://transactionfee.info/charts/transactions-1in-2out/))

위 그래프는 다음과 같이 2가지 방법으로 해석할 수 있을 것이다.

* <mark style="background-color:blue;">bc1qvjg4ctfsvqgjr4e3rkstz7ve52g98ame3azxm8</mark> 주소로부터 0.00490078 BTC가 <mark style="background-color:purple;">1FVtPvTnUuiDr6ZZubj9yZgkV3YRBkMB4o</mark> 주소로 전송되고, 수수료를 제외한 차액인 0.00007654 BTC가 <mark style="background-color:orange;">bc1qel2agpm8cxktt86mqzr599ejg5yqpfkxp8v9w4</mark> 주소로 전송되었다.
* <mark style="background-color:blue;">bc1qvjg4ctfsvqgjr4e3rkstz7ve52g98ame3azxm8</mark> 주소로부터 0.00007654 BTC가 <mark style="background-color:orange;">bc1qel2agpm8cxktt86mqzr599ejg5yqpfkxp8v9w4</mark> 주소로 전송되고, 수수료를 제외한 차액인 0.00490078 BTC가 <mark style="background-color:purple;">1FVtPvTnUuiDr6ZZubj9yZgkV3YRBkMB4o</mark> 주소로 전송되었다.



첫 단추를 잘 끼워야 한다는 말이 있듯이, 잔금 주소를 어떤 주소로 식별하는지에 따라 이후 트랜잭션 분석에서 올바른 결과가 도출될지, 완전히 잘못된 결과가 도출될지 결정된다.

위와 같은 이유로 비트코인의 익명성을 강화하기 위해서 주소 재사용(잔금 주소로 입력 주소를 사용하는  것;address reuse)을 방지하고, 새 주소를 생성하거나 기존에 생성된 다른 주소를 이용해서 잔금 주소로 활용하는 것이다.

따라서, on-chain 데이터를 통한 비트코인 트랜잭션 분석의 첫 걸음은 잔금 주소를 식별하는 것으로부터 시작된다.



## 2. 비트코인 클러스터링 휴리스틱



본 글에서는 비트코인 on-chain 데이터를 가지고 적용할 수 있는 몇 가지 휴리스틱을 소개하고자 한다.



### 2-1) 주소 재사용

<figure><img src=".gitbook/assets/image (2).png" alt=""><figcaption><p>[그림 2] 비트코인 휴리스틱 1 - 주소 재사용</p></figcaption></figure>



잔금 주소를 새로 생성하는 것을 권장하고 있지만, 일부 지갑 프로그램에서는 입력 주소를 재사용하고 있다.

\[그림 2]를 보면 입력 주소와 2번째 출력 주소가 같은 것을 알 수 있다. 이 때, 첫 번째 출력 주소를 지불 주소로 판단할 수 있다.



### 2-2) 동일한 주소 포맷

<figure><img src=".gitbook/assets/image (14).png" alt=""><figcaption><p>[그림 3] 비트코인 휴리스틱 2 - 동일한 주소 포맷 사용</p></figcaption></figure>



대부분의 시스템에서 입력 주소와 잔금 주소는 동일한 포맷을 사용한다.

\[그림 3]에서 입력 주소는 1로 시작하는 P2PKH 타입이며, 출력 주소는 bc1q로 시작하는 P2WPKH와 1로 시작하는 P2PKH 타입이다. 이 때, 2번째 출력주소가 입력 주소와 동일한 포맷을 사용하기 때문에 잔금 주소로 볼 수 있다.

비트코인은 크게 4가지 주소 형식을 사용하는 것으로 널리 알려져 있으며, 다음과 같다.

* 1 로 시작하는 P2PKH Format
* 3 으로 시작하는 P2SH Format
* bc1q 로 시작하는 P2WPKH Format
* bc1p 로 시작하는 P2TR Format



### 2-3) 트랜잭션 이전 기록이 없는 주소

<figure><img src=".gitbook/assets/image (7).png" alt=""><figcaption><p>[그림 4] 비트코인 휴리스틱 3 - 트랜잭션 이전 기록이 없는 주소</p></figcaption></figure>



A 트랜잭션이 발생했을 때, 출력 주소 중 하나는 A 트랜잭션 발생 이전 트랜잭션 내역이 존재하지만 다른 출력 주소는 A 트랜잭션이 첫 번째 트랜잭션일 경우 잔금 주소로 판단하는 방법이다.

\[그림 4] 트랜잭션의 경우, 첫 번째 출력 주소에서 \[그림 4] 트랜잭션 보다 먼저 발생한 트랜잭션이 있는 것을 확인할 수 있지만, 두 번째 출력 주소는 \[그림 4] 트랜잭션이 첫 번째 트랜잭션이기 때문에 잔금 주소로 볼 수 있다.

* [\[그림 4\] 트랜잭션](https://www.blockchain.com/explorer/transactions/btc/f122ced0a8400d97b5c67fe609d86b181c6b8ea49e65cb2e867ddd96c57b0f95)
* [첫 번째 출력 주소](https://www.blockchain.com/explorer/addresses/btc/1CYkZ5aNdMbRtzpExTpqw99pdMg2nkeXmU)
* [두 번째 출력 주소](https://www.blockchain.com/explorer/addresses/btc/1FgJMt7MhYorHnd6gtHTpNwzeKosucjPrZ)



### 2-4) 어림수 (Round Number)

<figure><img src=".gitbook/assets/image.png" alt=""><figcaption><p>[그림 5] 비트코인 휴리스틱 4 - 어림수 (Round Number)</p></figcaption></figure>



어림수는 버림, 올림, 반올림 등을 통해 얻은 딱 떨어지는 수를 의미한다.

사람의 특성 상 깔끔하게 떨어지는 액수를 보낼 확률이 높은 것에 기반한 휴리스틱으로, 출력 주소 중 어림수가 전송된 주소를 지불 주소로 판단하는 방법이다.

\[그림 5] 트랜잭션에서는 0.00349588 BTC보다는 깔끔하게 떨어지는 0.0005 BTC를 보낸 첫 번째 출력 주소를 지불 주소로 판단할 수 있다.



### 2-5) 같은 속성의 주소

<figure><img src=".gitbook/assets/image (5).png" alt=""><figcaption><p>[그림 6] 비트코인 휴리스틱 5 - 같은 속성의 지갑 사용</p></figcaption></figure>



출력 주소 중 입력 주소와 같은 속성을 사용하는 주소가 있을 경우(다중 서명 등), 해당 출력 주소를 잔금 주소로 판단하는 방법이다.

\[그림 6]은 입력 주소와 첫 번째 출력 주소 모두 다중 서명 지갑 주소이지만, 두 번째 출력 주소는 Legacy 주소이기 때문에 지불 주소로 볼 수 있다.

다중 서명 지갑 주소 판단은 다음과 같은 방법으로 할 수 있다.

* [https://bitcointalk.org/index.php?topic=5279353.0](https://bitcointalk.org/index.php?topic=5279353.0)

<figure><img src=".gitbook/assets/image (15).png" alt=""><figcaption><p>[그림 7] oxt.me 사이트에서 트랜잭션 조회</p></figcaption></figure>



또는 [oxt.me](https://oxt.me)와 같은 사이트에서 트랜잭션을 조회했을 때 태깅되는 정보로 확인할 수 있다.



2-6)&#x20;











































위에서 언급한 휴리스틱들을 바탕으로 일부 트랜잭션 조회 사이트나 암호화폐 추적 솔루션에서는 트랜잭션에 잔금 주소를 식별해주기도 한다.

하지만 잔금 주소 식별은 어디까지나 휴리스틱에 의존하는 것이기 때문에 100% 신뢰해선 안된다는 것을 명심할 필요가 있다.





































