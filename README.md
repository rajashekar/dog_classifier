
# Dog image classifier 
This project classifies given images as dog image or not. 

## Pre-requisites
- Python 3
- Anaconda 

## Getting Started
### Clone Repository 

```
git clone https://github.com/rajashekar/dog_classifier.git
cd dog_classifier
```

Create the environment 
```
conda env create -f environment.yml
```
Once dog_classifier environment is created. Activate the environment
```
conda activate dog_classifier
```
Run the check images to classify images
```
python check_images.py
```
Sample output 
```
CNN Model : vgg
Number of Images : 40
Number of Dog images : 30
Number of Not-a Dog images : 10
100.00% Correct Dogs
93.33% Correct Breed
100.00% Correct Not-a Dog
87.50% Match

** Total Elapsed Runtime: 0:0:19
```
By default `vgg` is used, to use different arch like `resnet` you can do like below
```
python check_images.py --dir pet_images/ --arch resnet  --dogfile dognames.txt
```
To check the classification based on `alexnet` 
```
python check_images.py --dir pet_images/ --arch alexnet --dogfile dognames.txt
```
To run as batch to compare results of `vgg`, `resnet` and `alexnet`
```
sh run_models_batch.sh
```