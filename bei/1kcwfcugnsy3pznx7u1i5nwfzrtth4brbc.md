# 1KCwfCUgnSy3pzNX7U1i5NwFzRtth4bRBc

## 1. 1KCwfCUgnSy3pzNX7U1i5NwFzRtth4bRBc 지갑 주소 정보

<figure><img src="../.gitbook/assets/image (3) (1).png" alt=""><figcaption><p>[그림 1] 1KCwfCUgnSy3pzNX7U1i5NwFzRtth4bRBc 지갑 주소 정보</p></figcaption></figure>

QLUE 에서 조회한 1KCwfCUgnSy3pzNX7U1i5NwFzRtth4bRBc 지갑 주소의 요약 정보는 위와 같다.

|               목록               |                  값                 |
| :----------------------------: | :--------------------------------: |
|          Address Hash          | 1KCwfCUgnSy3pzNX7U1i5NwFzRtth4bRBc |
|          Balance (BTC)         |                  0                 |
|          Transactions          |                  6                 |
|       Cluster Identifier       |              806944670             |
| Number of Addresses in Cluster |                 94                 |
|          BitRank Score         |            0 , High Risk           |
|       Entities and Flags       |    , \[Ransomware, North Korea]    |
|      Received Transactions     |                  3                 |
|        Sent Transactions       |                  3                 |
|      Received Amount (BTC)     |               0.0361               |
|        Sent Amount (BTC)       |               0.0361               |
|   First Seen Receiving (UTC)   |         2021-05-13 19:30:47        |
|    Last Seen Receiving (UTC)   |         2022-12-25 23:59:15        |
|    First Seen Sending (UTC)    |         2021-05-14 21:26:36        |
|     Last Seen Sending (UTC)    |         2022-12-27 12:49:31        |

해당 지갑 주소는 2021년 5월 13일 19시 30분 경에 처음으로 수신, 22년 12월 25일 23시 59분 경에 마지막으로 수신 트랜잭션이 발생했다. 그리고 21년 5월 14일 21시 26분 경에 처음, 22년 12월 27일 12시 49분 경에 마지막으로 송신 트랜잭션이 발생했다.

트랜잭션은 송·수신 각 3회씩 총 6번 발생했고, 총 0.0361 BTC를 전송했다.

해당 지갑 주소는 Ransomware, North Korea 플래그를 부여 받았다.

BitRank Score는 0점으로 High Risk이다.

QLUE에서 식별할 수 있는 Cluster 식별 값은 806944670이며, 해당 클러스터에는 94개의 지갑 주소가 포함되어 있다.

## 2. 1KCwfCUgnSy3pzNX7U1i5NwFzRtth4bRBc 주소 트랜잭션 추적

<figure><img src="../.gitbook/assets/image (8) (1).png" alt=""><figcaption><p>[그림 2] 1KCwfCUgnSy3pzNX7U1i5NwFzRtth4bRBc - eGraph</p></figcaption></figure>

분석 대상 지갑 주소인 1KCwfCUgnSy3pzNX7U1i5NwFzRtth4bRBc를 eGraph에서 조회한 결과는 위와 같다.

3회의 수신 트랜잭션으로 0.012, 0.0001, 0.024 BTC를 전송 받았으며, 동일한 액수로 송신 트랜잭션이 3회 발생했다.

### 2-1) Output 트랜잭션 추적

<figure><img src="../.gitbook/assets/image (79).png" alt=""><figcaption><p>[그림 3] Binance 거래소로 전송되는 BTC</p></figcaption></figure>

3개의 트랜잭션 중 0.024 BTC는 Binance 거래소 소유의 지갑 주소로 전송되었다.

해당 거래소의 지갑 주소는 CISA가 공개한 북한 비트코인 지갑 주소 43개 중 하나이다.

다른 지갑 주소 소유의 BTC와 함께 전송되었는데 0.024 BTC를 전송한 input이 많다는 점을 알 수 있다.

#### Peel Chain

<figure><img src="../.gitbook/assets/image (66).png" alt=""><figcaption><p>[그림 4] Peel Chain 형태의 트랜잭션</p></figcaption></figure>

분석 대상 지갑 주소에서 전송된 0.0001 BTC는 다른 지갑 주소의 BTC와 합쳐져 0.09006927 BTC로 전송되었으며, 해당 금액 또한 다른 BTC와 합쳐져 두 개의 output으로 분리되었다. 분리된 output 중 하나는 전송 받은 다른 BTC와 합쳐져 약 26 BTC가 되었다.

합쳐진 약 26 BTC는 위 그림과 같이 Peel Chain 기법을 사용해서 추적을 어렵게 한 것을 알 수 있다.

<figure><img src="../.gitbook/assets/image (36).png" alt=""><figcaption><p>[그림 5] Output 트랜잭션 추적 중 일부</p></figcaption></figure>

\[그림 4]에서 분리된 트랜잭션의 BTC 중 일부는 위 그림에서 볼 수 있는 3Q27wPHPSSs2ZQsTuuD7sK6ARG4LHjFNaR 지갑 주소로 전송되었다.

해당 지갑 주소에서는 Binance, Bitzlato 등 거래소를 비롯하여 Lazarus 그룹과 Hydra market에도 전송한 기록을 확인할 수 있다.

#### **식별된 Lazarus Group의 지갑 주소**

* 121AkmEbHBX9FuFeuDWv2CpyHqNq9F18k9
* 1C5qLPgqW4Ed6PuyLHPqXpdF2gQ1EEnJ65

<figure><img src="../.gitbook/assets/image (33) (1).png" alt=""><figcaption><p>[그림 6] Coinspaid 엔티티 소유 지갑 주소로 전송되는 트랜잭션 형태</p></figcaption></figure>

분석 대상 지갑 주소에서 확인한 송신 트랜잭션 중 마지막 하나는 다른 지갑 주소에서 전송된 BTC와 합쳐져 0.14022775 BTC가 전송되었고, 해당 BTC는 또 다른 BTC와 합쳐져 Coinspaid 엔티티가 부여된 지갑 주소인 bc1qns9f7yfx3ry9lj6yz7c9er0vwa0ye2eklpzqfw로 전송된 것을 알 수 있다.

해당 지갑 주소는 Coinspaid로 클러스터링되지는 않았지만 트랜잭션 수가 약 26만 건인 점을 통해 실제 Coinspaid 소유의 지갑 주소로 볼 수 있을 것이다.

### 2-2) Input 트랜잭션 추적

<figure><img src="../.gitbook/assets/image (6) (1).png" alt=""><figcaption><p>[그림 7] Coinbase 거래소로부터 전송된 BTC</p></figcaption></figure>

분석 대상 지갑 주소에서 확인된 3개의 수신 트랜잭션 중 하나는 위 그림과 같이 Coinbase 거래소 소유의 지갑 주소로부터 전송되었다.

0.28139644 BTC가 전송되었고 그 중 0.012에 해당하는 BTC만 분석 대상 지갑 주소로 전송되었다.

Output이 41개나 되는 걸로 봤을 때, 일반적인 사용자의 전송 형태는 아닌 것으로 판단되며, 공격자 소유의 지갑 주소로 추측된다.

<figure><img src="../.gitbook/assets/image (20).png" alt=""><figcaption><p>[그림 8] Peel Chain 및 거래소로부터 전송된 트랜잭션 형태</p></figcaption></figure>

분석 대상 지갑 주소의 input 트랜잭션 3개 중 하나는 Peel Chain으로부터 전송되었다.

Peel Chain에서 분리된 트랜잭션 다수는 Coinbase 거래소 소유의 지갑 주소로 전송되었다.

그리고 마지막 input 트랜잭션은 Coinbase 거래소 소유의 50개 이상의 지갑 주소로부터 전송되었다.

전송된 BTC는 분석 대상 지갑을 포함해서 Binance, Bitrue, Bibox, Kraken, Nexo 등의 거래소에도 전송되었다.

BTC가 Peel Chain으로부터 전송되었다는 점, 거래소 소유의 다수의 input으로부터 다수의 output으로 전송되었다는 점으로 미루어보아 input 트랜잭션은 공격자의 행위로 추측된다.

## 3. 소결론

* 1KCwfCUgnSy3pzNX7U1i5NwFzRtth4bRBc 주소는 6회의 트랜잭션을 포함하고 있으며, 총 0.0361 BTC를 주고 받았다.
* Input 트랜잭션은 총 3회로, Coinbase 거래소 소유의 단일 주소로부터 전송받은 트랜잭션 하나, 똑같은 Coinbase 거래소 소유의 다수 주소로부터 전송받은 트랜잭션 하나가 존재한다. 나머지 하나는 Peel Chain 형태의 트랜잭션으로부터 전송된 것으로 해당 Peel Chain의 Peel은 많은 비중이 Coinbase 거래소 소유의 주소로 전송되었으며, 일부는 Binance, Bitrue, Bibox, Kraken, Nexo, Gate.io 거래소로 전송되기도 했다.
* 전송 받은 자금은 Binance 거래소, Lazarus 그룹, Hydra Market, Coinspaid 등으로 전송되었으며 일부는 Peel Chain 형태로 전송해서 추적을 어렵게 만들었다.

