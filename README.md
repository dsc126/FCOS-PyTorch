# FCOS

## Setup
```bash
$ pip install -r Requirements.txt
```

## Data preparation

Download the training, validation, test data and VOCdevkit
```bash
$ wget http://host.robots.ox.ac.uk/pascal/VOC/voc2007/VOCtrainval_06-Nov-2007.tar
$ wget http://host.robots.ox.ac.uk/pascal/VOC/voc2007/VOCtest_06-Nov-2007.tar
$ wget http://host.robots.ox.ac.uk/pascal/VOC/voc2007/VOCdevkit_08-Jun-2007.tar
```
Extract all of these tars into one directory named ```VOCdevkit```

```bash
$ tar xvf VOCtrainval_06-Nov-2007.tar
$ tar xvf VOCtest_06-Nov-2007.tar
$ tar xvf VOCdevkit_08-Jun-2007.tar
```

It should have this basic structure

```bash
$VOCdevkit/                           # development kit
$VOCdevkit/VOCcode/                   # VOC utility code
$VOCdevkit/VOC2007                    # image sets, annotations, etc.
# ... and several other directories ...
```
Follow similar steps to get PASCAL VOC 2012. Now we have 
```bash
$VOCdevkit/                           # development kit
$VOCdevkit/VOCcode/                   # VOC utility code
$VOCdevkit/VOC2007                    # image sets, annotations, etc.
$VOCdevkit/VOC2012                    # image sets, annotations, etc.
# ... and several other directories ...
```

Create a new directory ```VOC0712``` and merge ```VOC2007``` and ```VOC2012``` except the ```ImageSet``` folder since the merged version is provided as is.

## Train

```bash
$ python train_voc.py --use_tfb
```

## Test

```bash
$ python eval_voc.py --use_tfb
```

## Detect

```bash
$ python detect.py
```

## Model

Link：https://pan.baidu.com/s/1VCv2HS-ToEBDjhXgPPAdRA 
Key：skbh 
