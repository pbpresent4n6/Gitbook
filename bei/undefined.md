# 결론

미국 사이버인프라보안청인 CISA에서 공개한 북한 랜섬웨어 관련 비트코인 주소 43개에 대한 분석을 진행했다.

43개의 주소 중 트랜잭션 기록이 있는 유효한 주소는 9개였으며, 그 중 2개는 Binance 거래소 소유의 지갑 주소로 식별되었으며, 트랜잭션 기록이 있는 유효한 주소의 잔금은 모두 0인 것을 확인했다.

그리고 2개의 주소는 블록체인 조회 사이트에서 조회되지 않는 주소인 것을 확인했으며, 그 중 하나는 라이트코인 지갑 주소의 포맷으로 추측되는데, 트랜잭션 기록은 없는 것을 확인했다.

([https://blockchair.com/litecoin/address/LZ1VNJfn6mWjPzkCyoBvqWaBZYXAwn135](https://blockchair.com/litecoin/address/LZ1VNJfn6mWjPzkCyoBvqWaBZYXAwn135))

따라서, 유효한 주소 9개 중 거래소 소유의 지갑 주소 2개를 제외한 7개 지갑 주소의 트랜잭션을 암호화폐 추적 솔루션인 QLUE를 이용해서 추적했다.



|               美 CISA 공개 지갑 주소              |                     유형                    |
| :----------------------------------------: | :---------------------------------------: |
|     1KmWW6LgdgykBBrSXrFu9kdoHz95Fe9kQF     |               거래소 (Binance)               |
|     1FX4W9rrG4F3Uc7gJ18GCwGab8XuW8Ajy2     |               거래소 (Binance)               |
|      LZ1VNJfn6mWjPzkCyoBvqWaBZYXAwn135     | <p>조회되지 않는 주소</p><p>(Litecoin 주소로 추측)</p> |
| bc1qxrpevck3pq1yzrx2pq2rkvkvy0jnm56nzjv6pw |                 조회되지 않는 주소                |
|     1KCwfCUgnSy3pzNX7U1i5NwFzRtth4bRBc     |                  일반 지갑 주소                 |
|     1J8spy62o7z2AjQxoUpiCGnBh5cRWKVWJC     |                  일반 지갑 주소                 |
|     14hVKm7Ft2rxDBFTNkkRC3kGstMGp2A4hk     |                  일반 지갑 주소                 |
|     16ENLdHbnmDcEV8iqN4vuyZHa7sSdYRh76     |                  일반 지갑 주소                 |
|     16sYqXancDDiijcuruZecCkdBDwDf4vSEC     |                  일반 지갑 주소                 |
| bc1q3wzxvu8yhs8h7mlkmf7277wyklkah9k4sm9anu |                  일반 지갑 주소                 |
| bc1q8xyt4jxhw7mgqpwd6qfdjyxgvjeuz57jxrvgk9 |                  일반 지갑 주소                 |



## 분석요약



랜섬웨어 공격 그룹은 암호화폐 자금을 현금화하기 위해 거래소 소유의 지갑 주소에 전송하거나 Bitcoin ATM 및 암호화폐 결제 서비스 주소에 전송하는 등 다수의 암호화폐 서비스를 이용하려는 시도가 확인되었다.



### 트랜잭션 추적 중 식별된 암호화폐 서비스 목록



{% tabs %}
{% tab title="Exchange" %}
* Bibox
* Binance
* Bithumb
* Bitmart
* Bitmex
* Bitrue
* Bitstamp
* Bittrex
* Bitzlato
* Bybit
* Coinbase
* Coincola
* Crypto.com
* Ferma.cc
* Garantex
* Gate.io
* Gemini
* Huobi
* Hydra market
* Ice3
* Kraken
* KuCoin
* Localbitcoins
* Luno
* MEXC
* NairaEx
* Nexo
* OKX
* Paxful
* TradeOgre
* Upbit
* ...
{% endtab %}

{% tab title="Mining pool" %}
* Discus fish
{% endtab %}

{% tab title="Payment Processor" %}
* Coinspaid
* Coinpayments
{% endtab %}

{% tab title="ATM" %}
* Bitcoin Depot
{% endtab %}

{% tab title="Converter" %}
* renBTC
{% endtab %}
{% endtabs %}



암호화폐 자금 중 일부는 Lazarus 그룹으로 식별되는 주소로 전송되기도 했으며 관련 주소는 다음과 같다.

* 3B9yt9LVFW6Fv6cMZSfJL1mgSj2ZewBqSv [#lazarus-group](bc1q3wzxvu8yhs8h7mlkmf7277wyklkah9k4sm9anu.md#lazarus-group "mention")
* bc1ql0j5kuklmuvcejthxmdp66eyxrwtdy08tp5v36 [#lazarus-group](bc1q3wzxvu8yhs8h7mlkmf7277wyklkah9k4sm9anu.md#lazarus-group "mention")
* 121AkmEbHBX9FuFeuDWv2CpyHqNq9F18k9 [#lazarus-group](1kcwfcugnsy3pznx7u1i5nwfzrtth4brbc.md#lazarus-group "mention")
* 1C5qLPgqW4Ed6PuyLHPqXpdF2gQ1EEnJ65 [#lazarus-group](1kcwfcugnsy3pznx7u1i5nwfzrtth4brbc.md#lazarus-group "mention")



암호화폐 추적을 회피하기 위한 행위로 다음 행위를 수행한 것이 확인됐다.

* Coinjoin [#coinjoin](bc1q3wzxvu8yhs8h7mlkmf7277wyklkah9k4sm9anu.md#coinjoin "mention")
* Wasabi Coinjoin [#wasabi-coinjoin](bc1q3wzxvu8yhs8h7mlkmf7277wyklkah9k4sm9anu.md#wasabi-coinjoin "mention")
* Joinmarket Coinjoin [#joinmarket-coinjoin](16syqxancddiijcuruzecckdbdwdf4vsec.md#joinmarket-coinjoin "mention")
* Peel Chain [#peel-chain](1kcwfcugnsy3pznx7u1i5nwfzrtth4brbc.md#peel-chain "mention")
* Chain Hopping [#chain-hopping](bc1q8xyt4jxhw7mgqpwd6qfdjyxgvjeuz57jxrvgk9.md#chain-hopping "mention")



분석 대상 각 지갑 주소의 트랜잭션 분석 중 동일한 주소가 발견되기도 했다.

|                공통적으로 검출된 주소                |    클러스터   |                                       美 CISA 공개 지갑 주소                                       |
| :----------------------------------------: | :-------: | :-----------------------------------------------------------------------------------------: |
|     1FX4W9rrG4F3Uc7gJ18GCwGab8XuW8Ajy2     |  Binance  | <p><em>1FX4W9rrG4F3Uc7gJ18GCwGab8XuW8Ajy2</em></p><p>16sYqXAncDDiijcuruZecCkdBDwDf4vSEC</p> |
|     19rpCFxpAtuR9T7LmHm53mvGt65m8ju5Vp     |  Binance  |       <p>1KmWW6LgdgykBBrSXrFu9kdoHZ95Fe9kQF<br>1KCwfCUgnSy3pzNX7U1i5NwFzRtth4bRBc</p>       |
|     1KmWW6LgdgykBBrSXrFu9kdoHZ95Fe9kQF     |  Binance  | <p><em>1KmWW6LgdgykBBrSXrFu9kdoHZ95Fe9kQF</em></p><p>1KCwfCUgnSy3pzNX7U1i5NwFzRtth4bRBc</p> |
|     1NDyJtNTjmwk5xPNhjgAMu4HDHigtobu1s     |  Binance  |       <p>1FX4W9rrG4F3Uc7gJ18GCwGab8XuW8Ajy2<br>1KmWW6LgdgykBBrSXrFu9kdoHZ95Fe9kQF</p>       |
| bc1qns9f7yfx3ry9lj6yz7c9er0vwa0ye2eklpzqfw | Coinspaid |   <p>bc1q8xyt4jxhw7mgqpwd6qfdjyxgvjeuz57jxrvgk9<br>1KCwfCUgnSy3pzNX7U1i5NwFzRtth4bRBc</p>   |
| bc1quq29mutxkgxmjfdr7ayj3zd9ad0ld5mrhh89l2 |   Gemini  |   <p>bc1q3wzxvu8yhs8h7mlkmf7277wyklkah9k4sm9anu<br>1J8spy62o7z2AjQxoUpiCGnBh5cRWKVWJC</p>   |



### 특징

1. 트랜잭션 도중 분리되어 전송된 자금들 중 작은 금액이 아님에도 불구하고 방치된 것이 꽤 있다.
2. **Coinjoin**과 **Peel Chain** 기법을 주로 사용했다.
3. renBTC를 이용한 **Chain Hopping** 기법을 사용했다.
4. 자금을 전송한 거래소 중 많은 비중을 차지한 거래소는 "**Binance**" 이다.
5. 7개의 주요 분석 대상 지갑 주소에서는 2018년 9월부터 2022년 12월까지 트랜잭션이 발생했다.
6. 일부 자금은 Lazarus 그룹의 주소로 전송되었다.
7. 다크 웹 거래소인 Hydra Market을 사용한 기록이 있다.

