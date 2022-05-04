# **Dataset 1: Diabetes indicators with outcomes**

# Description

## Dataset Format: Tabular

The [dataset](https://www.kaggle.com/shantanudhakadd/diabetes-dataset-for-beginners) that I first chose was a csv that contained items and attributes about indicators of people that might or might not have diabetes. That is to say that you could use this dataset for a machine learning model to predict if given the different attributes such as blood pressure, BMI, age, etc. you could predict their diabetes status. While I am not using the &quot;Outcome&quot; column for this assignment, the dataset sill serves to be useful with 768 rows and 9 columns. They include, number of pregnancies, glucose, blood pressure, skin thickness, insulin, BMI, diabetes pedigree function, age, and then the outcome.

## Data Type: Items

I chose to say that this table was made up of item-based data points as each one represents a specific person or patent. Each of those rows is a singular person correlated to their specific metrics in the columns.

## Attribute Types and Semantics

For this dataset there are both attributes that are categorical and quantitative. The categorical attribute would be the outcome column. That column represents whether or not the patent has diabetes with 1 being diabetes and 0 being no diabetes. That represents a categorical attribute. The rest are qualitative. They are all numerical values that have meaning and are a measurement of something. The real world meaning, or semantics of this data is that each of these 8 columns serve to be an important indicator of someone who could be diabetic. Something that I learned when using this dataset is that women after pregnancy have a slight increased risk of developing type 2 diabetes, especially if they developed gestational diabetes during [pregnancy](https://www.cdc.gov/reproductivehealth/maternalinfanthealth/diabetes-during-pregnancy.htm). While BMI is not a perfect measurement, it does show that people with higher BMI could potentially have a greater risk of developing or having diabetes. Each one of these columns is a pertinent measurement for someone with or at risk of developing diabetes.

## Preprocessing

For preprocessing, apart from just loading in my data I did not do any preprocessing. However when I actually visualized my data I filtered the data frame down to just people with diabetes

## Visualization

_Figure 1 Correlation Heat Map_

 Before I started visualizing, I wanted to plot a quick correlation heat map for the table. After plotting my heat map, I moved into my first visualization which was plotting four dimensions. I am working with python so again I chose to use plotly express for my visualizations for this first one. I decided to do a 3d scatter plot. I first filtered down the outcome column to people with diabetes. Then I chose to put the age column on the x axis, blood pressure on the y axis and glucose on the z axis. Those were my three dimensions, for my four dimension I decided to color each point by the BMI column. I t ![](RackMultipart20220504-1-xnk7tf_html_6545707ef75b26bf.png) hen changed the size of each point to be smaller as it was a little hard to see a first. Next I decided to run the PCA on this dataset using sklearn.

![](https://i.imgur.com/ZwdE3Zy.png)

![](https://i.imgur.com/NmarWvJ.png)

![](https://imgur.com/iDgeJdK.png)

![](https://imgur.com/ZZWvsw1.png)


## Analysis

To start I will talk about the correlation heatmap. The first thing I noticed is that there is a correlation between 2 areas. Age and pregnancy and glucose and outcome. These two correlations make logical sense to me as to have more kids you would need to be physically older. Furthermore, glucose is a direct indicator of diabetes status. That is a good sign that there is a correlation between those two areas. I ended up with choosing the 3d scatter plot for this as I thought it would work the best. However, I am not so sure. I think you could make it look better by possibly not using plotly. Nevertheless, as you can see in the visualization people tend to be higher up on both the blood pressure and glucose side of the scales. This makes sense as people with diabetes tend to have high blood pressure. Those two attributes are 2/3 of what some refer to as the &quot;diabetes trifecta&quot;. That is High blood pressure, high glucose, and high cholesterol. As expected, the BMI did play too much of a role in telling us too much. Without knowing their height, and weight BMI serves no real purpose other than being a classifying ratio.

# **Dataset 2: Health Insurance**

# Description

## Dataset Format: Tabular

For the second [dataset](https://www.kaggle.com/shivadumnawar/health-insurance-dataset) I chose a ­dataset that represented individuals&#39; health care spending with factors such as age, BMI, children, smoking status, region, and finally their healthcare charges. Again, this is another flat, tabular dataset containing 1338 rows and 7 columns

## Data Type: Items

Again, this table has item-based data types with each column corresponding to a specific row or person here.

## ­­Attribute Types and Semantics

The dataset is made up of both categorical and quantitative data types. For example, the &quot;sex&quot;, &quot;smoker&quot;, and &quot;region&quot; columns are categorical datatypes. The rest are all quantitative. The real world meaning behind these are how they are all classic health care indicators for things. Especially BMI and smoking status. Typically they are used for indicators on higher health care cost.

## Preprocessing

The only preprocessing for this dataset was fixing the column names. There was either an issue downloading it or it was like that when uploaded to Kaggle but regardless there was an extra a space or white space tacked on to the end of each column name. I fixed that no programmatically but jut in excel as there were only a few columns.

## Visualization

The visualization I wanted to show was using five of the dimensions in this dataset. I chose to use a 2d or flat scatter plot using plotly express again. I showed the age of the person on the x axis, the BMI of the person on the y axis. Those were my first two dimensions. For the third dimension I chose to color each point by if there were either a smoker or not. For the fourth dimension I chose to differentiate each point by using a different symbol if they were whether male or female, finally to add the fifth dimension, I chose to represent their insurance cost by utilizing the size of each point. Next, I decided to also create a correlation heatmap using seaborn again.

![](https://i.imgur.com/I5eFA8K.png)

# ![](https://i.imgur.com/3aEuRcz.png)

#

#

#

#

# Analysis

As we can see there is a clear trend in the higher the BMI you have, the higher your insurance charges are. Furthermore, the people with the highest insurance charges are those with high BMIs, smokers, and are males. To me I read this as men possibly only go to the doctor for very major things, thus its very expensive, whereas females possibly practice more preventative care which leads to lower cost. Smoker or not, men&#39;s insurance chargers are a lot higher. Looking at the correlation plot we can see there is somewhat of a correlation between age and cost, as well as BMI and cost at 0.3 and 0.2 respectively.

#

# **Dataset 3: students**

# Description

## Dataset Format: Tabular

For the third [dataset](https://www.kaggle.com/spscientist/students-performance-in-exams) I chose a ­dataset that represented students scoring on exams. They were graded on their reading, writing, and math. Furthermore, there were other data points such as their gender, parents level of education, race/ethnicity, test preparation etc. The table has 1000 rows and 8 columns.

## Data Type: Items

The student dataset is also made up of item-based data types with each column corresponding to a specific row or test taker in this case.

## ­­Attribute Types and Semantics

In terms of attribute types, the table has mostly categorical data which made it interesting to visualize. The columns of gender, race/ethnicity, parents&#39; level of education, lunch, test preparation were all categorical. The remain three of math, reading, and writing scores were all quantitative. These all have real world meaning. They are key metrics to possibly predicting someone&#39;s outcome on a test. For example, it would be easy to assume that the person with the highest level of parental education and most test prep would score higher than the opposite.

## Preprocessing

For preprocessing I did not to do anything and uses the table as is.

## Visualization

Since this was the final visualization, I needed to visualize six dimensions. First, I yet again used a seaborn correlation heatmap first. After that I chose my 6 dimensions to visualize. I started by choosing my plot type. I again used a 2d scatter plot with reading scores on the x axis and writing scores on the y axis. However, this time I utilized facets and split each plot by race ethnicity. That gave us three dimensions to start. I then added in a color which was based on gender to give us the fourth dimension. For the fifth dimension I chose to use the size which was based on the math score. And finally for the 6th dimension I used a different symbol for each of the different parental levels of education which gave us all six dimensions. ![](RackMultipart20220504-1-xnk7tf_html_968b3194fe595b9.png)

![](https://i.imgur.com/G29nPUU.png)

![](https://i.imgur.com/NMpUwdG.png.png)

## Analysis

While not immediately obvious due to the picture that I was able to capture of the visualization. There appeared to be a small correlation between parents&#39; level of education and test scores being slightly lower. If we look at these: ![](RackMultipart20220504-1-xnk7tf_html_96d42e8f81016862.png)

Which are scores that are from 60 and lower, we see there are lot more &#39;+&#39; representing only parents having high school education. That&#39;s not to say there aren&#39;t plenty of people scoring low whose parents have a bachelor&#39;s degree though. Furthermore, the biggest correlation in this dataset is between the scores. Especially between reading and writing. That makes perfect logical sense to me. I think that next time I would assign a numerical value to each of the categorical columns to see if there is a correlation between the parent&#39;s level of education and testing lower.
