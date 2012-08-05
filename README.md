SubsonicPlayerCLI
=================
[Subsonic](http://www.subsonic.org/)に登録した曲をコマンドライン上で再生するBashスクリプト

## 使い方

### 曲を検索する

    % sub test
     1     Drug Test ___ Prisoners Of Love [Disc 2] ___ Yo La Tengo ___ 2f7661722f6d757369632f596f204c612054656e676f2f507269736f6e657273204f66204c6f7665205b4469736320325d2f322d3035204472756720546573742e6d3461
     2     The Litmus Test / Cut Chemist ___ Wonderground Season.03 ___ 三木祐司　 ___ 2f7661722f6d757369632f4d695fe4b889e69ca8e7a590e58fb82f576f6e64657267726f756e6420536561736f6e2e30332f343420546865204c69746d75732054657374205f20437574204368656d6973742e6d3461
     3     フィルムのかたち ___ 極東最前線 2 [Disc 2] ___ TEST PATTERN ___ 2f7661722f6d757369632f436f6d70696c6174696f6e732fe6a5b5e69db1e69c80e5898de7b79a2032205b4469736320325d2f322d313020e38395e382a3e383abe383a0e381aee3818be3819fe381a12e6d3461

- "test"にマッチした曲がリストアップされる

### 曲を再生する

    % sub test | sub 1 3
    MPlayer 1.1-4.2.1 (C) 2000-2012 MPlayer Team
    192 audio & 400 video codecs
    ...

- 検索結果を同コマンドに渡すと再生を始める
- コマンド例では検索結果の1番と3番を順番に再生する
- 番号を入れなければ検索結果全てを順番に再生する

## 注意点
- Subsonicサーバーにパスワードを平文のまま送るので、使用は家庭内LAN内などのみに限定する (https://は未検証)

## 使用ツール
- Lynx
- XMLStarlet
- MPlayer

## 実行環境
- Mac OSX 10.6.8
- Subsonic 4.5
- 使用ツールはMacPorts経由でインストールした
