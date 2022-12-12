Data Science Final Project Report

Kia Aalaei

Dataset: https://www.kaggle.com/datasets/seymasa/rice-dataset-gonenjasmine 

I decided to choose this project because I was scrolling through all of the possible datasets to use and this one really stood out to me.
I had no idea that there were so many ways to describe and measure a rice, and those were the deciding factors as to what type of rice it was.
I have always had a fascination for rice due to my persian heritage, every single food in persian culture includes some sort of rice.
The classification of two different types of rice stood out to me in that way.

The Purpose of this project was to find the best fit to help classify a specific dataset that involved two different types of rice, Gonen and Jasmine.
The dataset had a little over 18,000 entries, based on these different columns: ID, Area, MajorAxisLength, MinorAxisLength,	Eccentricity,	ConvexArea,	EquivDiameter,
Extent,	Perimeter,	Roundness,	AspectRation, and	Class. All of which I was not expecting as different parameters to determine rice.

First, I imported the required libraries for this project.

![image](https://user-images.githubusercontent.com/120366695/206996007-654bff8a-8686-4e8e-8d9c-6d5e16469a96.png)

Then I had to import the actual dataset into jupyter using the seaborn load dataset function. I named the actual dataset 'rice'.

![image](https://user-images.githubusercontent.com/120366695/206996175-3dbfbe59-c37d-4d51-a54c-790503b864a3.png)

Next, to view the actual data, I used the head() function to see the first few entries to make sure every column was there.

![image](https://user-images.githubusercontent.com/120366695/206996397-3682c528-63ac-4181-9b90-4d5ca80ee856.png)

Next I decided to use the info() function to look for any null values that may be within the dataset and there was none.

![image](https://user-images.githubusercontent.com/120366695/206996594-c1746ebf-d6ee-4923-9d79-e23c7374862f.png)

The first was to divide the dataset into features and labels, this is due to the fact that I know what classification each row goes into.
I already know the data. I give features the variable x and labels the variable y. 
I use the drop() function to drop the columns ID and class for my features, this is because I don't want the ID numbers as a part of my testing data.
I also do not want the Class column because that is my label that corresponds to the specific features.

![image](https://user-images.githubusercontent.com/120366695/206997413-d5bd5d63-df81-4db5-88a3-2f7ddc207845.png)

And for the labels y, I just need the Class column.

![image](https://user-images.githubusercontent.com/120366695/206997659-f1f52bfa-a26b-4994-adb5-ae4d692da4fe.png)

I then use the seaborn pairplot function to see the different plots created between the features. The picture is too big to fit on the screen,
but the full picture can be found in the jupyter textbook

![image](https://user-images.githubusercontent.com/120366695/206998066-a4852f46-e762-481b-8ab3-b009ec92dbba.png)

After the creation of the features and labels, I want to split my dataset into training and testing, and I chose 33% of the dataset to be used for testing,
67% of the dataset will be used for training. I use the train_test_split() function to split the dataset and create different test and train variables for x and y.

![image](https://user-images.githubusercontent.com/120366695/206998669-09249e1a-7014-451f-a3c7-22e156f39af4.png)

For the method to use for classification, I looked at the Scikit-learn algorithm cheat sheet that shows what method would work best for your classification.
I started at the beginning, I definitely have more than 50 samples, I already have labeled data and less than 100k samples, so the best option for me was the
Linear SVC, and that is what I used.

![image](https://user-images.githubusercontent.com/120366695/206999199-081a359d-5ee1-4a76-9e23-113bbfe58e0f.png)

I then intialized the Linear SVC.

![image](https://user-images.githubusercontent.com/120366695/206999323-09cea6ef-3ed2-42dc-915b-fa6a43ad42ef.png)



























































