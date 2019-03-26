X433-7 Machine Learning with Tensorflow Project

Title: Istanbul or Taipei?

Members: Aslihan Demirkaya & Shih-Chieh (Jerry) Hsu

Project Goal:
    Develop and train a system that can identify if the picture is taken in Istanbul or Taipei

Inside the folder:
1. demirkaya_hsu_project.ipynb: jupyter notebook that has the code.
2. demirkaya_hsu_project.pdf: .pdf version of the code.
3. Hsu_Demirkaya_Presentation.pdf: Presentation slides
4. istanbul_taipei folder: Data set of images of both sites
5. TensorBoard_Graphs_screenshots: Screenshots are taken after zooming in.
6. tensorboard_notebook2.py: is needed to have the tensorboard graphs on the jupyter   	notebook.


Overview:
    Project consist of two major modules:
        1) Flicker Downloader
        2) Image Classifier

    Flickr Downloader:
        Using Flickr API to download Istanbul and Taipei pictures from Flickr
        Scale down and save to folders accordingly

    Image Classifier:
        Tensorflow Keras high level API allows one to build graphs with pre-built layers 	and modules.
        In this project, we use MobileNet module and 'softmax' layer to build the model
        Using Flickr pictures to train and validate the model we built. We add more dense 	layers to improve the results.


Platform:
    - Mac OS HighSierra on Macbook Pro
    - Jupyter Notebook 5.7.2 and 5.5.0
    - Python 3.6.5


Packages:
    - Pillow(PIL) 5.4.1
    - matplotlib 3.0.2
    - numpy 1.16.1
    - tensorboard 1.12.2-1.13-1
    - tensorflow 1.12.0-1.13.1
    - flickrapi 2.4.0
    - panda 0.3.1

External Resources:
    - MobileNet_V2 on Tensorflow Hub: https://tfhub.dev/google/imagenet/mobilenet_v2_100_224/feature_vector/2"
    - Flickr API: https://stuvel.eu/flickrapi-doc/

Execution Sequences:
    0) place demirkaya_hsu_project.ipynb and tensorboard_notebook2.py in the same execution folder
    1) launch demirkaya_hsu_project.ipynb from Jupyter Notebook
    2) If image has not been downloaded yet, run code in the "Preparing the Data Set:" section to download pictures
       Skip to step 3) if pictures are already downloaded

       It takes about two hours to download pictures for each city.
       When running code in the "Preparing the Data Set:" section, make following changes accordingly

       a) Change redownload=False to redownload=True

       b) Change the following according to the downloading city
            keyword =  'istanbul' #'taipei'

       c) comment/uncomment the following code according to the downloading city

            pickle.dump(urls, open("istanbul_urls_flickr.pckl", 'wb'))
            !mkdir istanbul

            #pickle.dump(urls, open("taipei_urls_flickr.pckl", 'wb'))
            #!mkdir taipei

    3) After pictures are downloaded, run code in the "Image Classification using Tensorflow Hub with Keras"
       section sequentially.

       Some steps, such as training and validation, can take several minutes to complete