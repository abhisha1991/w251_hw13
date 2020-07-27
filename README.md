# w251_hw13 by abhisha@berkeley.edu

This homework is based off the week 13 homework given here: https://github.com/MIDS-scaling-up/v2/tree/master/week13/hw

#### Please submit the time it took you to train the model along with the final accuracy top1/top5 that you were able to achieve. 
The top 1 and top 5 accuracy achieved are as follows:
```Acc@1 51.630 Acc@5 83.877```
Please see accuracy.png in this repo for more details.

#### Could you increase the batch size? Why? 
Yes, I was able to increase the batch size from the default value, 8 to 32. We were able to do this on the jetson tx2 without getting OOM because the jetson has sufficient memory to hold 32 image batches.

The following command was used to launch the training
```
root@nvidia-desktop:/data/w251/w251_hw13/jetson-inference/python/training/classification/pytorch-classification# python3 train.py --model-dir=plants --epochs=100 -b=32 /data/w251/w251_hw13/plants/PlantCLEF_Subset
```

#### How long did the training take you? 
The training took a few hours, I didnt track the exact time, but it was easily 3+ hours.
