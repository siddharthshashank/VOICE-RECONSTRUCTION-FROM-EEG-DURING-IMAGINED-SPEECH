## Requirements
All algorithm are developed in Python 3.8.

To install requirements:

```setup
pip install -r requirements.txt
```

## Training
To train the model for spoken EEG in the paper, run this command:
```train
python train.py pretrained_model/SpokenEEG/ pretrained_model/UNIVERSAL_V1/g_02500000 --task SpokenEEG_vec --batch_size 20 --pretrain False --prefreeze False
```
To train the model for Imagined EEG with pretrained model of spoken EEG in the paper, run this command:
```train
python train.py pretrained_model/SpokenEEG/ pretrained_model/UNIVERSAL_V1/g_02500000 --task ImaginedEEG_vec --batch_size 20 --pretrain True --prefreeze True
```
>📋 the arguments of models

## Evaluation
To evaluate the trained model for spoken EEG on an example data, run:
```eval
python eval.py pretrained_model/SpokenEEG/ pretrained_model/UNIVERSAL_V1/g_02500000 --task SpokenEEG_vec --batch_size 5
```
To evaluate the trained model for Imagined EEG on an example data, run:
```eval
python eval.py pretrained_model/ImaginedEEG/ pretrained_model/UNIVERSAL_V1/g_02500000 --task ImaginedEEG_vec --batch_size 5
```

## Pre-trained Models
You can download pretrained models here:
- [Pretrained model](https://drive.google.com/drive/folders/1x6GNHzAQkqL5eQmIcPTjVPb9D5dtx02W?usp=sharing) trained on participant 1