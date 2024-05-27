# Titanic_data_set
i'll be working with titanic dataset from kaggle.com

There's 3 files from kaggle.com :
- train
- test
- submission

The train file contains 891 entries and 12 columns :
 
- PassengerId
- Survived : 0 = died , 1 = Survived
- Pclass : 1 = 1st, 2 = 2nd, 3 = 3rd
- Name : Name of the passangers
- Sex : male or female
- Age  : Age of the passangers
- SibSp : Sibling = brother, sister, stepbrother, stepsister
          Spouse = husband, wife (mistresses and fiancés were ignored)
- Parch  : Parent = mother, father
           Child = daughter, son, stepdaughter, stepson
- Ticket : Ticket entitled
- Fare : Price of the ticket
- Cabin : Cabin of each passanger
- Embarked : Port of Embarkation 
             C = Cherbourg, Q = Queenstown, S = Southampton   

 ![Capture d'écran 2024-05-27 165913](https://github.com/medayoubaziz1993/Titanic_data_set/assets/162934368/7aab3d62-5e51-4306-81c6-4ad8815c489e)             

Since our target or our goal is to predict if the passanger will die or survive ,
the test file contains the same columns as the train file except for "Survived" column
and it has 418 entries 

For the submission file it contains the necessary form of the submission :
- PassengerId
- The prediction of our model 


To begin with , i tried to understand the data :

 ![téléchargement (1)](https://github.com/medayoubaziz1993/Titanic_data_set/assets/162934368/981e0a12-9b5e-486b-aafc-0c780e225edf)

The age of the passangers goes from 0 to over 80 but most of them are between 20 and less than 40 .

![téléchargement](https://github.com/medayoubaziz1993/Titanic_data_set/assets/162934368/3e64a851-04a9-461a-8f2b-02e755f21080)

As we can see from this plot that the survivers are less than the dead , they represent 38,38% from the passangers on the train data set .

![téléchargement (2)](https://github.com/medayoubaziz1993/Titanic_data_set/assets/162934368/7fb4cd51-fc88-4dfa-8ac7-27599097eb0d)

![téléchargement (3)](https://github.com/medayoubaziz1993/Titanic_data_set/assets/162934368/1c93bacc-ad4e-4b39-bbec-89891c89eb75)

when we look at the two plots we can agree that the number of males that died are more than the females .

After that i tried to clean the data by inputing the missing data , removing the unecessary columns that will not help our model to train on the data so it could predict the survived ones 

I used two known models for this data :

- LogisticRegression

- DecisionTreeClassifier 

after tuning the parameters of those two model i ended up with DecisionTreeClassifier since it gives me the better result with 89% accuraccy .
