# kadai1

# システム工学・課題１
課題１は講義で扱ったラズパイでLEDを光らせるプログラムです。  

講義中の**sushi**と表示させるプログラムを**fish**と表示させるプログラムにする改造を加えた。    

# 概要
**echo 1 > /dev/myled0**と入力するとLEDが光ります。  
**echo 0 > /dev/myled0**と入力するとLEDが消えます。
**cat /dev/myled0**と入力すると**fish**と表示されます。  

# 使用環境
- Raspberry Pi 3 Model B  
- Ubuntu 18.04 LTS

# 回路の情報
## 使用したもの  
- Raspberry Pi 3 Model B ×1
- ブレッドボード ×1  
- LED ×1
- 抵抗（200Ω）×1
- ジャンパーワイヤー (オス-メス) ×2

## 回路の写真
![IMG_5072](https://user-images.githubusercontent.com/95730326/147661710-c274d459-a296-4fed-9e00-b9bd2fe60101.JPG)

# 操作方法
## LEDの点灯
```   
make                          //コンパイル  
sudo insmod myled.ko  
sudo chmod 666 /dev/myled0  
echo 1 > /dev/myled0　　　　　 //LED点灯  
echo 0 > /dev/myled0 　　　　　//LED消灯
```

## fishの表示
```   
make                          //コンパイル  
sudo insmod myled.ko  
sudo chmod 666 /dev/myled0  
cat /dev/myled0               //fishの表示  
```

# 実演動画
[Youtube・課題１](https://youtu.be/IhJudgNxoRk)

# License
GNU General Public License v3.0
