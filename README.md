# Representation-learning

Under Results folder you have two notebooks :

normal :
For this notebbok we have trained a resnet50 on on the original brain dataset. This dataset has 4 classes. 3 disease types and 1 healhty. We got 97 accuracy on test dataset with just training for 100 epochs and a fixed learning rate of 0.1. For this case our IID data is brain dataset and OOD data is chest dataset. For ood detection we know that energy scores work better than softmax scores but to report it I added both of them. 
How do we do OOD detection using softmax scores  ? 
After training the model you feed your brain test dataset to model and get softmax scores. After getting the softmax scors for each class you pick the highest softmax score. 
max_brain = max_softmax_score(brain_softmax_scores)
max_chest = max_softmax_score(chest_softmax_scores)

I have also added a KDE plot which shows the ditsribution of IID(brain dataset )   and OOD(chest dataset) softmax  scores. After that we use a thresholding function. Basically a line seperating these two scores with minimum erorr. The plot under KDE is this one. Also pon top of the table it includes the farction of falsly classified data( OOD or IID not classification error ). 

For energy OOD detection :
We use the denominator of softmax and apply the nergy transformation for each data point (like explained in the paper, you dont have to explian how energy score is calculates just reference to the energy paper ). You can also find the KDE and thresholding function plot for OOD scores. For this case energy gave worse results in OOd detection than softmax but with very little difference ( just repoting it would be fine bc we are not arguing if energy is better than softmax ) . I have also added true positive rates and other stuff for results of OOd detection using energy scores. Since energy paper concluded that energy score is better than softmax I have only calculates this measures for energy scores.

Segmented notebook :
Model was trained exactly in same structure , 100 epochs learning rate also fixed to 0.1. 
Same experiment done with this notebook but now we have the segmneted dataset for brain and segmenetd dataset for chest. You can see that accuracy dropped to 30% and model gave same sfotmax scores thus same energy scores for each image making it impossible to speerate between. For this experiment you can report accuracy dropped to 30 percent and bc accuracy dropped and model gave same softmax score for each image, model did not learn so we OOd also failed.

