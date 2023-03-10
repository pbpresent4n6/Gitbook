# 비트코인 주소 클러스터링 휴리스틱

암호화폐 트랜잭션의 추적이 가능하기 위해서 먼저 수행되어야 하는 것은 암호화폐 주소에 대한 그룹 식별과 클러스터링이다.

블록체인 네트워크 상의 데이터인 on-chain 데이터와 소셜 네트워크나 웹 등에 공개되어 있는 데이터인 OSINT, HUMINT를 통해 얻을 수 있는 데이터가 적절하게 조화될 수록 암호화폐 추적이 용이해진다.

OSINT, HUMINT 정보를 통해 특정 그룹에 속한 주소를 식별하는 경우는 다음의 예시로 들 수 있다.

* 랜섬웨어 공격 과정 분석을 통해 특정 그룹으로 식별했을 경우, 몸값 주소
* SNS, 웹 등에 공개된 거래소 소유의 주소
* VASP의 협조를 통해 획득한 주소
* ...

위와 같은 정보를 통해 동일한 그룹에 포함되는 주소들끼리 클러스터링 할 수 있을 것이다.

비교적 정확한 정보를 얻을 수 있는 OSINT, HUMINT를 통한 방법과 달리, on-chain 상에서의 클러스터링은 그 사실이 100% 보장되지 않는 휴리스틱에 의존한다.

UTXO 구조를 기반으로 하는 비트코인은 트랜잭션을 수행했을 때, 지불 금액과 전송할 UTXO의 크기가 일치하지 않을 때, 차액에 해당하는 UTXO를 돌려받는다.

현재 비트코인 생태계에서는 차액으로 인한 UTXO를 돌려받을 때, 특수한 경우를 제외하면 주소 하나를 새로 생성해서 해당 주소로 돌려받는 것이 대부분이다.

이 때 생성되는 주소를 change 주소라고 한다. (본 글에서는 잔금 주소라고 하겠다.)

그리고 사용자의 의도로 인해 비트코인을 받는 주소를 payment 주소라고 한다. (본 글에서는 지불 주소라고 하겠다.)

비트코인을 전송하는 주소는 input, source, send 등 다양한 방법으로 표현할 수 있겠지만, 본 글에서는 입력 주소라고 하겠다.



<figure><img src=".gitbook/assets/image (3).png" alt=""><figcaption><p>[그림 1] 가장 일반적인 비트코인 트랜잭션 형태</p></figcaption></figure>



가장 일반적인 비트코인 트랜잭션의 형태는 입력 주소 1개, 지불 주소 1개, 잔금 주소 1개를 가지는 형태이며, 위와 같은 그래프로 표현될 수 있다.

위 그래프는 다음과 같이 2가지 방법으로 해석할 수 있을 것이다.

* <mark style="background-color:blue;">bc1qvjg4ctfsvqgjr4e3rkstz7ve52g98ame3azxm8</mark> 주소로부터 0.00490078 BTC가 <mark style="background-color:purple;">1FVtPvTnUuiDr6ZZubj9yZgkV3YRBkMB4o</mark> 주소로 전송되고, 수수료를 제외한 차액인 0.00007654 BTC가 <mark style="background-color:orange;">bc1qel2agpm8cxktt86mqzr599ejg5yqpfkxp8v9w4</mark> 주소로 전송되었다.
* <mark style="background-color:blue;">bc1qvjg4ctfsvqgjr4e3rkstz7ve52g98ame3azxm8</mark> 주소로부터 0.00007654 BTC가 <mark style="background-color:orange;">bc1qel2agpm8cxktt86mqzr599ejg5yqpfkxp8v9w4</mark> 주소로 전송되고, 수수료를 제외한 차액인 0.00490078 BTC가 <mark style="background-color:purple;">1FVtPvTnUuiDr6ZZubj9yZgkV3YRBkMB4o</mark> 주소로 전송되었다.



첫 단추를 잘 끼워야 한다는 말이 있듯이, 잔금 주소를 어떤 주소로 식별하는지에 따라 이후 트랜잭션 분석에서 올바른 결과가 도출될지, 완전히 잘못된 결과가 도출될지 결정될 것이다.

따라서, on-chain 데이터를 통한 비트코인 트랜잭션 분석의 첫 걸음은 잔금 주소를 식별하는 것으로부터 시작된다.



본 글에서는 비트코인 on-chain 데이터를 가지고 적용할 수 있는 몇 가지 휴리스틱을 소개하고자 한다.

































