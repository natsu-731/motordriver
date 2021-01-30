# モーターを正転・逆転する


## 必要なパーツ

| メーカー | 秋月 通販コード | 型番 | 商品名 | 個数 |
|--|--|--|--|--:|
| 東芝 | K-14753 | AE-TB67H450 | モータードライバ | 1 |

| TAMIYA | - | ITEM 70168 | ダブルギヤボックス | 1 |



## 配線

PIN 20 と PIN 21 をモーターコントローラーに接続しています。
黒い線は GND、赤い線は5V電源を接続しています。


@soruma
images フォルダに移動
3 months ago
18
<img src='https://raw.githubusercontent.com/libertyfish-co/ruby-hw/master/images/motor_forward_and_back.png' alt='モーターを正転・逆転する 回路図' width="400" />
@soruma
1日目資料追加
2 years ago



## コーディングに必要な情報

AE-TB67H450 はモーターコントローラーです。TA7291P を用いれば、モーターの正転・逆転を制御できます。
@soruma
外部リンクを別ウィンドウで開く
3 months ago

[TB67H450 データシート](https://toshiba.semicon-storage.com/info/docget.jsp?did=65345&prodName=TB67H450FNG){:target='_blank'} を確認してみましょう。TB67H450 の切り欠け側が、PIN 1番です。
@soruma
1日目資料追加
2 years ago

「端子説明」と「ファンクション」を参照します。
25
ファンクションの `OUT` に `H` が出力されれば、モーターに電流が流れます。
26

27
TA7291P の PIN 4番(Vref) を PWM のピンに繋げています。
28
これで、Vrefの値によってモーターの速度が変わります。
29

30
## Let's try
31

32
1. モーターを正転してみましょう
33
1. ジャンパーピンを差し替えることなくモーターを逆転してみましょう
34
1. Vref を変更して速度を変更してみましょう(0〜5vまで設定可能)
@soruma
回答例へのリンクを追加
3 months ago
35

36
回答例は[こちら](https://github.com/libertyfish-co/ruby-hw/blob/master/answers/output/motor_forward_and_back/motor_forward_and_back.rb){:target='_blank'}
