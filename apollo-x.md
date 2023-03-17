---
cover: .gitbook/assets/그림4.png
coverY: 24
---

# Apollo X 거래소 해킹 공격자 주소 추적

1\. 사건 개요

<figure><img src=".gitbook/assets/image (1).png" alt=""><figcaption><p>[그림 1] Apollo X 거래소 해킹 관련 <a href="http://coinreaders.com/35680">coinreaders </a>기사</p></figcaption></figure>



### 1-1) 공격 관련

* 2022년 6월 8일 19시 경(UTC+8) Apollo X 거래소 대상으로 공격 발생
* 공격자의 ETH 주소 - 0x9e532b19abd155ae5ced76ca2a206a732c68f261
* ApolloxExchangeTreasury의 claim() 함수를 반복적으로 호출하여 계약에서 약 5,300만 APX 토큰을 획득(서명 확인 취약점)
* claim() 함수는 ECDSA.recover()로 입력 메시지와 서명을 성공적으로 검증하고 계약에서 공격자에게 해당 토큰 양을 전송
* 획득한 APX 토큰을 PancakeSwap을 통해 공격 당시 210만 BUSD로 전환
* PancakeSwap 과정 중 총 8건의 트랜잭션 수행
* 확보한 BUSD는 3건의 트랜잭션을 통해 ZAP Bridge를 통해 USDC로 전환
* 자산은 Etherscan으로 전송된 뒤, renBTC로 교환 후 최종적으로 BTC로 전환

{% hint style="info" %}
APX 토큰과 BUSD는 모두 Binance Chain에서 발행된 BEP-20 기반의 토큰이다.
{% endhint %}

{% hint style="info" %}
PancakeSwap은 Binance Chain 상에서 서로 다른 토큰 간의 교환을 가능하게 해주는 일종의 DEX이다.
{% endhint %}

{% hint style="info" %}
ZAP Bridge는 서로 다른 블록체인 간의 토큰 교환을 가능하게 해주는 일종의 프로토콜이다.
{% endhint %}



### 1-2) Apollo X 측의 대응

* 사건 당일 해킹을 당했다고 공식적으로 발표
* 4 시간 동안 DEX에서 출금 기능을 일시적으로 비활성화
* 문제 해결 후 DEX에서 출금 기능 재개
* 거래소 사용자의 자금에는 손실이 없다고 발표
* 거래소 수수료로 얻은 APX를 통해 손실을 만회할 계획이라고 발표



### 1-3) Apollo X 트위터 공식 입장

{% embed url="https://twitter.com/ApolloX_com/status/1534570239177789440?s=20&t=-SGQQ7F3xJYWt-mgCKsCVg" %}
Apollo X 트위터 공식 입장1
{% endembed %}

{% embed url="https://twitter.com/ApolloX_com/status/1534810576198979586" %}
Apollo X 트위터 공식 입장2
{% endembed %}



## 2. Apollo X 거래소에서 유출된 암호화폐 추적



{% embed url="https://docs.google.com/spreadsheets/d/1uyjVTzuAC76RdgLo0_kSbflqZHL0Z3By/edit?usp=share_link&ouid=103310110257892207500&rtpof=true&sd=true" %}
탈취한 APX를 BUSD로 전환하기까지의 과정
{% endembed %}



공격자가 탈취한 APX 토큰을 BUSD 토큰으로 전환하기까지의 과정은 위 시트와 같이 정리했다.













