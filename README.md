# Age Detector
Detecting A Person's Age In A Photo 

This project uses Deep Learning to guess a person's age in a photo. I used the fastai library for Deep Learning: https://github.com/fastai/fastai

I used the IMDB-Wiki Dastbase for my data: https://data.vision.ee.ethz.ch/cvl/rrothe/imdb-wiki/

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

Specifically, I used the Faces Only data from Wikipedia in that dataset which is around 1 GB. I trained this on a resnet-50 model pre-trained on Imagenet.






