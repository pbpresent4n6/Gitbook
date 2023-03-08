# 16sYqXancDDiijcuruZecCkdBDwDf4vSEC

## 1. 16sYqXancDDiijcuruZecCkdBDwDf4vSEC 지갑 주소 정보

<figure><img src="../.gitbook/assets/image (44).png" alt=""><figcaption><p>[그림 1] 16sYqXancDDiijcuruZecCkdBDwDf4vSEC 지갑 주소 정보</p></figcaption></figure>

QLUE에서 조회한 16sYqXancDDiijcuruZecCkdBDwDf4vSEC 지갑 주소의 요약 정보는 위와 같다.

|               목록               |                  값                 |
| :----------------------------: | :--------------------------------: |
|          Address Hash          | 16sYqXancDDiijcuruZecCkdBDwDf4vSEC |
|          Balance (BTC)         |                  0                 |
|          Transactions          |                  2                 |
|       Cluster Identifier       |              538807739             |
| Number of Addresses in Cluster |                  5                 |
|          BitRank Score         |            0 , High Risk           |
|       Entities and Flags       |    , \[Ransomware, North Korea]    |
|      Received Transactions     |                  1                 |
|        Sent Transactions       |                  1                 |
|      Received Amount (BTC)     |                0.06                |
|        Sent Amount (BTC)       |                0.06                |
|   First Seen Receiving (UTC)   |         2019-07-24 18:51:27        |
|    Last Seen Receiving (UTC)   |         2019-07-24 18:51:27        |
|    First Seen Sending (UTC)    |         2019-07-25 14:56:16        |
|     Last Seen Sending (UTC)    |         2019-07-25 14:56:16        |

해당 지갑 주소는 2019년 7월 24일 18시 51분 경에 처음으로 트랜잭션이 발생했고, 다음 날인 25일 14시 56분 경을 마지막으로 트랜잭션이 확인되지 않는다.

트랜잭션은 송·수신 각 1회씩 총 2번 발생했고, 총 0.06 BTC를 전송했다.

해당 지갑 주소는 Ransomware, North Korea 플래그를 부여 받았다.

Ransomware 공격에 사용되었으며, 고위험 관할군에 속한 지갑 주소이기 때문에 BitRank Score는 0점으로 High Risk이다.

QLUE에서 식별할 수 있는 Cluster 식별 값은 538807739이며, 해당 클러스터에는 5개의 지갑 주소가 포함되어 있다.

## 2. 16sYqXancDDiijcuruZecCkdBDwDf4vSEC 주소 트랜잭션 추적

### 2-1) Output 트랜잭션 추적

<figure><img src="../.gitbook/assets/image (61).png" alt=""><figcaption><p>[그림 2] Binance 거래소로 비트코인 전송</p></figcaption></figure>

1Mq7ak3RKMf2dfC3tkYhDtaa2d8yRiQoFA 지갑 주소로부터 전달 받은 0.06 BTC와 다른 지갑 주소에서 전송된 BTC들이 합쳐져 총 0.298056 BTC가 Binance 거래소로 전송된 것을 확인했다.

전송된 Binance 거래소의 주소는 CISA가 공개한 지갑 주소에 포함되어 있다.

<figure><img src="../.gitbook/assets/image (60).png" alt=""><figcaption><p>[그림 3] 자금이 Hydra Market에서 흘러들어온 모습</p></figcaption></figure>

\[그림 2]의 트랜잭션 input으로 사용된 지갑 주소 중 하나인 1AWhWHDkyvgQic919C8JLJoG1a8NaByuxP 지갑 주소의 트랜잭션을 거슬러 올라가다 보면 Hydra Market에서 자금이 흘러들어온 것을 알 수 있다. Hydra Market은 다크 웹에서 사용되는 불법 마약 밀매와 자금 세탁 등을 위한 마켓 플레이스였는데, 2022년 4월 미국 법 집행 기관과 독일 당국에 의해 압수 및 폐쇄처리 되었으며, 2,500만 달러 상당의 비트코인이 들어있는 암호화폐 지갑이 압수된 사실이 있다.

<figure><img src="../.gitbook/assets/image (81).png" alt=""><figcaption><p>[그림 4] Upbit에서 자금이 흘러들어온 모습</p></figcaption></figure>

\[그림 2]의 input 지갑 주소 중 하나인 18qyDj6pSQRMvcUUjdh7X5fLnn4CxTDD8h에 들어온 0.06 BTC의 자금을 추적하면 국내 암호화폐 거래소인 Upbit로부터 온 것을 알 수 있다.

<figure><img src="../.gitbook/assets/image (67).png" alt=""><figcaption><p>[그림 5] Bitstamp에서 자금이 흘러들어온 모습</p></figcaption></figure>

\[그림 2]의 input 지갑 주소 중 1MjHu1yt38Xn1MDoMEHuLyiAhPfzvg58sR, 15GNYpjAeV5XnpJzv2zDJHGy7JzzQoWuce로 전송된 자금은 Bitstamp 거래소로부터 온 것을 알 수 있다.

### 2-2) Input 트랜잭션 추적

<figure><img src="../.gitbook/assets/image (31).png" alt=""><figcaption><p>[그림 6] Peel Chain 형태로 자금이 들어오는 모습</p></figcaption></figure>

분석 대상 지갑 주소인 16sYqXAncDDiijcuruZecCkdBDwDf4vSEC로 들어온 자금을 추적한 그래프 중 일부는 위와 같다.

트랜잭션은 Peel Chain과 유사한 형태로 이어져 오고 있으며, 큰 줄기를 따라가다 보면 8개의 지갑 주소로부터 BTC를 전송 받아 200 BTC로 시작하는 것을 볼 수 있다.

200 BTC는 트랜잭션이 발생하면서 약 3.98, 50, 25, 0.77, 25, 16, 53.22, 7.1, 15.65에 해당하는 금액을 분리시켜 또 다른 트랜잭션 줄기를 생성하는 형태를 띈다.

도중에는 Bitstamp나 BitPay 소유의 지갑으로 자금이 전송되기도 했으며, 크고 작은 BTC들이 떨어져나감에 따라 몸값 지불 주소에는 0.06 BTC만 전송되었다.

자금이 유입되는 형태로 봐서 피해자가 몸값을 지불한 것으로 보이지는 않는다.

#### Joinmarket Coinjoin

<figure><img src="../.gitbook/assets/image (34).png" alt=""><figcaption><p>[그림 7] 다수의 지갑 주소로부터 자금이 모이는 모습</p></figcaption></figure>

\[그림 6]에서 확인한 트랜잭션에 있는 input 지갑 주소의 트랜잭션을 더 확장한 모습은 위 그림과 같다.

Wallet Joinmarket Coinjoin 엔티티가 부여된 다수의 지갑 주소에서 하나의 트랜잭션을 통해 BTC를 모으는 형태를 띄고 있다.

Joinmarket은 P2P 환경에서 작동하는 탈중앙화 비트코인 거래 프로그램이다. Python으로 개발된 오픈소스 프로젝트로, GUI 환경(Joinmarket-Qt)을 제공하고 있다. ([https://github.com/JoinMarket-Org/joinmarket-clientserver](https://github.com/JoinMarket-Org/joinmarket-clientserver))

Joinmarket 프로젝트에는 coinjoin이 임의의 시간에 임의의 금액으로 자동 생성되는 스크립트가 포함되어 있으며, 사용자가 손쉽게 coinjoin을 수행할 수 있도록 지원한다.

<figure><img src="../.gitbook/assets/image (42).png" alt=""><figcaption><p>[그림 8] Peel Chain 트랜잭션 그래프 확장 모습</p></figcaption></figure>

\[그림 6]에서 확인한 Peel Chain 형태의 그래프를 확장한 그림은 위와 같다.

큰 가지에서 분리된 자금은 대부분 붉은색 원으로 표시한 BitPay 클러스터로 향하는 것을 확인했다.

BitPay는 미국에 위치한 암호화폐 결제 서비스 제공업체이다. KYC 정책을 잘 준수하는 것으로 알려져 있다.

## 3. 소결론

* 16sYqXancDDiijcuruZecCkdBDwDf4vSEC 지갑 주소는 0.06 BTC를 주고 받았으며, 총 2회의 트랜잭션을 포함하고 있다.
* 자금은 다수의 Joinmarket Coinjoin으로부터 시작해서 Peel Chain 형태로 전송되어 왔다.
* Peel Chain 트랜잭션에서 분리된 Peel 중 대부분은 BitPay 소유의 주소로 전송되었다.
* 전송 받은 자금은 다른 주소의 BTC와 합쳐져 Binance 거래소로 전송되었다.
* Binance 거래소로 전송하는 트랜잭션의 Input으로 사용된 주소의 수신 트랜잭션을 추적한 결과, Bitstamp, Upbit 거래소로부터 전송된 것을 확인했다. 또 다른 트랜잭션에서는 다크넷 거래소인 Hydra Market으로부터 전송받기도 했다.

