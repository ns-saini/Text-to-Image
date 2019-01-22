# Text To Image Synthesis Using Thought Vectors

This is an experimental tensorflow implementation of synthesizing images from captions using [Skip Thought Vectors][1]. The images are synthesized using the GAN-CLS Algorithm from the paper [Generative Adversarial Text-to-Image Synthesis][2]. This implementation is built on top of the excellent [DCGAN in Tensorflow][3]. The following is the model architecture. The blue bars represent the Skip Thought Vectors for the captions.

## Requirements
- Python 2.7.6
- [Tensorflow][4]
- [h5py][5]
- [Theano][6] : for skip thought vectors
- [scikit-learn][7] : for skip thought vectors
- [NLTK][8] : for skip thought vectors

## Datasets
- All the steps below for downloading the datasets and models can be performed automatically by running `python download_datasets.py`. Several gigabytes of files will be downloaded and extracted.
- The model is currently trained on the [flowers dataset][9]. Download the images from [this link][9] and save them in ```Data/flowers/jpg```. Also download the captions from [this link][10]. Extract the archive, copy the ```text_c10``` folder and paste it in ```Data/flowers```.
- Download the pretrained models and vocabulary for skip thought vectors as per the instructions given [here][13]. Save the downloaded files in ```Data/skipthoughts```.
- Make empty directories in Data, ```Data/samples```,  ```Data/val_samples``` and ```Data/Models```. They will be used for sampling the generated images and saving the trained models.



[1]:http://arxiv.org/abs/1506.06726
[2]:http://arxiv.org/abs/1605.05396
[3]:https://github.com/carpedm20/DCGAN-tensorflow
[4]:https://github.com/tensorflow/tensorflow
[5]:http://www.h5py.org/
[6]:https://github.com/Theano/Theano
[7]:http://scikit-learn.org/stable/index.html
[8]:http://www.nltk.org/
[9]:http://www.robots.ox.ac.uk/~vgg/data/flowers/102/
[10]:https://drive.google.com/file/d/0B0ywwgffWnLLcms2WWJQRFNSWXM/view
[11]:https://github.com/reedscot/icml2016
[12]:https://github.com/ryankiros/skip-thoughts
[13]:https://github.com/ryankiros/skip-thoughts#getting-started
[14]:https://bitbucket.org/paarth_neekhara/texttomimagemodel/raw/74a4bbaeee26fe31e148a54c4f495694680e2c31/latest_model_flowers_temp.ckpt
[15]:https://github.com/zsdonghao/dcgan
[16]:https://github.com/zsdonghao/text-to-image
