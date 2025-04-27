# Graffiti_Picture_Classifier

The following story is made up and **fully fictional**!  


I am working in the data science unit of the city Hamburg and will develop following experiment: In this project I will develop a software which detects graffiti based on pictures. The potentially successful graffiti detector will be applied to the surveillance cameras in Hamburg to automatically detect graffiti. So far, this has been done irregularly by several employees. This is expensive and organizational effort. In addition, the metric of how certain the model is about a detection is used to prioritize the cleanings. This means that graffiti can be combated more effectively. There are a number of positive effects, such as higher property prices and a better sense of well-being. The goal will be to develop a deep learning model which can do exactly that. The data was taken by me using my phone. I will go later more into detail about the data. The project is therefore a binary classification between graffiti and no graffiti.

## Data
To train and evaluate a model it is necessary to have data. I took 883 pictures in Kiel within of approx. 4 hours.

| Category              | Number of Pictures | Percentage |
|-----------------------|--------------------|------------|
| Graffiti Pictures      | 452                | 53.9%      |
| Non-Graffiti Pictures  | 386               | 46.1%      |
| **Total**              | **838**            | **100%**   |

If you are interested in the data, contact me.

## Results
I used a dummy classifier and a support vector machine as a baseline. No classification power could be archieved. A optimized ResNet-18 architecture was used for the model. The results can be seen here:

| Algorithm          | Dataset | Balanced Accuracy | AUC   | Trainable Params |
|--------------------|---------|-------------------|-------|-------------------|
| Modified_ResNet18  | train   | 0.84              | 0.91  | 65793            |
| Dummy Classifier   | train   | 0.50              | 0.50  | 0                |
| SVM                | train   | 0.50              | 0.50  | 2                |


| Algorithm          | Dataset | Balanced Accuracy | AUC   | Trainable Params |
|--------------------|---------|-------------------|-------|-------------------|
| Modified_ResNet18  | test    | 0.79              | 0.90  | 65793            |
| Dummy Classifier   | test    | 0.50              | 0.50  | 0                |
| SVM                | test    | 0.50              | 0.50  | 2                |



