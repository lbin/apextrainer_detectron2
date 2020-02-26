# Apex Trainer Example


## Install Apex

- apex: `pip install -v --no-cache-dir --global-option="--cpp_ext" --global-option="--cuda_ext" --upgrade 'git+https://github.com/NVIDIA/apex'`

## Results:

Trained with 2080Ti

### faster rcnn
lr sched 1x 
| Name | train time(s/iter)|infer time(s/im)|train mem(GB)|box AP|
|:------:|:------:|:------:|:------:|:------:|
|R50-FPN-V100| 0.210|	0.055|3.0|37.9|
|R50-FPN|0.312 |0.056 | 2.893| 37.9|
|R50-FPN-Apex|0.322|0.053|2.793|38.0|

### RetineNet
lr sched 1x 
| Name | train time(s/iter)|infer time(s/im)|train mem(GB)|box AP|
|:------:|:------:|:------:|:------:|:------:|
|R50-V100|0.200|	0.062	|3.9	|36.5|
|R50| 0.285|0.079 |3.934 | 36.5|
|R50-Apex|0.248|0.067|3.275|36.4|

### Mask R-CNN
lr sched 1x 
| Name | train time(s/iter)|infer time(s/im)|train mem(GB)|box AP|mask AP|
|:------:|:------:|:------:|:------:|:------:|:------:|
|R50-V100|0.261|	0.053	|3.4	|38.6|35.2|
|R50-FPN|0.348 |0.063 | 3.44|38.5|35.1|
|R50-FPN-Apex|0.363|0.061|3.26|38.6|35.2|
