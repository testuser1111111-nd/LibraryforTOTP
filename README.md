# LibraryforTOTP

2/18公開

以下のものを含んでます
コピペするかダウンロードするかしたらいいと思います(ライセンスに注意)

 * base32 デコード/エンコード
 * TOTP と HOTP の生成器
 * 汚いコード

また、このコードが.NET6で動くことは確認しています。
たぶん .NET5でも動くとは思います。

下記の(他人の)4リポジトリ中にあるBase32の実装より早いです(最大3~6倍)(ランダムな1Mbyteの変換&再変換にかかる合計時間)
 https://github.com/mirthas/totp-net/blob/master/TOTP/Base32.cs
 https://github.com/Cova8bitdots/Base32/blob/master/Base32.cs
 https://gist.github.com/erdomke/9335c394c5cc65404c4cf9aceab04143
 https://github.com/aspnet/Identity/blob/master/src/Core/Base32.cs
 
ライセンスは、The Unlicenseを採用します。
