# Age Predictor Application

This project leverages Deep Learning to predict a person's age in a photo.

I used the fastai library for Deep Learning: https://github.com/fastai/fastai

I used the IMDB-Wiki Dastbase for my data: https://data.vision.ee.ethz.ch/cvl/rrothe/imdb-wiki/

Specifically, I used the Faces Only data from Wikipedia in that dataset which is around 1 GB. I trained this on a resnet-50 model pre-trained on Imagenet.

# Data Preparation

The Jupyter notebook has all the steps required to prep the data and generate labels.

Once downloaded and untarred, the data is divided into subsets and stored in folders numbered 01–99. A python snippet in the notebook will loop through the directories and move all the files into one folder where the model could consume it.

There is no separate file for labels but rather they are within the filenames of the images themselves. The images in the dataset have filenames that include the date of birth of the person and the year the picture was taken. Using these, and assuming a mid-year date of 7/1 for when the photo was taken, we can come up with a good estimate of the age of the person in the photo when it was taken.

Another snippet of python code in the notebook will derive the age from these two dates to get the labels. To keep it simple for now, I selected only images from ages between 10–120. This means the model will not work for really young kids…or really really old people. The final data looks like this:

![alt text](https://github.com/btahir/age-detector/blob/master/data_batch.jpg)

# Model Training

I used a Resnet-50 pretrained on Imagenet for this project.

# Results

You can check out a live version of the app here: https://age-predictor.now.sh/

![alt text](https://github.com/btahir/age-detector/blob/master/example-photo.jpg)


# Citations

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

Check out Fastai if you want to get into Deep Learning. It's awesome: https://www.fast.ai/



