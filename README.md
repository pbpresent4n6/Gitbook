---
layout: editorial
---

# 北 랜섬웨어 관련 비트코인 주소 트랜잭션 추적

## 北 랜섬웨어 관련 韓美 합동 사이버보안 권고



미국 사이버인프라보안청인 CISA에서 2023년 2월 9일 북한 랜섬웨어 관련 한미 합동 사이버 보안 권고문을 발행했다. ([https://www.cisa.gov/uscert/ncas/alerts/aa23-040a](https://www.cisa.gov/uscert/ncas/alerts/aa23-040a))

해당 사이버 보안 권고문은 미국에서 진행 중인 랜섬웨어 예방 캠페인(#StopRansomeware)의 일환으로, 네트워크 방어자들을 위해 다양한 랜섬웨어 변종 및 랜섬웨어 위협 행위자에 대해 상세히 기술하고 있다.

북한 정권이 지원하는 랜섬웨어에 대한 전반적인 내용과 함께 랜섬웨어 공격을 목적으로 의료 및 공중 보건 분야와 기타 중요 인프라 분야 기관에 접근하기 위해 북한 사이버 행위자가 사용한 TTP 및 침해지표와 몸값을 요구하기 위해 암호화폐를 사용하는 것에 대한 정보를 담고 있다.

특히 이번에 발행된 사이버 보안 권고문에는 북한에서 사용하는 것으로 추정되는 비트코인 지갑 주소 43개가 공개되었기 때문에,  본 글에서는 43개의 지갑 주소에 대한 정보를 간략하게 다루고 트랜잭션을 추적한 결과를 다루고자 한다.



## 북한에서 사용하는 것으로 확인되는 43개의 비트코인 지갑  주소



공개된 43개의 비트코인 지갑 주소에 대해 분석한 결과는 아래 표와 같다.



| Wallet Address                             | Tx Count | Received Amount (BTC) | Sent Amount (BTC) | Balance | First Seen Receiving (UTC) | Last Seen Receiving (UTC) | First Seen Sending (UTC) | Last Seen Sending (UTC) |
| ------------------------------------------ | -------- | --------------------- | ----------------- | ------- | -------------------------- | ------------------------- | ------------------------ | ----------------------- |
| 1KmWW6LgdgykBBrSXrFu9kdoHz95Fe9kQF         | 3573     | 922.1659523           | 922.1659523       | 0       | 2019-07-22 09:08:09        | 2021-09-01 21:33:53       | 2019-07-22 10:46:00      | 2021-09-02 00:09:46     |
| 1FX4W9rrG4F3Uc7gJ18GCwGab8XuW8Ajy2         | 3464     | 1126.67631961         | 1126.67631961     | 0       | 2018-10-02 09:52:25        | 2020-06-06 05:12:51       | 2018-10-02 13:03:12      | 2020-06-06 14:03:08     |
| 1KCwfCUgnSy3pzNX7U1i5NwFzRtth4bRBc         | 6        | 0.0361                | 0.0361            | 0       | 2021-05-13 19:30:47        | 2022-12-25 23:59:15       | 2021-05-14 21:26:36      | 2022-12-27 12:49:31     |
| 1J8spy62o7z2AjQxoUpiCGnBh5cRWKVWJC         | 5        | 1.87482707            | 1.87482707        | 0       | 2021-05-11 19:52:04        | 2021-05-17 21:02:25       | 2021-05-12 09:15:59      | 2021-06-25 03:34:00     |
| 14hVKm7Ft2rxDBFTNkkRC3kGstMGp2A4hk         | 4        | 10                    | 10                | 0       | 2018-09-14 15:57:05        | 2018-09-14 18:20:18       | 2018-09-14 16:38:07      | 2018-09-14 18:20:18     |
| 16ENLdHbnmDcEV8iqN4vuyZHa7sSdYRh76         | 2        | 0.00064181            | 0.00064181        | 0       | 2021-05-12 09:15:59        | 2021-05-12 09:15:59       | 2021-06-25 03:34:00      | 2021-06-25 03:34:00     |
| 16sYqXancDDiijcuruZecCkdBDwDf4vSEC         | 2        | 0.06                  | 0.06              | 0       | 2019-07-24 18:51:27        | 2019-07-24 18:51:27       | 2019-07-25 14:56:16      | 2019-07-25 14:56:16     |
| bc1q3wzxvu8yhs8h7mlkmf7277wyklkah9k4sm9anu | 2        | 2.54                  | 2.54              | 0       | 2022-03-30 15:49:37        | 2022-03-30 15:49:37       | 2022-03-30 23:14:34      | 2022-03-30 23:14:34     |
| bc1q8xyt4jxhw7mgqpwd6qfdjyxgvjeuz57jxrvgk9 | 2        | 0.51256               | 0.51256           | 0       | 2022-05-24 03:24:15        | 2022-05-24 03:24:15       | 2022-07-05 07:24:58      | 2022-07-05 07:24:58     |
| 1MTHBCrBKYEthfa16zo9kabt4f9jMJz8Rm         | 0        | 0                     | 0                 | 0       |                            |                           |                          |                         |
| 1NqihEqYaQaWiZkPVdSMiTbt7dTy1LMxgX         | 0        | 0                     | 0                 | 0       |                            |                           |                          |                         |
| 1N6JphHFaYmYaokS5xH31Z67bvk4ykd9CP         | 0        | 0                     | 0                 | 0       |                            |                           |                          |                         |
| bc1q80vc4yjgg6umedkut3e9mhehxl4q4dcjjyzh59 | 0        | 0                     | 0                 | 0       |                            |                           |                          |                         |
| bc1qlqgu2l2kms5338zuc95kxavctzyy0v705tpvyc | 0        | 0                     | 0                 | 0       |                            |                           |                          |                         |
| bc1qy6su7vrh7ts5ng2628escmhr98msmzg62ez2sp | 0        | 0                     | 0                 | 0       |                            |                           |                          |                         |
| bc1q8t69gpxsezdcr8w6tfzp3jeptq4tcp2g9d0mwy | 0        | 0                     | 0                 | 0       |                            |                           |                          |                         |
| bc1q9h7yj79sqm4t536q0fdn7n4y2atsvvl22m28ep | 0        | 0                     | 0                 | 0       |                            |                           |                          |                         |
| bc1qj6y72rk039mqpgtcy7mwjd3eum6cx6027ndgmd | 0        | 0                     | 0                 | 0       |                            |                           |                          |                         |
| bc1qcp557vltuu3qc6pk3ld0ayagrxuf2thp3pjzpe | 0        | 0                     | 0                 | 0       |                            |                           |                          |                         |
| bc1ql8wsflrjf9zlusauynzjm83mupq6c9jz9vnqxg | 0        | 0                     | 0                 | 0       |                            |                           |                          |                         |
| bc1qx60ec3nfd5yhsyyxkzkpts54w970yxj84zrdck | 0        | 0                     | 0                 | 0       |                            |                           |                          |                         |
| bc1qunqnjdlvqkjuhtclfp8kzkjpvdz9qnk898xczp | 0        | 0                     | 0                 | 0       |                            |                           |                          |                         |
| bc1q6024d73h48fnhwswhwt3hqz2lzw6x99q0nulm4 | 0        | 0                     | 0                 | 0       |                            |                           |                          |                         |
| bc1qwdvexlyvg3mqvqw7g6l09qup0qew80wjj9jh7x | 0        | 0                     | 0                 | 0       |                            |                           |                          |                         |
| bc1qavrtge4p7dmcrnvhlvuhaarx8rek76wxyk7dgg | 0        | 0                     | 0                 | 0       |                            |                           |                          |                         |
| bc1qagaayd57vr25dlqgk7f00nhz9qepqgnlnt4upu | 0        | 0                     | 0                 | 0       |                            |                           |                          |                         |
| bc1quvnaxnpqlzq3mdhfddh35j7e7ufxh3gpc56hca | 0        | 0                     | 0                 | 0       |                            |                           |                          |                         |
| bc1qu0pvfmtxawm8s99lcjvxapungtsmkvwyvak6cs | 0        | 0                     | 0                 | 0       |                            |                           |                          |                         |
| bc1qg3zlxxhhcvt6hkuhmqml8y9pas76cajcu9ltdl | 0        | 0                     | 0                 | 0       |                            |                           |                          |                         |
| bc1qn7a3g23nzpuytchyyteyhkcse84cnylznl3j32 | 0        | 0                     | 0                 | 0       |                            |                           |                          |                         |
| bc1qhfmqstxp3yp9muvuz29wk77vjtdyrkff4nrxpu | 0        | 0                     | 0                 | 0       |                            |                           |                          |                         |
| bc1qnh8scrvuqvlzmzgw7eesyrmtes9c5m78duetf3 | 0        | 0                     | 0                 | 0       |                            |                           |                          |                         |
| bc1q7qry3lsrphmnw3exs7tkwzpvzjcxs942aq8n0y | 0        | 0                     | 0                 | 0       |                            |                           |                          |                         |
| bc1qcmlcxfsy0zlqhh72jvvc4rh7hvwhx6scp27na0 | 0        | 0                     | 0                 | 0       |                            |                           |                          |                         |
| bc1q498fn0gauj2kkjsg35mlwk2cnxhaqlj7hkh8xy | 0        | 0                     | 0                 | 0       |                            |                           |                          |                         |
| bc1qnz4udqkumjghnm2a3zt0w3ep8fwdcyv3krr3jq | 0        | 0                     | 0                 | 0       |                            |                           |                          |                         |
| bc1qk0saaw7p0wrwla6u7tfjlxrutlgrwnudzx9tyw | 0        | 0                     | 0                 | 0       |                            |                           |                          |                         |
| bc1qyue2pgjk09ps7qvfs559k8kee3jkcw4p4vdp57 | 0        | 0                     | 0                 | 0       |                            |                           |                          |                         |
| bc1q6qfkt06xmrpclht3acmq00p7zyy0ejydu89zwv | 0        | 0                     | 0                 | 0       |                            |                           |                          |                         |
| bc1qmge6a7sp659exnx78zhm9zgrw88n6un0rl9trs | 0        | 0                     | 0                 | 0       |                            |                           |                          |                         |
| bc1qcywkd7zqlwmjy36c46dpf8cq6ts6wgkjx0u7cn | 0        | 0                     | 0                 | 0       |                            |                           |                          |                         |
| LZ1VNJfn6mWjPzkCyoBvqWaBZYXAwn135          |          |                       |                   |         |                            |                           |                          |                         |
| bc1qxrpevck3pq1yzrx2pq2rkvkvy0jnm56nzjv6pw |          |                       |                   |         |                            |                           |                          |                         |



















