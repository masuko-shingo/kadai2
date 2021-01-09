# kadai2
ロボットシステム学2020課題2
# 概要

「ROS」を入力するとモールス信号での”R”,”O”,”S”がledで光り、「1」を入力するとledが点灯、「0」を入力するとledが消灯するプログラムです。

改造した部分は、出力を行うGPIOピンをGPIO:25からGPIO:21に変更しています。




# 動作環境
|||
|:--:|:--:|
| Raspberry Pi | Raspberry Pi Model 3B+ |
| OS | Ubuntu 20.04 |
| ROS | ROS Noetic |

# 実行方法
```
$ cd ~/catkin/src
$ git clone https://github.com/masuko-shingo/kadai2.git     //このリポジトリをローカルにクローンする
$ cd ..
$ catkin_make     //ビルドする
$ cd src/kadai2/myled
$ make    //コンパイル
$ sudo insmod myled.ko      //カーネルモジュールのインストール
$ sudo chmod 666 /dev/myled0      //パーミッションの変更
$ roslaunch kadai2 led.launch     //ローンチファイルの実行
$ sudo rmmod myled.ko       //カーネルモジュールのアンインストール
```

# 回路図
![回路図ロボシス課題１](https://user-images.githubusercontent.com/72721963/101239901-aa4b0a80-372e-11eb-9ddb-fcbab11e1ce7.png)

# 動画

# Copyright
Copyright © (Free Software Foundation, Inc.) 2020  Sayaka Toda + Shingo Masuko. 

This program is free software: you can redistribute it and/or modify
    it under the terms of the GNU General Public License as published by
    the Free Software Foundation, either version 3 of the License, or
    (at your option) any later version.

This program is distributed in the hope that it will be useful,
    but WITHOUT ANY WARRANTY; without even the implied warranty of
    MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
    GNU General Public License for more details.

You should have received a copy of the GNU General Public License
    along with this program.  If not, see <http://www.gnu.org/licenses/>.
