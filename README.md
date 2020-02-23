# Apex Trainer Example


## Install Apex

- apex: `git clone https://github.com/NVIDIA/apex; cd apex; pip install -v --no-cache-dir --global-option="--cpp_ext" --global-option="--cuda_ext" ./`

## Results:

Trained with 2080Ti

### faster rcnn
lr sched 1x 
| Name | train time(s/iter)|infer time(s/im)|train mem(GB)|box AP|
|:------:|:------:|:------:|:------:|:------:|
|R50-FPN-V100| 0.210|	0.055|	3.0|37.9|
|R50-FPN| | | | |
|R50-FPN-Apex|0.326|0.051|2.8|40.1|

RetineNet
lr sched 1x 
| Name | train time(s/iter)|infer time(s/im)|train mem(GB)|box AP|
|:------:|:------:|:------:|:------:|:------:|
|R50-V100|0.200|	0.062	|3.9	|36.5|
|R50| | | | |
|R50-Apex|0.258|0.077|3.3|38.3|

Mask R-CNN
lr sched 1x 
| Name | train time(s/iter)|infer time(s/im)|train mem(GB)|box AP|mask AP|
|:------:|:------:|:------:|:------:|:------:|:------:|
|R50-V100|0.261|	0.053	|3.4	|38.6|35.2|
|R50-FPN||||||
|R50-FPN-Apex|0.388|0.057|3.3|40.9|37.2|
