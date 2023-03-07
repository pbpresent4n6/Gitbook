# 1J8spy62o7z2AjQxoUpiCGnBh5cRWKVWJC

## 1. 1J8spy62o7z2AjQxoUpiCGnBh5cRWKVWJC 지갑 주소 정보

<figure><img src="../.gitbook/assets/image (92).png" alt=""><figcaption><p>[그림 1] 1J8spy62o7z2AjQxoUpiCGnBh5cRWKVWJC 지갑 주소 정보</p></figcaption></figure>



QLUE에서 조회한 1J8spy62o7z2AjQxoUpiCGnBh5cRWKVWJC 지갑 주소의 요약 정보는 위와 같다.



|               목록               |                  값                 |
| :----------------------------: | :--------------------------------: |
|          Address Hash          | 1J8spy62o7z2AjQxoUpiCGnBh5cRWKVWJC |
|          Balance (BTC)         |                  0                 |
|          Transactions          |                  5                 |
|       Cluster Identifier       |              828661150             |
| Number of Addresses in Cluster |                  2                 |
|          BitRank Score         |            5, High Risk            |
|       Entities and Flags       |            , Ransomware            |
|      Received Transactions     |                  3                 |
|        Sent Transactions       |                  2                 |
|      Received Amount (BTC)     |           1.87482707 BTC           |
|        Sent Amount (BTC)       |           1.87482707 BTC           |
|   First Seen Receiving (UTC)   |         2021-05-11 19:52:04        |
|    Last Seen Receiving (UTC)   |         2021-05-17 21:02:25        |
|    First Seen Sending (UTC)    |         2021-05-12 09:15:59        |
|     Last Seen Sending (UTC)    |         2021-06-25 03:34:00        |



해당 지갑 주소는 2021년 5월 11일 19시 52분 경 처음으로 수신 트랜잭션이 발생해서 같은 달 17일 21시 02분 경에 마지막으로 수신했다.

그리고 2021년 5월 12일 09시 15분 경 처음으로 전송 트랜잭션이 발생했고, 다음 달인 6월 25일 03시 34분 경에 마지막으로 전송 트랜잭션이 발생했다.

트랜잭션은 송신 2회, 수신 3회를 포함해서  총 5회 발생했고, 총 1.87482707 BTC를 주고 받았다.

또한, Ransomware, North Korea 플래그를 부여 받았고 BitRank Score는 0점으로 High Risk이다.

QLUE에서 식별할 수 있는 Cluster 식별 값은 828661150이며, 해당 클러스터에는 2개의 지갑 주소가 포함되어 있다.



## 2. 1J8spy62o7z2AjQxoUpiCGnBh5cRWKVWJC 주소 트랜잭션 추적

<figure><img src="../.gitbook/assets/image (53).png" alt=""><figcaption><p>[그림 2] Binance 거래소로 비트코인 전송</p></figcaption></figure>



분석 대상 지갑 주소인 1J8spy62o7z2AjQxoUpiCGnBh5cRWKVWJC 주소에서는 앞서 16ENLdHbnmDcEV8iqN4vuyZHa7sSdYRh76 주소 분석에서 다뤘듯이 수신한 BTC를 모두 Binance 거래소로 전송한 것을 확인할 수 있다.



### 2-1) Input 트랜잭션 추적



<figure><img src="../.gitbook/assets/image (88).png" alt=""><figcaption><p>[그림 3] Bithumb 거래소로부터 전송된 비트코인</p></figcaption></figure>



3개의 Input 트랜잭션 중 하나는 Bithumb 거래소로부터 0.1 BTC가 전송된 것이다.

거래소로부터 전송되었다는 점과 딱 떨어지는 0.1이라는 수치를 봤을 때 랜섬웨어 피해자가 지불했을 가능성이 높다고 볼 수 있다.



<figure><img src="../.gitbook/assets/image (69).png" alt=""><figcaption><p>[그림 4] Binance 거래소로부터 전송된 비트코인</p></figcaption></figure>



3개의 Input 트랜잭션 중 나머지 하나는 Binance 거래소로부터 1.66405585 BTC가 전송된 것이다.

해당 금액은 피해자가 전송했을 수도 있지만, 분석 대상 지갑 주소와 거래소 사이에 하나의 지갑 주소가 더 있다는 점과 딱 떨어지지 않는 금액으로 봤을 때, 출금에 어려움이 생겼거나 모종의 사유로 인해 다른 지갑 주소로 비트코인을 모으고 다시 거래소로 전송했을 것이라는 생각도 해볼 수 있다.



<figure><img src="../.gitbook/assets/image (52).png" alt=""><figcaption><p>[그림 5] Gemini 거래소로부터 전송된 비트코인</p></figcaption></figure>



3개의 Input 트랜잭션 중 마지막 트랜잭션의 정보는 위 그림과 같이 Gemini 거래소로부터 0.11145822 BTC가 전송된 것이다.

위 트랜잭션에서 주의깊게 봐야할 부분은 분석 대상 지갑 주소로 전송된 BTC외에도 Bitcoin Depot, Bitmart, Bybit 클러스터에도 자금이 전송되었다는 사실이다.

Bitcoin Depot은 미국과 캐나다 전역에서 7,000개 이상의 Bitcoin ATM을 운영하고 있는 서비스 업체이며, Bitmart와 Bybit는 암호화폐 거래소이다. BIG의 연구에 따르면 Bitmart는 충분한 KYC 절차를 준수하고 있으나 Bybit는 인증 없이 P2P 거래 및 일부 기본 혜택에 접근할 수 있는데, 최대 1000$까지 거래하거나 2 BTC를 입출금할 수 있다고 한다.

하나의 트랜잭션에서 Bitcoin ATM, 2개의 암호화폐 거래소 그리고 별도의 지갑 주소로 자금이 전송되는 형태로 봤을 때, 랜섬웨어 피해자의 몸값 전송으로 보기에는 의문점이 있기 때문에 공격자의 또 다른 지갑 주소로부터 전송된 것으로 보는 것이 더 타당할 것이다.



## 3. 소결론



* 1J8spy62o7z2AjQxoUpiCGnBh5cRWKVWJC  주소는 5회의 트랜잭션을 포함하고 있으며, 총 1.87482707 BTC를 주고받았다.
* Input 트랜잭션은 총 3개이며, Binance, Bithumb, Gemini 거래소로부터 전송되었다.
* 거래소로부터 전송된 트랜잭션에는 Output이 분석 대상 지갑 주소 뿐만 아니라 Bitcoin ATM 서비스인 Bitcoin Depot 소유로 알려진 주소에도 전송되었으며, Bitmart, Bybit 거래소 소유의 주소로도 전송되었다.
* 1J8spy62o7z2AjQxoUpiCGnBh5cRWKVWJC 지갑 주소의 송·수신 트랜잭션 분석은 이상으로 마친다.

