# Covid-X-ray
A project of a **Computer Vision Deep Learning model** for **Covid-19** and pneumonias Xray images classification.

#### IMPORTANT! 
All the conclusions from this project should undergo a thorough clinical study, so it is not possible to validate any conclusion without a valid clinical test.

## The Project
This project has been developed in May 2020 and intends to evaluate a deep learning model for classification of Xray images coming from various kind of pneumonia included Covid-19, using keras and Tensorflow
<p align="center">
  <img src="https://github.com/sandrofab/Covid-X-ray/blob/master/dataset_for_classification/COVID/1-s2.0-S1684118220300682-main.pdf-002-a1.png?raw=true" height="300">
  <img src="https://github.com/sandrofab/Covid-X-ray/blob/master/dataset_for_classification/NORMAL/IM-0145-0001.jpeg?raw=true" height="300" alt="accessibility text">
  <br>
    <em>Fig. 1: On the left Covid-19 XRay, on the right normal lungs Xray </em>

</p>


Is there a way for a deep learning computer vision model to tell the difference between various king of pneumonia by  Xray images?

### How this repository is structured
Here is a description of folders and files in this repository
* [dataset_for_classification](https://github.com/sandrofab/Covid-X-ray/tree/master/dataset_for_classification) - here you will find x-ray images split in 4 self explaining subfolders. The Covid Xray images are taken from the Covid project of Dr. [Joseph Paul Cohen](https://github.com/ieee8023/covid-chestxray-dataset). Some randomly selected images have been taken only if they were covid positive and in PA (posteroanterior) view. The other images have been randomly taken from [Kaggle Chest X-Ray Images Pneumonia dataset](https://www.kaggle.com/paultimothymooney/chest-xray-pneumonia)
* [Scripts and Notebooks](https://github.com/sandrofab/Covid-X-ray/tree/master/Scripts%20and%20Notebooks) - a folder with scripts and Colab notebooks with code used for the pre-processing tasks and model training. So far i included the **covid19_multiclass.py** file, that i used to train the model in the case of a 4 classes scenario, and the **covid_binary.py** file that i used in the case of covid/no-covid scenario (everything is explained in detail in the [project report](https://github.com/sandrofab/Covid-X-ray/blob/master/Covid-project-report.pdf)).
* [Plots](https://github.com/sandrofab/Covid-X-ray/tree/master/plots) - Plots with losses and accuracies in different scenarios- For **binary classification** scenario classification reports are included. Note that in this case we achived 0.98 F-score for covid detection
<p align="center">
  <img src="https://github.com/sandrofab/Covid-X-ray/blob/master/plots/binary-scenario/Bin_InceptionResNetV2_Amsgrad_20epo_DA_FT.JPG?raw=true">
  <br>
    <em>Fig. 2: Classification Report for binary Classification scenario </em>

</p>



In the file [Covid-project-report.pdf](https://github.com/sandrofab/Covid-X-ray/blob/master/Covid-project-report.pdf) you will find the report and all the steps i followed to train the model and achieve some conclusions.

## Conclusions and further investigations
* The trained model seems to be accurate on this dataset but what is
really detecting? Remember that the Xray images come from 2
different datasets for what concerns Covid and No‐Covid, is there
any chance the model is detecting this difference maybe in the way
the X‐ray images were taken?
* The dataset is still too small for this purpose it would be useful to
make the same training on a larger dataset
