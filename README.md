# SyulimeTracker_BusIO

AdafruitのBusIOライブラリ、`Adafruit_BusIO`を改造したものです。

# 変更点

デフォルトではこのライブラリ単体によってI2Cのピンを変更出来ません。  
しかし、ESP32は内部のGPIO MatrixによってI2Cのピンを変更する事ができます。  
(ArduinoでもソフトウェアI2Cを用いる事で変更可能である。)

そこで、通常はI2Cアドレスを渡すコンストラクタにSDA、SCLピンの番号を渡すようにしました。  
内部的には`<Wire>.begin`に対してピン番号を渡しているだけになります。  

# インストール

このライブラリを単体で利用することはほぼないと思います。  
利用するには、この依存ライブラリを使用した[`nattyan-tv/SyulimeTracker_BNO08x`](https://github.com/nattyan-tv/SyulimeTracker_BNO08x)などを利用してください。
