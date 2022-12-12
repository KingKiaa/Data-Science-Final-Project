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

