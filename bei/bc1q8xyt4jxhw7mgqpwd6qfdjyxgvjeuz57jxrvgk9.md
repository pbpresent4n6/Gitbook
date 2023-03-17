# bc1q8xyt4jxhw7mgqpwd6qfdjyxgvjeuz57jxrvgk9

## 1. bc1q8xyt4jxhw7mgqpwd6qfdjyxgvjeuz57jxrvgk9 지갑 주소 정보

<figure><img src="../.gitbook/assets/image (24).png" alt=""><figcaption><p>[그림 1] bc1q8xyt4jxhw7mgqpwd6qfdjyxgvjeuz57jxrvgk9 지갑 주소 정보</p></figcaption></figure>

QLUE에서 조회한 bc1q8xyt4jxhw7mgqpwd6qfdjyxgvjeuz57jxrvgk9 지갑 주소의 요약 정보는 위와 같다.

|               목록               |                      값                     |
| :----------------------------: | :----------------------------------------: |
|          Address Hash          | bc1q8xyt4jxhw7mgqpwd6qfdjyxgvjeuz57jxrvgk9 |
|          Balance (BTC)         |                      0                     |
|          Transactions          |                      2                     |
|       Cluster Identifier       |                 1014461646                 |
| Number of Addresses in Cluster |                      1                     |
|          BitRank Score         |                0 , High Risk               |
|       Entities and Flags       |        , \[Ransomware, North Korea]        |
|      Received Transactions     |                      1                     |
|        Sent Transactions       |                      1                     |
|      Received Amount (BTC)     |                   0.51256                  |
|        Sent Amount (BTC)       |                   0.51256                  |
|   First Seen Receiving (UTC)   |             2022-05-24 03:24:15            |
|    Last Seen Receiving (UTC)   |             2022-05-24 03:24:15            |
|    First Seen Sending (UTC)    |             2022-07-05 07:24:58            |
|     Last Seen Sending (UTC)    |             2022-07-05 07:24:58            |

해당 지갑 주소는 2022년 5월 24일 03시 24분 경에 처음으로 트랜잭션이 발생했고, 2022년 7월 5일 07시 24분 경을 마지막으로 트랜잭션이 확인되지 않는다.

트랜잭션은 송·수신 각 1회씩 총 2번 발생했고, 총 0.51256 BTC를 전송했다.

QLUE의 제조사인 BIG에서는 공개된 자료 등을 통해 식별된 지갑 주소들에 플래그와 엔티티 정보를 부여하는데, 해당 지갑 주소는 Ransomware, North Korea 플래그를 부여 받았다.

Ransomware 공격에 사용됐으며, 고위험 관할권에 속한 지갑 주소이기 때문에 BitRank Score는 0점으로 High Risk이다.

QLUE에서 식별할 수 있는 Cluster 식별 값은 1014461646이며, 해당 클러스터에는 1개의 지갑 주소가 포함되어 있다.

## 2. bc1q8xyt4jxhw7mgqpwd6qfdjyxgvjeuz57jxrvgk9 주소 트랜잭션 추적

<figure><img src="../.gitbook/assets/image (86).png" alt=""><figcaption><p>[그림 2] bc1q8xyt4jxhw7mgqpwd6qfdjyxgvjeuz57jxrvgk9 - eGraph</p></figcaption></figure>

QLUE의 Explorer Graph 기능으로 조회한 트랜잭션 그래프는 위와 같다.

bc1q8xyt4jxhw7mgqpwd6qfdjyxgvjeuz57jxrvgk9 지갑 주소로 들어온 0.51256 BTC는 전송 받았을 때는 15,008.10$의 가치를 가지고 있었지만, 전송할 때는 시세가 하락하여 10,397.85$의 가치를 가졌다.

0.51256 BTC 중 0.512 BTC는 3ByzggH211WiSPuqK6AvAGuvSE2dbduHvM 주소로 전송되었다.

차액은 bc1q4l6626rfd2ms4e68gzntjvte2swxnxcre3dpgn 주소로 전송되었는데, 그 후 트랜잭션은 발생하지 않았다.

### 2-1) Output 트랜잭션 추적

<figure><img src="../.gitbook/assets/image (14) (1).png" alt=""><figcaption><p>[그림 3] NairaEx 거래소로 비트코인 전송</p></figcaption></figure>

0.512 BTC가 전송된 3ByzggH211WiSPuqK6AvAGuvSE2dbduHvM 지갑 주소는 NairaEx라는 거래소의 지갑 주소로 식별되었다. ([https://nairaex.com/](https://nairaex.com/))

QLUE에서 제공하는 Entity Explorer 기능으로 NairaEx 거래소에 대한 정보를 확인할 수 있다.

BIG의 조사에 따르면 NairaEx 거래소는 2015년 나이지리아에 설립된 암호화폐 거래소로, 13만 명 이상의 사용자를 보유하고 있으며 90만 건 이상의 거래를 처리했다고 한다.

NairaEx 거래소는 이메일 주소를 제출하기만 하면 암호화폐를 입금하고 인출할 수 있도록 허용한다고 한다. 또한, 은행 계좌번호와 은행 확인 번호(Bank Verification Number)를 제공하면 되기 때문에 충분하지 못한 KYC 프로세스를 가지고 있다고 평가했다.

### 2-2) Input 트랜잭션 추적

<figure><img src="../.gitbook/assets/image (59).png" alt=""><figcaption><p>[그림 4] 0.51256 BTC가 들어온 과정</p></figcaption></figure>

bc1qx3nf69khasc4uhmk8q3ygezaxcramjnurthkm7 주소에서 분석 대상 지갑 주소로 0.51256 BTC를 전송했다.

잠깐 근본적인 문제로 돌아가보면, 북한이 랜섬웨어 몸값 지불에 사용할 수 있다는 사실 외에 실제로 랜섬웨어 피해가 발생해서 몸값이 지불이 되었는지에 대한 사실 여부는 드러나 있지 않다.

따라서, 저 0.51256 BTC를 전송한 지갑 주소가 랜섬웨어 피해자의 지갑 주소인지, 공격자의 또 다른 지갑 주소인지 알 수 없는 상황이다.

트랜잭션 그래프의 형태를 봤을 때는 랜섬웨어 피해자의 지갑 주소로 보이지는 않는다. 다수의 트랜잭션을 가지고 있고, 일반적인 피해자라면 거래소를 통해 암호화폐를 입금하기 때문이다.

따라서 본 글에서는 해당 지갑 주소를 공격자의 또 다른 지갑 주소로 판단하고 계속해서 추적을 진행했다.

<figure><img src="../.gitbook/assets/image (87).png" alt=""><figcaption><p>[그림 5] bc1qx3nf69khasc4uhmk8q3ygezaxcramjnurthkm7 지갑 주소로 들어온 자금 출처 중 일부</p></figcaption></figure>

해당 지갑 주소에서는 3개의 지갑 주소로부터 6.17482795 BTC를 전송 받았고, 0.51256 BTC를 제외한 나머지 BTC를 2개의 지갑 주소에 나누어 전송했다.

bc1qx3nf69khasc4uhmk8q3ygezaxcramjnurthkm7 지갑 주소로 BTC를 전송한 3개의 지갑 중 2개의 지갑 주소의 input을 추적한 결과 거래소로 클러스터링되지는 않았지만, 거래소로 추정되는 지갑 주소로부터 BTC를 받은 사실을 확인했다.

bc1qvajhalgj3remvepxn0m4aj39kjppgz2q90whzx 지갑 주소에서는 4천 건 이상의 트랜잭션이 있었고, 약 13만 개의 BTC를 주고 받은 기록을 확인했다.

bc1qsrr8sf7xxyvaxylefta92m3qhwdj3nlu0jrl4x 지갑 주소에서는 약 2천 건의 트랜잭션이 있었고, 약 2만 개의 BTC를 주고 받은 기록을 확인했다.

일반 사용자의 지갑 주소라면 위와 같이 많은 트랜잭션을 가지고, 많은 비트코인을 거래한다고 보기 힘들기 때문에 거래소 소유의 지갑 주소로 추정할 수 있고, 랜섬웨어 피해자가 비트코인을 입금하기 위해 거래소로부터 가져온 것으로 추측된다.

또한 액수가 깔끔하게 떨어지는 0.5, 5라는 수치도 합리적인 의심의 근거가 된다고 볼 수 있겠다.

따라서 bc1qx3nf69khasc4uhmk8q3ygezaxcramjnurthkm7 지갑 주소는 랜섬웨어 몸값 비용을 전달 받는 지갑 주소로 의심해볼 수 있다.

#### 2-2-A) 중간 지갑 주소 Output 트랜잭션 추적1

더 이상, 중간 지갑 주소의 input을 추적하는 것은 의미가 없는 것으로 판단되어, output을 추적했다.

<figure><img src="../.gitbook/assets/image (17).png" alt=""><figcaption><p>[그림 6] 중간 지갑 주소의 output 추적</p></figcaption></figure>

중간 지갑 주소의 Output은 앞서 봤듯이 이 글의 메인 분석 대상 지갑 주소를 제외하고 2개가 있었는데, 그 중 bc1qmhucf0p7l0dfprmdg5w6h6juq8yttmws4l2x0u 지갑 주소의 트랜잭션을 따라가봤다.

해당 지갑 주소에서는 4.99251 BTC가 1.2, 3.792478 BTC로 나뉘어 전송되었다.

<figure><img src="../.gitbook/assets/image (49).png" alt=""><figcaption><p>[그림 7] 1.2 BTC의 트랜잭션을 추적</p></figcaption></figure>

나뉜 BTC 중 1.2에 해당하는 값을 계속 추적했다.

1.2 BTC는 중간에 다른 지갑 주소에서 전송된 BTC와 합쳐져 2.99 BTC로 전송된 것을 알 수 있다.

<figure><img src="../.gitbook/assets/image (4) (1) (1).png" alt=""><figcaption><p>[그림 8] 2.99 BTC의 트랜잭션을 추적</p></figcaption></figure>

2.99 BTC는 다시 한 번 다른 지갑 주소에서 전송된 BTC들과 합쳐졌고, 2.048 BTC의 액수로 동시에 다수의 지갑에 나뉘어서 전송되었다.\
그 중 bc1q99vcvyuqxhg26ss3xygqz4x37w2le092zqh9ew 지갑 주소의 트랜잭션을 지속해서 추적해보기로 한다.

<figure><img src="../.gitbook/assets/image (74).png" alt=""><figcaption><p>[그림 9] 2.048 BTC의 트랜잭션을 추적 (1/5)</p></figcaption></figure>

2.048 BTC는 bc1qzyksw2g4f8zgq8en9pc6e2wpaw3nk6tdpfw5aq 지갑 주소로 전송되었고 해당 지갑 주소에서는 총 78개의 트랜잭션이 발생해 다수의 지갑으로 BTC를 주고받은 것을 알 수 있다.

<figure><img src="../.gitbook/assets/image (12).png" alt=""><figcaption><p>[그림 10] 흩어진 BTC가 하나의 지갑으로 모이는 형태</p></figcaption></figure>

다수의 트랜잭션을 통해 분산된 지갑들을 모두 확장시켜본 결과, 위 그래프와 같이 하나의 지갑으로 모이는 형태를 확인했다.

해당 지갑은 Coinspaid라는 암호화폐 결제 서비스 업체의 지갑으로 식별되었다. ([https://coinspaid.com/](https://coinspaid.com/))

암호화폐 서비스 업체의 지갑으로 전송되었기 때문에 더 이상의 추적은 무의미하다고 판단했다.

<figure><img src="../.gitbook/assets/image (32).png" alt=""><figcaption><p>[그림 11] 또 다른 2.048 BTC 추적 (2/5)</p></figcaption></figure>

앞서 분산되었던 2.048 BTC 중 다른하나를 추가로 추적했다.

추적 결과, 다른 지갑 주소에서 전송된 BTC와 합쳐져 위 그림에서 빨간색 원으로 표시한 Kucoin 거래소의 지갑으로 일부가 전송되었고 ([https://www.kucoin.com/ko](https://www.kucoin.com/ko)), 나머지는 보라색 원으로 표시한 지갑 주소로 전송되었는데, 해당 지갑 주소는 아직 output 트랜잭션이 발생하지 않았다.

<figure><img src="../.gitbook/assets/image (73).png" alt=""><figcaption><p>[그림 12] 또 다른 2.048 BTC 추적 (3/5)</p></figcaption></figure>

세 번째 2.048 BTC를 추적한 결과, 다른 지갑 주소에서 전송된 BTC와 합쳐져 OKX라는 거래소 소유의 지갑 주소로 전송된 것을 확인했다. ([https://www.okx.com/](https://www.okx.com/))

<figure><img src="../.gitbook/assets/image (43).png" alt=""><figcaption><p>[그림 13] 또 다른 2.048 BTC 추적 (4/5)</p></figcaption></figure>

네 번째 2.048 BTC를 추적한 결과, 다른 지갑 주소에서 전송된 BTC와 합쳐져 Mexc 거래소 소유의 지갑 주소로 전송되었다. ([https://www.mexc.com/ko-KR](https://www.mexc.com/ko-KR))

#### Chain Hopping

<figure><img src="../.gitbook/assets/image (5) (1) (1).png" alt=""><figcaption><p>[그림 14] 또 다른 2.048 BTC 추적 (5/5)</p></figcaption></figure>

다섯 번째 2.048 BTC를 추적한 결과, 다른 지갑 주소에서 전송된 BTC와 합쳐져 23.0396877 BTC에 해당하는 금액이 renBTC로 변환된 것을 확인했다.

renBTC는 비트코인을 이더리움 생태계에서 쓰기 위해 ERC20 토큰으로 전환하는 방법 중 하나이다.

이는 Chain Hopping이라고 하는 기법으로, 특정 플랫폼의 암호화폐를 다른 플랫폼의 암호화폐로 교환하는 것을 의미한다. (BTC->ETH 등)

#### 2-2-B) 중간 지갑 주소 Output 트랜잭션 추적2

<figure><img src="../.gitbook/assets/image (72).png" alt=""><figcaption><p>[그림 15] 분리된 다른 트랜잭션 추적</p></figcaption></figure>

중간 지갑 주소에서 분리된 다른 트랜잭션의 일부분을 추적해본 결과 다수의 트랜잭션이 \[그림 14]에서 확인한 renBTC 클러스터로 모이는 형태를 확인할 수 있었다.

그 외 BigONE, Binance 거래소로 자금이 흘러가는 것도 확인할 수 있었다.

## 3. 소결론

* bc1q8xyt4jxhw7mgqpwd6qfdjyxgvjeuz57jxrvgk9 지갑 주소는 0.51256 BTC를 주고 받았으며 2회의 트랜잭션 기록을 가지고 있다.
* 자금은 거래소로 식별되지는 않지만 트랜잭션 횟수 등의 근거로 인해 거래소 주소로 추정되는 곳으로부터 전송되었다.
* 전송받은 자금은 NairaEx 거래소로 전송되었다.
* 공격자 소유로 추정되는 또 다른 주소의 Output을 추적했을 때, 자금은 암호화폐 지불 결제 서비스인 Coinspaid 소유의 주소로 전송되기도 했으며 MEXC, Kucoin, OKX, Binance, BigONE 등의 거래소 소유 주소로도 전송되었다.
* 공격자는 비트코인을 이더리움 플랫폼 환경에서 사용하기 위해서 renBTC 서비스를 이용했다.

