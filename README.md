# mypkg
ROS 2 パッケージのリポジトリです．

# plusコマンド
[![test](https://github.com/SsamXI27/mypkg/actions/workflows/test.yml/badge.svg)](https://github.com/SsamXI27/mypkg/actions/workflows/test.yml)

## それぞれの説明
* talker.py
  * パブリッシャを持つノードであり，数字を/countupを通じて送信する．
* listener.py
  * サブスクライバを持つノードであり，/countupからメッセージを受け取り表示する．
* talk_listen.launch.py
  * talker.pyとlistener.pyを同時に立ち上げる．

## トピックについて
* 本コードではInt16型のメッセージを使用し，countupをトピックとしている．

## 必要なソフトウェア
* Python
  * テスト済み: 3.7~3.10 

## 開発環境
* Ubuntu 20.04
  * ROS 2 Foxy Fitzroy

## テスト環境
* Ubuntu 22.04
  * ROS 2 Humble Hawksbill

## インストール手順
```
$ git clone https://github.com/SsamXI27/mypkg.git
```
## このコードの使用方法
### taker.pyの実行
```
$ ros2 run mypkg talker
```
* 出力結果
  * 表示なし
### listener.pyの実行
* パブリッシャを持つノードを実行させた後，別端末上に以下を入力
  * 今回はtalkerを立ち上げた例
```
$ ros2 run mypkg listener
```
* 出力結果の例
```
[INFO] [1703763832.352170775] [listener]: Listen: 12
[INFO] [1703763832.843576440] [listener]: Listen: 13
[INFO] [1703763833.343520676] [listener]: Listen: 14
[INFO] [1703763833.843938289] [listener]: Listen: 15
[INFO] [1703763834.344401975] [listener]: Listen: 16
[INFO] [1703763834.844508069] [listener]: Listen: 17
[INFO] [1703763835.343582468] [listener]: Listen: 18
[INFO] [1703763835.843793613] [listener]: Listen: 19
[INFO] [1703763836.343617494] [listener]: Listen: 20
[INFO] [1703763836.843872357] [listener]: Listen: 21
[INFO] [1703763837.344143456] [listener]: Listen: 22
```
### talk_listen.launch.pyの実行
```
$ ros2 launch mypkg talk_listen.launch.py
```
* 出力結果の例
```
[INFO] [launch]: All log files can be found below /home/samx/.ros/log/2023-12-28-20-38-28-583970-RX78-2-168
[INFO] [launch]: Default logging verbosity is set to INFO
[INFO] [talker-1]: process started with pid [170]
[INFO] [listener-2]: process started with pid [172]
[listener-2] [INFO] [1703763509.863064274] [listener]: Listen: 0
[listener-2] [INFO] [1703763510.353144200] [listener]: Listen: 1
[listener-2] [INFO] [1703763510.853858128] [listener]: Listen: 2
[listener-2] [INFO] [1703763511.353180955] [listener]: Listen: 3
[listener-2] [INFO] [1703763511.853538734] [listener]: Listen: 4
[listener-2] [INFO] [1703763512.353146903] [listener]: Listen: 5
[listener-2] [INFO] [1703763512.853232460] [listener]: Listen: 6
[listener-2] [INFO] [1703763513.353243984] [listener]: Listen: 7
[listener-2] [INFO] [1703763513.853509347] [listener]: Listen: 8
[listener-2] [INFO] [1703763514.353450107] [listener]: Listen: 9
[listener-2] [INFO] [1703763514.853014284] [listener]: Listen: 10
```
## 著作権とライセンス
* このソフトウェアパッケージは, 3条項BSDライセンスの下, 再頒布および使用が許可されます.  
* このパッケージのコードは, 下記のスライド (CC-BY-SA 4.0 by Ryuichi Ueda)のものを, 本人の許可を得て自身の著者としたものです. 
  * [ryuichiueda/my_slides/robosys_2022](https://github.com/ryuichiueda/my_slides/tree/master/robosys_2022)
* © 2023 Syousei Samitu
