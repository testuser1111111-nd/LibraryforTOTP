# LibraryforTOTP

以下のものを含んでます

csファイルだけダウンロードしたらいいと思います

 * base32 デコード/エンコード
 * TOTP と HOTP の生成器
 * 汚いコード

また、このコードが.NET6で動くことは確認しています。
たぶん .NET5でも動くとは思います。

Base32の変換にかかる計算量は時間、空間ともにO(n)(ここでnはbyteの長さまたはBase32textの長さ)(詳しくないので間違っていたら教えてください)ですが、定数倍が変なことになって100MBのデータを変換→再変換したら30秒で7GBくらい余裕で食い尽くしてくれたので、使うときは気を付けてください。

10^8byte以上のデータを変換/再変換する際にプログラム側で途中で止めることはないですが、オーバーフローなどでデータが逝かれても知りませんし、そもそも普通の場合ではメモリが足りませんので非推奨(should not)です

早見表(あくまで目安で、保障ではない)↓
| データ長(byte) | 時間(ms) | メモリ(MB) |
| ---- | ---- | ---- |
| 10^2 | 150 ~ 200 | ~ 20 |
| 10^3 | 150 ~ 200 | ~ 20 |
| 10^4 | 150 ~ 250 | 15 ~ 20 |
| 10^5 | 200 ~ 300 | 20 ~ 40 |
| 10^6 | 250 ~ 750 | 40 ~ 60 |
| 10^7 | 2500 ~ 5000 | 600 ~ 800 |
| 10^8 | 25000 ~ 50000 | 6000 ~ 8000 |
| それ以上 | パソコン再起動 | 燃え尽きる |

ライセンスは、NPCAのウェブサイトの利用規約とThe Unlicenseの内重い方を採用します。
