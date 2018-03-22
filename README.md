# ARNet
Regularizing RNNs for Caption Generation by Reconstructing The Past with The Present

## Prerequisites
 - Python 3.6
 - Pytorch 0.12
 - CUDA 8.0

## Image Captioning

### Image Feature Extraction
Download the MSCOCO data from [here](http://cocodataset.org/): train2014, val2014, and test2014, respectively. Uncompress and move them into `data/images/mscoco`.



### Data Pre-processing
You can download and use the data from [here](https://drive.google.com/open?id=1MxKySRCnXN2Q0bBg5Asi_mjJPpNwhtC5):
```bash
unzip -q data.zip
```

You can also pre-process the data by yourself: 
```python
python3.6 prepro_build_vocab.py --word_count_threshold 5
```

After this, you will get the following files:
 - word_to_idx.pkl
 - idx_to_word.pkl
 - bias_init_vector.pkl
 - train_images_captions_index.pkl

Finally, make sure that the `data` folder contains the following files:
 - annotations
 - coco-train-idxs.p
 - captions_index.pkl
 - word_to_idx.pkl
 - idx_to_word.pkl



## Code  Captioning


