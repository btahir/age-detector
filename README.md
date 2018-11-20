# Age Predictor Application
Detecting A Person's Age In A Photo 

This project leverages Deep Learning to predict a person's age in a photo. I used the fastai library for Deep Learning: https://github.com/fastai/fastai

I used the IMDB-Wiki Dastbase for my data: https://data.vision.ee.ethz.ch/cvl/rrothe/imdb-wiki/

Specifically, I used the Faces Only data from Wikipedia in that dataset which is around 1 GB. I trained this on a resnet-50 model pre-trained on Imagenet.

Only images with age labels from 10-120 were selected so the model will not probably work well for photos of kids younger than 10 or...really really old people.

# Data Preparation

After downloading the data, you have to use the filenames to generate ages. The file names come in the fromat of the date of birth of the person in the picture and the year the photo was taken. Assumiing a mid year date of 7/1, we can extrapolate th age of the person at the time the photo was taken.

The Jupyter notebook has all the steps required to prep the data and genrate these labels.

# Model Training

I used a Resnet-50 pretrained on Imagenet for this project.

# Results

You can check out a live version of the app here: https://age-predictor.now.sh/

![alt text](https://github.com/btahir/age-detector/blob/master/example-photo.jpg)


### Citations

@article{Rothe-IJCV-2016,
  author = {Rasmus Rothe and Radu Timofte and Luc Van Gool},
  title = {Deep expectation of real and apparent age from a single image without facial landmarks},
  journal = {International Journal of Computer Vision (IJCV)},
  year = {2016},
  month = {July},
}

@InProceedings{Rothe-ICCVW-2015,
  author = {Rasmus Rothe and Radu Timofte and Luc Van Gool},
  title = {DEX: Deep EXpectation of apparent age from a single image},
  booktitle = {IEEE International Conference on Computer Vision Workshops (ICCVW)},
  year = {2015},
  month = {December},
}





