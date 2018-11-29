# Adaptive-hierarchical-SVM
#Multi-class classification:
training:
svm-train -k multiclass -t 2 -c 1 -g 0.1 "./sample dataset/multiclass classification/train.dat" "./sample dataset/multiclass classification/model"
testing:
svm-predict "./sample dataset/multiclass classification/test.dat" "./sample dataset/multiclass classification/model" "./sample dataset/multiclass classification/prediction"

#Multi-label classification:
training:
svm-train -k multilabel -t 2 -c 1 -g 0.1 "./sample dataset/multilabel classification/train.dat" "./sample dataset/multilabel classification/model"
testing:
svm-predict "./sample dataset/multilabel classification/test.dat" "./sample dataset/multilabel classification/model" "./sample dataset/multilabel classification/prediction"

#Hierarhical multi-label classification:
training:
svm-train -k hierarchical "./sample dataset/hierarhical multilabel classification/train.hf" -a 1 -f 1 "./sample dataset/hierarhical multilabel classification/train.dat" "./sample dataset/hierarhical multilabel classification/model"
testing:
svm-predict "./sample dataset/hierarhical multilabel classification/test.dat" "./sample dataset/hierarhical multilabel classification/model" "./sample dataset/hierarhical multilabel classification/prediction"
