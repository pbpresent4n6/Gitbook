# 14hVKm7Ft2rxDBFTNkkRC3kGstMGp2A4hk

1\. 14hVKm7Ft2rxDBFTNkkRC3kGstMGp2A4hk 지갑 주소 정보

<figure><img src="../.gitbook/assets/image (62).png" alt=""><figcaption><p>[그림 1] 14hVKm7Ft2rxDBFTNkkRC3kGstMGp2A4hk 지갑 주소 정보</p></figcaption></figure>



QLUE에서 조회한 14hVKm7Ft2rxDBFTNkkRC3kGstMGp2A4hk 지갑 주소의 요약 정보는 위와 같다.



|               목록               |                                        값                                        |
| :----------------------------: | :-----------------------------------------------------------------------------: |
|          Address Hash          |                        14hVKm7Ft2rxDBFTNkkRC3kGstMGp2A4hk                       |
|          Balance (BTC)         |                                        0                                        |
|          Transactions          |                                        4                                        |
|          Cluster Name          |                                 RYUK Ransomware                                 |
|       Cluster Identifier       |                                    431284000                                    |
| Number of Addresses in Cluster |                                        2                                        |
|          BitRank Score         |                                  0 , High Risk                                  |
|       Entities and Flags       | Ryuk Ransomware, \[Ransomware, Ransomware Ryuk, Seen On Paste Bin, North Korea] |
|      Received Transactions     |                                        2                                        |
|        Sent Transactions       |                                        2                                        |
|      Received Amount (BTC)     |                                        10                                       |
|        Sent Amount (BTC)       |                                        10                                       |
|   First Seen Receiving (UTC)   |                               2018-09-14 15:57:05                               |
|    Last Seen Receiving (UTC)   |                               2018-09-14 18:20:18                               |
|    First Seen Sending (UTC)    |                               2018-09-14 16:38:07                               |
|     Last Seen Sending (UTC)    |                               2018-09-14 18:20:18                               |



해당 지갑 주소는 2018년 9월 14일 15시 57분 경에 처음, 같은 날 18시 20분 경에 마지막으로 수신트랜잭션이 발생했다. 또한, 같은 날 16시 38분 경에 처음, 18시 20분 경에 마지막으로 송신 트랜잭션이 발생했다.

트랜잭션은 송·수신 각 2회씩 총 4번 발생했고, 총 10 BTC를 전송했다.

엔티티와 플래그에 Ryuk Ransomware가 부여되었으며, 특히 플래그 중 Seeon On Paste Bin은 Pastebin.com이라는 텍스트 파일 공유 사이트에서 관련 정보가 식별된 것으로 볼 수 있다. 또한 North Korea 플래그가 부여되었다.

BitRank Score는 0점으로 High Risk이다.

QLUE에서 식별할 수 있는 Cluster 식별 값은 431284000이며, 해당 클러스터에는 2개의 지갑 주소가 포함되어 있다.



## 2. 14hVKm7Ft2rxDBFTNkkRC3kGstMGp2A4hk 주소 트랜잭션 추적

<figure><img src="../.gitbook/assets/image (64).png" alt=""><figcaption><p>[그림 2] Gemini 거래소로부터 전송된 비트코인</p></figcaption></figure>



Gemini 거래소로부터 분석 대상 지갑 주소인 14hVKm7Ft2rxDBFTNkkRC3kGstMGp2A4hk로 10 BTC가 전송된 것을 알 수 있다.

거래소로부터 금액이 들어왔다는 점, 10이라는 딱 떨어지는 금액으로 봤을 때 피해자가 몸값을 지불한 것일 확률이 높다고 볼 수 있다.

전송된 10 BTC는 2개의 트랜잭션을 통해 3개의 지갑 주소로 나뉘어서 전송되었다.



### 2-1. Output 트랜잭션 추적



<figure><img src="../.gitbook/assets/image (11).png" alt=""><figcaption><p>[그림 3] DiscusFish 지갑 주소로 전송되는 트랜잭션 형태</p></figcaption></figure>



\[그림 2]에서 전송된 1.45984994 BTC의 트랜잭션을 추적한 결과 중간 과정에서 다른 지갑 주소에서 전송된 BTC와 합쳐져 여러가지 트랜잭션으로 분산된 것을 확인했다.

분산된 트랜잭션 중 대부분은 1Y12ZZjua8VG4FgZY6KrsuCiQT7ZxEF9R 지갑 주소와 17xUuSoJDMhcz8bN91QPnF3cfg4TDwPjyk 지갑 주소로 연결되는 것을 확인할 수 있었고 해당 두 지갑 주소에서는 위 그림과 같이 DiscusFish 클러스터로 식별되는 지갑 주소로 다량의 비트코인을 전송했다.

Discus Fish는 중국의 최초이자 대규모 마이닝 풀로 알려져 있으며 f2pool로 알려져 있다.

마이닝 풀 소유의 지갑 주소로 비트코인이 전송된 이유에 대해서는 현재로서는 파악하지 못했다.

분산된 다른 비트코인들 중 일부는 Binance, Coinpayments, Bittrex, Local Bitcoin 등으로 전송되었다.



<figure><img src="../.gitbook/assets/image (25).png" alt=""><figcaption><p>[그림 4] Output 트랜잭션 중 일부</p></figcaption></figure>



분석 대상 지갑 주소인 14hVKm7Ft2rxDBFTNkkRC3kGstMGp2A4hk의 Output 트랜잭션 중 9.9 BTC를 추적한 그래프는 위와 같다.

전송된 9.9 BTC는 여러 트랜잭션으로 분산되어 Local Bitcoin, Coinpayments, Binance 등 암호화폐 서비스 업체 소유 지갑 주소로 이동된 것을 확인했다.

그리고 일부 트랜잭션(초록색 네모 영역)은 Peel Chain 형태를 띄고 있어 추적을 어렵게 했다.

Output 트랜잭션 중 상당한 규모의 액수는 33bEYhASee8UhJrdprWS7orzZT2i8eNEug 지갑 주소로 전송되었다. (검은색 네모 영역)

해당 주소는 거래소로 클러스터링 되지는 않았지만, 트랜잭션 횟수가 약 3천 건이고, 주고 받은 BTC가 약 46,744 정도 되기 때문에 식별되지 않은 거래소의 지갑 주소로 추측해볼 수 있다.



<figure><img src="../.gitbook/assets/image (16).png" alt=""><figcaption><p>[그림 5] 1Lpv2cpu9fkdhhGcMc36b78JEWgtqrYm8A 지갑 주소 Input 트랜잭션</p></figcaption></figure>



Ryuk Ransomware 클러스터에 포함되어 있던 주소인 1Lpv2cpu9fkdhhGcMc36b78JEWgtqrYm8A의 Input BTC는 분석 대상 지갑 주소의 Output 트랜잭션 중 일부가 들어간 것으로 확인됐다.



## 3. 소결론



* 14hVKm7Ft2rxDBFTNkkRC3kGstMGp2A4hk 주소는 4회의 트랜잭션을 포함하고 있으며, 총 10 BTC를 주고 받았다.
* 자금은 Gemini 거래소로 식별되는 주소로부터 전송 받았다.
* 전송받은 자금은 Mining pool인 Discus Fish 소유의 주소를 비롯해서 Bittrex, Binance, Localbitcoin 등의 거래소, 암호화폐 지불 결제 서비스인 Coinpayments 소유의 주소 등으로 전송되었다.
* Peel Chain 기법을 사용한 것으로 보이는 트랜잭션도 확인되었으며, 전송된 자금 중 상당한 규모의 액수가 33bEYhASee8UhJrdprWS7orzZT2i8eNEug 주소로 전송되었는데, 거래소로 식별되지는 않았지만 트랜잭션의 횟수로 봤을 때 거래소 소유의 주소로 추정된다.
* 또한, 자금 중 일부는 동일한 랜섬웨어 클러스터에 속한 주소로 전송되기도 했다.
* 14hVKm7Ft2rxDBFTNkkRC3kGstMGp2A4hk 지갑 주소의 송·수신 트랜잭션 분석은 이상으로 마친다.

