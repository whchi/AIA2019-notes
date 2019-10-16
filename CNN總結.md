# summary
* local connectivity: 一般而言相近的pixel的特徵比較相近
* weight sharing: 不同的區域可以使用共同特徵(一個特徵會出現在一張影像的不同地方)
* Handling input channels: 厚度(RGB), 有幾個channel, filter就會有幾層厚度(1024x1024x3 uses 3x3x3)
* Handling output map: feature map 也是有厚度
epohc === run all batch\
iter === batch
## AlexNet
* why relu is faster than sigmoid?
see image then you can know
## VGGNet
multiple scale training: 不同解析度的訓練
[補充](https://medium.com/@danjtchen/vgg-%E6%B7%B1%E5%BA%A6%E5%AD%B8%E7%BF%92-%E5%8E%9F%E7%90%86-d31d0aa13d88)
## GoogLeNet
* inception module

Linear decrease in feature maps results in quadratic decrease in
computation
用1x1 filter 計算不同 pixel 在不同 channel 中的 iter
filter減半, 每個filter產出的feature map也減半, 所以計算量成冪次下降
* auxiliary classifiers
## ResNet

## DenseNet
## Network comparison


# QA
* 請問在keras範例裡 lr 沒有用到，如果要設定 lr 要在哪裡設定？還是keras 不再需要設定 lr？
* 要設定多少filters 是靠感覺的嗎？還是有什麼憑藉基礎可作參考？
* 當 training 效果不佳時，怎麼知道問題是出在參數還是在資料處理上？像是要優先加入刪除某些 feature 還是先調整參數？
* 請問在 CNN_CV-2.pdf p.16 裡面提到的 "multiple scale training", 有沒有甚麼理論可以解釋這樣的實驗結果嗎?
* 請問在 CNN_CV-2.pdf p.36 圖橫軸的 iter. 是指 epoch嗎? 為什麼在某些 iter. 的 error會大幅下降?

learning rate 設定的問題, 不同learning rate 有不同的loss
* 在 MaxPooling2D 之後為什麼還要 Dropout？是Dropout掉什麼？
* 目前看到的channel都是RGB 請問有用過YCbCr當輸入資料的嗎？
* image有三個channel(三層2D image), 為何跟三層的一個filter捲積後，一定要相加成為一個一層的feature map, 不能保留變成三層* 的feature map嗎? 然後一定要用相加嗎? 不能有加權的概念嗎? 譬如 0.2xR+0.2xG+0.6xB
* Image size can be reduced after stride and pooling. So stride in convolution can replace pooling ?
* 旋轉的image, 我們多用data augmentation來增加training data的豐富程度；那幾何上的旋轉(也就是旋轉幾度)，可以表示成神經網路* 嗎? 也就是旋轉幾度 變成 神經網路裡的weight，然後可以透過學習而得
* Inception Module 裡面 1x1 conv, 3x3 conv, 5x5 conv, 可以透過padding, 讓這三者的output 大小尺寸一樣，但是最右邊的* 3x3 max pooling, 不是就使得output變成input的1/3, 怎麼跟前三者 concatenate在一起?
* 能否再解釋一下為何要使用 1x1 conv
