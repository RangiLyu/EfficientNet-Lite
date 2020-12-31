# EfficientNet-Lite Pytorch

Pytorch implementation  of Google's [EfficientNet-lite](https://github.com/tensorflow/tpu/tree/master/models/official/efficientnet/lite). Provide imagenet pre-train models.

In EfficientNet-Lite, all SE modules are removed and all swish layers are replaced with ReLU6. It's more friendly for edge devices than EfficientNet-B series.


Model details:

|**Model** | **Params** | **MAdds** | **Top1 Acc(Official)** | **Top1 Acc(This repo)** | **Top5 Acc**|
|----------|-----|-------|-------|-------|-------|
|efficientnet-lite0 | 4.7M | 407M |  75.1% | 71.73% |90.17% | 
|efficientnet-lite1 | 5.4M | 631M |  76.7% | 74.71% |92.01% | 
|efficientnet-lite2 | 6.1M | 899M |  77.6% | 77.14% |93.54% | 
|efficientnet-lite3 | 8.2M | 1.44B |  79.8% | 78.91% |94.37% | 
|efficientnet-lite4 |13.0M | 2.64B |  81.5% | 80.34% |95.06% | 

## Download Model

|**Pre-train Model** |
|----------|
|efficientnet-lite0 [Download Link](https://github.com/RangiLyu/EfficientNet-Lite/releases/download/v1.0/efficientnet_lite0.pth) |
|efficientnet-lite1 [Download Link](https://github.com/RangiLyu/EfficientNet-Lite/releases/download/v1.0/efficientnet_lite1.pth) |
|efficientnet-lite2 [Download Link](https://github.com/RangiLyu/EfficientNet-Lite/releases/download/v1.0/efficientnet_lite2.pth) |
|efficientnet-lite3 [Download Link](https://github.com/RangiLyu/EfficientNet-Lite/releases/download/v1.0/efficientnet_lite3.pth) |
|efficientnet-lite4 [Download Link](https://github.com/RangiLyu/EfficientNet-Lite/releases/download/v1.0/efficientnet_lite4.pth) |

## Train

```
python train.py --model_name efficientnet_lite0 --train_dir YOUR_TRAINDATASET_PATH --val_dir YOUR_VALDATASET_PATH
```

## Eval

```
python train.py --eval --eval_resume YOUR_MODEL_PATH --model_name efficientnet_lite0  --train_dir YOUR_TRAINDATASET_PATH --val_dir YOUR_VALDATASET_PATH
```

eval reaults:

```
efficientnet_lite0
TEST Iter 0: loss = 2.100231,     Top-1 err = 0.282700,   Top-5 err = 0.098280,   val_time = 120.648957

efficientnet_lite1
TEST Iter 0: loss = 2.076898,     Top-1 err = 0.252940,   Top-5 err = 0.079880,   val_time = 126.869352

efficientnet_lite2
TEST Iter 0: loss = 1.929238,     Top-1 err = 0.228660,   Top-5 err = 0.064640,   val_time = 142.668548

efficientnet_lite3
TEST Iter 0: loss = 1.782202,     Top-1 err = 0.210920,   Top-5 err = 0.056260,   val_time = 147.359098

efficientnet_lite4
TEST Iter 0: loss = 1.714834,     Top-1 err = 0.196580,   Top-5 err = 0.049440,   val_time = 158.336004
```


