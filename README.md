# Pytorch-UNet 2.0 for noisy microarray image segmentation
![input and output for a random image in the test dataset](https://framapic.org/OcE8HlU6me61/KNTt8GFQzxDR.png)


This is forked version of https://github.com/milesial/Pytorch-UNet. To know more about it, 
[Click Here For Original Edition](https://github.com/milesial/Pytorch-UNet) 

## Usage
**Note : Use Python 3**
### Prediction

You can easily test the output masks on your images via the CLI.

To see all options:
`python predict.py -h`

To predict a single image and save it:

`python predict.py -i image.jpg -o output.jpg`

To predict a multiple images and show them without saving them:

`python predict.py -i image1.jpg image2.jpg --viz --no-save`

You can use the cpu-only version with `--cpu`.

You can specify which model file to use with `--model MODEL.pth`.

### Training

`python train.py -h` should get you started. A proper CLI is yet to be added.
## Warning
In order to process the image in training phase, every 512x512 input image is split into 16 squares of 128x128  and each square is passed into the net. 
For testing/predict phase, no size restriction.

## Dependencies
This package depends on [pydensecrf](https://github.com/lucasb-eyer/pydensecrf), available via `pip install`.


