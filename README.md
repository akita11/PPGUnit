# PPG Clip

<img src="https://github.com/akita11/PPGUnit/blob/main/PPGUnit.jpg" width="240px">

M5Stack社の心拍センサユニット(https://www.switch-science.com/products/5695)と機能的に互換のUnitです。
光学脈波(PPG)センサのMAX30100を使用し、光学脈波やSpO2、そこから心拍数の計測ができます。
また[PPG Clip部品セット](https://github.com/akita11/PPGclip)と組み合わせることで、透過型PPG計測装置をつくることができます。

※センサICのMAX30100は、再生品を使用している場合があります。基本的な測定には問題がないことは確認済みですが、新品とは多少の性能の差異がある場合があります。

## 使い方

M5Stack社の心拍センサユニット(https://www.switch-science.com/products/5695)と機能的に互換ですので、そちらのソフトウエア(Arduino用ライブラリ、UIFlow等)がそのまま使用できます。


## 作り方

2枚の基板を、向きをあわせて、2組の4pピンヘッダではんだ付けします。
ピンヘッダの足は十分に短くカットしてください。

## 補足情報(I2C信号線について)

MAX10300のI2C信号線の端子の絶対最大定格は6.0Vです。
I2C信号線のプルアップ抵抗はGroveコネクタのVDD側(M5Stackシリーズでは5V)に接続されており、HレベルはVDD電圧（同5V）となりますが、絶対最大定格を超えません。
M5Stack社の心拍センサユニットでは、ここに電圧変換用の部品が入っていますが、I2C信号の波形を観測したところ、立ち下がり速度がかなり遅く、特に400kHz通信の場合には通信エラーが多発する現象が確認されましたので、この構成としています。


## Author

Junichi Akita (@akita11) / akita@ifdl.jp






