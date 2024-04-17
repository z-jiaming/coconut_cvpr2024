# [CVPR2024] 🥥COCONut: Crafting the Future of Segmentation Datasets with Exquisite Annotations in the Era of ✨Big Data✨
Xueqing Deng, Qihang Yu, Peng Wang, Xiaohui Shen, Liang-Chieh Chen

[![Dataset](https://img.shields.io/badge/Dataset-Access-<COLOR>)](https://www.kaggle.com/datasets/xueqingdeng/coconut/)
[![Website](https://img.shields.io/badge/Project-Website-87CEEB)](https://xdeng7.github.io/coconut.github.io/)
[![paper](https://img.shields.io/badge/arXiv-Paper-<COLOR>.svg)](https://arxiv.org/abs/2404.08639)
[![Full Paper](https://img.shields.io/badge/Full_Paper-Read-0000FF.svg)](coconut_arxiv.pdf)


## 🚀 Contributions

#### 🔥 1st large-scale human verified dataset for segmentation, more info can be found at our [website](https://xdeng7.github.io/coconut.github.io/).

#### 🔥 COCONut is now available at [Kaggle](https://www.kaggle.com/datasets/xueqingdeng/coconut/), welcome to download!

<p>
<img src="static/vis_masks_video_tasks_v2.gif" alt="teaser" width=90% height=90%>
</p>


## 📢 News!
* 4/16: COCONut is available at Kaggle! Tutorial is coming! Stay tuned!
* 4/15: COCONut is higlighted by AK's [daily paper](https://huggingface.co/papers?date=2024-04-15)!
* 4/15: Huggingface download links are temporarily closed.

### TODO
- [ ] Huggingface dataset preview
- [ ] Release code to merge dataset split
- [ ] Convert the annotation to instance/semantic segmentation and object detection.
- [ ] Release COCONut-L and COCONut-val by the end of April

## Dataset splits
Splits    |  #images | #masks | images | annotations
----------|----------|--------|--------|-------------
COCONut-S | 118K     | 1.54M  | [download](http://images.cocodataset.org/zips/train2017.zip) | [huggingface](https://huggingface.co/datasets/xdeng77/coconut_cvpr2024/blob/main/coconut_s.zip)
COCONut-B | 242K     | 2.78M  | [download](http://images.cocodataset.org/zips/unlabeled2017.zip) | [huggingface](https://huggingface.co/datasets/xdeng77/coconut_cvpr2024/blob/main/coconut_b.zip)
COCONut-L | 358K     | 4.75M  | [coming]() | [coming]()
relabeled-COCO-val | 5K | 67K | [download](http://images.cocodataset.org/zips/val2017.zip) | [huggingface](https://huggingface.co/datasets/xdeng77/coconut_cvpr2024/blob/main/relabeled_coco_val.zip)
COCONut-val | 25K     | 437K  | [coming]() | [coming]()

To use the masks, you will need to download the corresponding segments info json files, for example, download [coconut_s.json](https://huggingface.co/datasets/xdeng77/coconut_cvpr2024/blob/main/coconut_s.json) for using masks in [coconut_s.zip](https://huggingface.co/datasets/xdeng77/coconut_cvpr2024/blob/main/coconut_s.zip).

## Get started

* Please refer to [get_started.md](get_started.md) for detailed instruction of using the dataset.

[COCONut-S](https://huggingface.co/datasets/xdeng77/coconut_cvpr2024/tree/main), [COCONut-B](https://huggingface.co/datasets/xdeng77/coconut_cvpr2024/tree/main), [relabeled-COCO-val](https://huggingface.co/datasets/xdeng77/coconut_cvpr2024/tree/main) and [annotation informations](https://huggingface.co/datasets/xdeng77/coconut_cvpr2024/tree/main)

We only provide the annotation in our huggingface, for those who are interested to use our annotation will need to download the images from the links: [COCONut-S images](http://images.cocodataset.org/zips/train2017.zip), [COCONut-B images](http://images.cocodataset.org/zips/unlabeled2017.zip) and [relabeled COCO-val images](http://images.cocodataset.org/zips/val2017.zip).


  
### Example dataset download scripts to build COCONut-S panoptic train dataset:

1. Download the [panoptic masks](https://huggingface.co/datasets/xdeng77/coconut_cvpr2024/tree/main) and [panoptic segments info](https://huggingface.co/datasets/xdeng77/coconut_cvpr2024/tree/main) from huggingface.
2. Download the train set images from [COCO dataset](http://images.cocodataset.org/zips/train2017.zip).
3. To use the dataset loader from detectron2, you will need to rename the mask folder to 'panoptic_train2017' and annotation file to 'panoptic_train2017.json'.

The dataset structure should be as follow:


```
COCONut-S
  train2017
  panoptic_train2017
  annotations
    panoptic_train2017.json
```

If you find our dataset useful, please cite:
```
@inproceedings{coconut2024cvpr,
  author    = {Xueqing Deng, Qihang Yu, Peng Wang, Xiaohui Shen, Liang-Chieh Chen},
  title     = {COCONut: Modernizing COCO Segmentation},
  booktitle   = {Proceedings of the IEEE/CVF Conference on Computer Vision and Pattern Recognition},
  year      = {2024},
```

## More visualization on COCONut annotation
<p>
<img src="static/vis_simple_mask.png" alt="vis1" width=90% height=90%>
</p>
<p>
<img src="static/vis_dense_mask.png" alt="vis2" width=90% height=90%>
</p>

## Terms of use
We follow the same license as [COCO dataset for images](https://cocodataset.org/#termsofuse). For COCONut's annotations, non-commercial use are allowed. 

## Acknowledgement
* [kMax-DeepLab](https://github.com/bytedance/kmax-deeplab.git)
* [FC-CLIP](https://github.com/bytedance/fc-clip.git)
* [detectron2](https://github.com/facebookresearch/detectron2.git)

