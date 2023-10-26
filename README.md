# Representation-learning

# Effect of Segmentation on OOD and effect of high Resolution on Energy Scores

In this project we have explored the effects of segmentation on OOD and classification accuracy. We have also investigated how energy scores perform on high resolution images. 

## Description

A very detailed description and the methodlogy we followed can be found on paper. 
## Structure of the Repo
* Results for effect of Segmentation on OOD detection and classification accuracy can be found under Results folder which contains 3 experiments.
* Results for effect of high reoslution on energy scores can be found under High_res_energy_exp folder which contains two experiments. 

### Dependencies

* Pytorch
* Python
* Matplotlib
* PILImage
* Numpy

### Links to Datasets

* [Brain Tumor MRI](https://www.kaggle.com/datasets/masoudnickparvar/brain-tumor-mri-dataset)
* [Bone Break Classifier](https://www.kaggle.com/datasets/amohankumar/bone-break-classifier-dataset?rvi=1)
* [Chest X-Ray](https://www.kaggle.com/datasets/tolgadincer/labeled-chest-xray-images?rvi=1)
* [Brain Tumor Dataset (Different Format)](https://www.kaggle.com/datasets/jakeshbohaju/brain-tumor?rvi=1)
* [Segmented Brain Tumor MRI](https://www.kaggle.com/datasets/sgcoder1/segmented-brain?rvi=1)


### Pth Files

* Related pth files for models can be found under pth folder.


## Help
* We have found out that segmentation of images takes a lot of processing power and time. To run this experiment on different datasets we recommend powerful GPUs with high memory. 

## Authors

Contributors names and contact info

Sarp Gol : s.gol@student.tue.nl

Horatiu Sicoie : h.sicoie@student.tue.nl

Danila Solodennikov : d.solodennikov@student.tue.nl

Amir Ali Hashemi : s.a.a.hashemi@student.tue.nl

Darshan Sudheer Amadalli : d.s.amadalli@student.tue.nl


## Acknowledgments

Inspiration, code snippets, etc.
* [Energy Paper](https://github.com/wetliu/energy_ood)
