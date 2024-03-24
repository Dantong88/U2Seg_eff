## Efficient Learning

In our main paper, we show results for efficient learning in section 4.5, which we provide code to reproduce our results.

### 1. Installation
Since the efficient learning takes the original detectron2 evaulation metrics for evaualtion of the instance segmentation,
semantic segmentation and panoptic segmentatin, while our U2Seg build on our own evaulation based on  that, so the main branch of the repo is adapted for specific use
for U2Seg. So in order to evaluate the efficient learning, users need to build a clean environment with the following steps.

#### Create a conda environment
```angular2html
conda create --name u2seg_eff python=3.8.1
conda activate u2seg_eff
```

#### Install the Pytorch
```angular2html

```

#### build this repo
```angular2html
git clone this repo
cd this repo
pip install -e.
```

### 2. Dataset Preparason
Follwing the offical detectron2 dataset saving structure, user should
download the MS COCO dataset and save it as:

```angular2html
this repo/
    datasets/
        coco/
            annotations/
                        panoptic_{train, val}2017.json
                        coco-semi/
                                {1, 5, 10, 20, 30, 40, 50}perc_instances_train2017.json
            {train, val}2017/
                            163330523.jpg
                            163330524.jpg
                            ...
            panoptic_stuff_{train, val}2017

                    
```
