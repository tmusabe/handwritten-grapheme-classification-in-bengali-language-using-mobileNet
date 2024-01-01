
# Handwritten Grapheme Classification In Bengali Language Using MobileNet
This is implementation of 

The Bengali language comprises numerous graphemes, which are the smallest functional units in a writing system. Detecting these graphemes is crucial for developing an OCR application.

## Idea
OCR application is mostly used embeded devices. So we utilized a class of efficient models for mobile and embedded vision applications called [MobileNet](https://arxiv.org/pdf/2006.11239.pdf). Specifically, we used [MobileNetV2](https://arxiv.org/abs/1801.04381). Since each grapheme contains three components, it is multilabel classification problem. As a results, we modified the softmax layer to facilitate our multilabel classification problem. 
![Project](https://github.com/tmusabe/handwritten-grapheme-classification-in-bengali-language-using-mobileNet/assets/46952648/f5515fd9-6a13-4e95-94c9-1955d6b44a39)

## Dataset
We used [this](https://arxiv.org/abs/2010.00170) dataset which is also available in [Kaggle](https://www.kaggle.com/c/bengaliai-cv19). After downloading change ```$PATH$``` to the dataset directory. Then, run the following command sequentially to pre-proccess the data by getting inside the data directory.
```
python create_image_pickles.py
python create_folds.py
python create_chunk.py
```
## Training 
Training the model requires to specify the `TRAINING FOLDS`, `VALIDATION FOLDS`. In addition,`BATCH_SIZE, IMAGE_WIDTH, IMAGE_LENGTH, EPOCHS` can be also specified. Command for training:
```
python main.py --mode train  --training_folds ($Num1$, $Num2$, $Num3$, $Num4$) --validation_folds ($Num4$,)
```
![Workflow](https://github.com/tmusabe/handwritten-grapheme-classification-in-bengali-language-using-mobileNet/assets/46952648/26efdbc3-4299-4363-831a-daf60d6e6456)

## Testing
command for testing:
```
python main.py --mode test
```

## Citetation
If you find this codebase useful, please cite our paper:

## Acknowledgement
We follow the tutorial of [Abhishek Thakur](https://www.youtube.com/@abhishekkrthakur) Youtube Channel.
# Handwritten Grapheme Classification In Bengali Language Using MobileNet
