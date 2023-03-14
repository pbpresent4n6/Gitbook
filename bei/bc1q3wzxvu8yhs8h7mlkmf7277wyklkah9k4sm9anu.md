# bc1q3wzxvu8yhs8h7mlkmf7277wyklkah9k4sm9anu

## 1. bc1q3wzxvu8yhs8h7mlkmf7277wyklkah9k4sm9anu 지갑 주소 정보

<figure><img src="../.gitbook/assets/image (58).png" alt=""><figcaption><p>[그림 1] bc1q3wzxvu8yhs8h7mlkmf7277wyklkah9k4sm9anu 지갑 주소 정보</p></figcaption></figure>

QLUE에서 조회한 bc1q3wzxvu8yhs8h7mlkmf7277wyklkah9k4sm9anu 지갑 주소의 요약 정보는 위와 같다.

|               목록               |                      값                     |
| :----------------------------: | :----------------------------------------: |
|          Address Hash          | bc1q3wzxvu8yhs8h7mlkmf7277wyklkah9k4sm9anu |
|          Balance (BTC)         |                      0                     |
|          Transactions          |                      2                     |
|       Cluster Identifier       |                  992294380                 |
| Number of Addresses in Cluster |                      1                     |
|          BitRank Score         |                0 , High Risk               |
|       Entities and Flags       |        , \[Ransomware, North Korea]        |
|      Received Transactions     |                      1                     |
|        Sent Transactions       |                      1                     |
|      Received Amount (BTC)     |                    2.54                    |
|        Sent Amount (BTC)       |                    2.54                    |
|   First Seen Receiving (UTC)   |             2022-03-30 15:49:37            |
|    Last Seen Receiving (UTC)   |             2022-03-30 15:49:37            |
|    First Seen Sending (UTC)    |             2022-03-30 23:14:34            |
|     Last Seen Sending (UTC)    |             2022-03-30 23:14:34            |

해당 지갑 주소는 2022년 3월 30일 15시 49분 경에 처음으로 트랜잭션이 발생했고, 당일 23시 14분 경을 마지막으로 트랜잭션이 확인되지 않는다.

트랜잭션은 송·수신 각 1회씩 총 2번 발생했고, 총 2.54 BTC를 전송했다.

해당 지갑 주소는 Ransomware, North Korea 플래그를 부여 받았다.

Ransomware 공격에 사용되었으며, 고위험 관할군에 속한 지갑 주소이기 때문에 BitRank Score는 0점으로 High Risk이다.

QLUE에서 식별할 수 있는 Cluster 식별 값은 992294380이며, 해당 클러스터에는 1개의 지갑 주소가 포함되어 있다.

## 2. bc1q3wzxvu8yhs8h7mlkmf7277wyklkah9k4sm9anu 주소 트랜잭션 추적

<figure><img src="../.gitbook/assets/image (78).png" alt=""><figcaption><p>[그림 2] bc1q3wzxvu8yhs8h7mlkmf7277wyklkah9k4sm9anu - eGraph</p></figcaption></figure>

QLUE의 e-Graph 기능으로 조회한 트랜잭션 그래프는 위와 같다.

2.54 BTC를 전송받은지 약 8시간 뒤, bc1qhjnxutw0qvah8rea430ark2df2fcxm5xlfy52r 주소로 전송하는 트랜잭션이 발생했다.

### 2-1) Output 트랜잭션 추적

<figure><img src="../.gitbook/assets/image (9).png" alt=""><figcaption><p>[그림 3] Binance 거래소로 비트코인 전송</p></figcaption></figure>

bc1qhjnxutw0qvah8rea430ark2df2fcxm5xlfy52r 주소에서 2.54 BTC 중 약 1.33에 해당하는 BTC를 Binance 거래소로 전송한 사실을 확인할 수 있다(붉은선). ([https://www.binance.com/en](https://www.binance.com/en))

Binance는 전 세계에서 가장 많은 사람들이 사용하는 거래소 중 하나로, 최근 들어서 KYC 정책을 준수하기 위해 노력하고 있으며 꾸준히 강화하고 있다. 따라서 Binance 지갑으로 자금이 흘러들어갔지만 현금화에 성공했는지는 알 수 없다.

그 후 약 1.2 BTC 중 0.00031 BTC에 해당하는 차액을 bc1q6uyfmjgy66afyz24q0e2v5d7pe2w6d7f7q052z 지갑 주소에 전송하고(녹색선) 나머지를 bc1qppzvg9vxscq84wrwel3kea8pfaswlwmvm66txq 지갑 주소에 전송했다(노란선).

<figure><img src="../.gitbook/assets/image (35).png" alt=""><figcaption><p>[그림 4] 0.00031 BTC의 트랜잭션을 추적</p></figcaption></figure>

0.00031 BTC 중 0.00025736 BTC는 붉은색 원으로 표시한 Bitzlato 거래소 소유의 지갑으로 전송되었다.

Bitzlato 거래소는 불법 활동에 상당히 연루되었고 느슨한 KYC 정책으로 인해 2023년 폐쇄 대상 거래소로 분류되었고 웹 사이트마저 압수되었다. 해당 거래소는 2018년부터 2022년까지 7억 달러 이상의 불법 자금을 처리했다고 알려져 있다.

위 그래프에서는 Bitzlato 거래소로 흘러간 자금이 11$에 불과하기 때문에 전체 BTC 중에서 큰 비중을 차지한다고 보기는 어렵다.

그리고 더 작은 금액인 0.00005 BTC가 별도의 output으로 분리되었기 때문에 해당 트랜잭션도 따라가보기로 했다.

<figure><img src="../.gitbook/assets/image (2) (1).png" alt=""><figcaption><p>[그림 5] 0.00005 BTC의 트랜잭션을 추적</p></figcaption></figure>

0.00005 BTC는 다른 102개의 input과 합쳐져 4.18927789 BTC가 되어 전송되었다.

여기서 그래프의 형태가 특이한데, 합쳐지는 데 사용된 지갑들의 트랜잭션이 모두 input 1개, output 1개만 존재했으며 하나의 output을 띄고 있다는 점이다.

#### Coinjoin이 반복되는 형태

<figure><img src="../.gitbook/assets/image (29).png" alt=""><figcaption><p>[그림 6] 자금 추적 회피 행위가 반복되는 형태</p></figcaption></figure>

위와 같이 같은 형태의 그래프가 반복되고 있는데, 하나의 트랜잭션에 다수의 input이 있는 형태로 봐서 coinjoin과 같은 서비스를 사용한 것으로 추측할 수 있다. 해당 그래프의 첫 coinjoin 형태가 보이는 트랜잭션보다 한참 전부터 같은 형태가 반복되어 오고 있었으며, output을 끝까지 추적한 결과 2023년 1월 13일 트랜잭션을 마지막으로 7.2107759 BTC가 bc1q22myyrpe8h2m0jqe5k7j9wqjcy6tksld05s3p0 지갑 주소로 전송된 것을 확인할 수 있었다.

해당 지갑 주소는 아직까지 input 트랜잭션 하나만 발생했기 때문에 추후 output 트랜잭션이 발생할 가능성이 높다고 볼 수 있다.

<figure><img src="../.gitbook/assets/image (41).png" alt=""><figcaption><p>[그림 7] 1.203262 BTC 트랜잭션 추적</p></figcaption></figure>

\[그림 3]에서 확인한 1.203262 BTC 전송 트랜잭션을 일부 추적한 그래프는 위와 같다.

중간에 coinjoin을 사용한 것으로 보이는 다른 트랜잭션 등의 BTC와 합쳐져 총 18.74752554 BTC가 되어 bc1qnj6v7fel4vjdkfzhguzgkm8heq2rk30750595u 주소로 전송되었다.

해당 금액은 4.096 크기의 트랜잭션 6개로 분리되었으며 각각 다른 방식으로 전송되는 것을 확인했다. 4.096 BTC로 분리된 트랜잭션 중 2개는 Binance와 Kraken 거래소로 각각 전송되었다.

<figure><img src="../.gitbook/assets/image (38).png" alt=""><figcaption><p>[그림 8] Peel Chain 트랜잭션 그래프</p></figcaption></figure>

\[그림 7]의 빨간색 네모 영역을 확대한 그림은 위와 같다. 그래프 형태를 보면 약 15.6 정도의 BTC를 계속해서 전송하고 있는데, 전송하는 메인 BTC에서 일부분을 조금씩 떼어내는 것을 알 수 있다. 이는 자금 추적을 회피하기 위해 많이 사용하는 Peel Chain 기법이다.

Peel Chain은 컴퓨터 스크립트로 자동화할 수 있으며 수백 또는 수천 건의 트랜잭션으로 생성할 수 있기 때문에 추적을 어렵게 만든다.

<figure><img src="../.gitbook/assets/image (83).png" alt=""><figcaption><p>[그림 9] Peel Chain Output 예시</p></figcaption></figure>

Peel Chain에서 떨어져 나간 작은 금액은 위 그림과 같이 거래소로 전송할 수 있다. 트랜잭션의 output 액수가 적기 때문에 AML 정책에 탐지될 위험이 적다.

#### Wasabi Coinjoin

<figure><img src="../.gitbook/assets/image (50).png" alt=""><figcaption><p>[그림 10] Coinjoin 트랜잭션 그래프</p></figcaption></figure>

\[그림 7]의 녹색 네모 영역을 확대한 그림은 위와 같다. 위 그래프는 자금 추적 기법 중 하나인 Coinjoin을 사용한 것으로, 하나의 트랜잭션에서 다수의 input과 다수의 output을 생성해 추적을 어렵게 만든다.

위 트랜잭션에서는 264개의 input과 311개의 output이 발생했다.

<figure><img src="../.gitbook/assets/image (91).png" alt=""><figcaption><p>[그림 11] Lazarus 그룹으로 흘러간 자금</p></figcaption></figure>

\[그림 7]에서 확인했던 분산된 4.096 BTC 중 일부는 위 그림과 같이 북한의 해커 그룹으로 알려져 있는 <mark style="background-color:red;">**Lazarus**</mark>의 소유로 식별된 지갑주소로 전송되었다.

#### **식별된 Lazarus Group의 지갑 주소**

* 3B9yt9LVFW6Fv6cMZSfJL1mgSj2ZewBqSv
* bc1ql0j5kuklmuvcejthxmdp66eyxrwtdy08tp5v36

3B9yt9LVFW6Fv6cMZSfJL1mgSj2ZewBqSv 주소에서 약 900건의 트랜잭션 기록이 발생한 사실과, 약 150 BTC가 전송되지 않고 남아있는 것을 확인했다. 또한, 본 글 작성일에도 트랜잭션이 발생하는 등 최근까지도 활발하게 트랜잭션이 발생하고 있다.

<figure><img src="../.gitbook/assets/image (28).png" alt=""><figcaption><p>[그림 12] 분산된 4.096 BTC 중 일부</p></figcaption></figure>

분산된 나머지 4.096 BTC들은 Binance 거래소로 전송되거나, 특정 지갑 주소에 전송된 후 추가 트랜잭션이 발생하지 않았다.

### 2-2) Input 트랜잭션 추적

<figure><img src="../.gitbook/assets/image (82).png" alt=""><figcaption><p>[그림 13] 거래소로부터 전송된 트랜잭션 그래프</p></figcaption></figure>

분석 대상 지갑 주소인 bc1q3wzxvu8yhs8h7mlkmf7277wyklkah9k4sm9anu로 전송된 BTC의 출처를 추적한 결과 Gemini 거래소에서 나온 것으로 확인되었다.

거래소로부터 랜섬웨어 몸값 지불 주소로 BTC가 전송됐다는 것은 정황상 랜섬웨어 피해자가 몸값을 지불한 것으로 볼 수 있다. ([https://www.gemini.com/](https://www.gemini.com/))

## 3. 소결론

* bc1q3wzxvu8yhs8h7mlkmf7277wyklkah9k4sm9anu 지갑 주소는 2회의 트랜잭션이 발생했으며, 2.54 BTC를 주고 받았다.
* 자금은 Gemini 거래소로부터 전송되었으며, 전송된 자금 중 일부는 Binance 거래소로 전송되었다.
* 자금 중 0.00005 BTC는 Coinjoin의 input으로 전송되었고, 반복되는 Coinjoin 행위 끝에 약 7.2 BTC가 되어 bc1q22myyrpe8h2m0jqe5k7j9wqjcy6tksld05s3p0 주소로 전송되었다.
* 또 다른 Output 트랜잭션 중 Wasabi Coinjoin을 사용했으며, Peel Chain 기법을 이용하는 등 추적을 회피하기 위한 행위들이 확인되었다.
* 자금들은 Binance, Bitzlato, Kraken 등 다양한 거래소로 전송되었으며 특히 Lazarus 그룹 소유의 주소에도 전송되었다.

